# **Version 10.2**

> **RELEASE DATE**
>
> October 30, 2020

The new Intelligent Automation Cloud v.10.2 provides you with a set of innovations to increase productivity and simplify your routine work. This release includes but is not limited to the following features:

> • **WorkSpace 2.0** is a human-in-the-loop tool designed to tackle various issues with the exception handling process, allowing faster completion and improving compliance. WorkSpace 2.0 improves upon the previous version with a new feature that enables you to manipulate and adjust the workflow.
>
> • With the new **A/B testing** feature, you can validate automation variations, review Analytics dashboards for test results, and choose the most confident automation version, thus improving the performance of pretrained bots.
>
> • **Automated retraining** allows you to start retraining on a collected training set, know the estimated duration, and see Analytics for validating models. The bot retraining workflow, now available in the Control Tower UI, becomes even more friendly to business users.
>
> • **Centralized user management and role-based access control** are introduced to rule all of the ecosystem components, including Analytics dashboards and WorkSpace.
>
> • **Analytics** introduces 20 new data points, drill-down capability, improved navigation, and simplified, user-friendly analysis.
>
> • **Intelligent automation cloud developer** updates include the new Launcher application for components management and other improvements to your local development environment.
>
> • **ML SDK** extensions address complex problems, including but not limited to hybrid models, grouping, and classification cascade training.
>
> • **Optimized orchestration** of services allows you to reduce hardware requirements to 11 servers for a high-availability environment.
>
> • Additional bug fixes, improvements, and deprecations address user requests and solve earlier flaws.

For more information on each improvement, see detailed descriptions below.

## **A/B Testing of the Use Cases**

The A/B testing functionality enables you to easily test adjustments to or new versions of automation and gather key metrics to determine whether to implement these changes in the production environment.

The intuitive workflow makes the whole procedure easy to run, and data is available for comparison after actual testing.

With the help of A/B tests, you can:

> • safely run data, historical or live, through a new version without impacting the original version.
>
> • manage variations of business processes to be tested.
>
> • test updated manual task efficiency and routing.
>
> • automatically gather data to measure and compare two different versions.
>
> • analyze business metrics and compare versions.

## **Bug Fixes**

### **Infrastructure**

> • Fixed an issue with Logstash start-up failing and secrets not being taken from Secrets Vault.
>
> • Fixed a bug that caused a failure to work jobs when cloning from the current directory.
>
> • Fixed a certificate error that made Logstash unable to start.
>
> • Fixed an issue on the \"Run postmigrate SQL script\" step.
>
> • Fixed an issue that caused the ports prechecker not to work when the FirewallD service blocks ports.
>
> • Fixed an issue with the update_artifacts task failing when running on the HA environment.
>
> • Fixed a Liquibase error when upgrading.

