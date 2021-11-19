**Bot Tasks** contain work to be completed by WorkFusion's Bots, which perform the steps in your Business Processes that are more suited for automation than human labor. A Bot Task can only exist as a Business Process step.

Examples of Bot Tasks include address parsing, determining the width and height of an image, interacting with your API or repository, and filtering content that does not meet certain criteria.

**Bot Configs** are written using Web-Harvest library and executed for each Record separately. To write Web-Harvest XML configs, you can use WorkFusion plug-ins or predefined Web-Harvest XML elements described here.

**Bot Config Bundle** is a bundled Java library containing a Bot Config and a Java code reference that can be used in this Bot Config.

## **How to Create, Test, and Run a Bot Task**

> 1. Create and test a Web-Harvest config using the WorkFusion Studio (Eclipse-based IDE).
>2. Create a Bot Use Case in WorkFusion. Choose the Bot Use Case type (it is best practice to choose ETL because it adds flexibility and is better for reuse).
> 3. Create a BP and include a Bot Step based on this Use Case. Alternatively, you can use WorkFusion Repository to import a Bot Config Bundle to WorkFusion.
>4. Test the Bot Config in BP using a small input batch.
> 5. Make changes, if needed, to column names, use proxy, datastore connection, or output column names.
>6. Update the created Bot Use Case and use it in your production BP.

Alternatively, you can create a Bot Task in BP (under the Design Process tab) from scratch (Blank Use Case) and paste your code, but this approach leads to multiple issues.

## **Execution Details**

XML configuration executes for each submission. If your input CSV file contains 40 Records, the Web-Harvest XML configuration will be executed 40 times (once for each Record).

If an error occurs, the Bot Config will run 5 times.

## **Results**

The results of a Bot Task are defined in the \<export> plug-in settings.

All of the columns created by the Bot Task can be used in further BP steps (both Manual and Bot).

## **Hello World Example**

The following example:

> 1. gets HTTP response from URLs listed in the **url_to_check** column of the input data file;
>2. records the HTTP response into the **http_response** variable;
> 3. exports all original columns and appends a new **http** column containing the **http_response** variable value.
>

### **Bot Config Example**

"<?xml version="1.0" encoding="UTF-8"?>

<config>

​     <!\--defining variable\--\>

​     <var-def name=\"http_response\"\>

​          <!\--passing the appropriate value from url_to_check column in input data file as a parameter for http plug-in\--\>

​          <http url=\"\${url_to_check}\"\>\</http>    </var-def>



​     <!\--exporting all original input columns\--\>

​     <export include-original-data=\"true\"\>

​         <!--adding a new column with the http plug-in result to the export file\--\>

​         <single-column name=\"http\" value=\"\${http_response}\"/> \</export>

\</config>"
