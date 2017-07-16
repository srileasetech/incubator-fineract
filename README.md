Apache Fineract: A Platform for Microfinance
============

The next evolution of Apache Fineract focuses on being faster, lighter and cheaper to change (than the existing Mifos) so that it is more responsive to the needs of Microfinance Institutions and Integrators.

Requirements
============
* Java >= 1.8 (Oracle JVMS have been tested)
* gradle-wrapper.jar version 2.10
* MySQL 5.5

Instructions to build war file
============

1. Extract the archive file to your local directory.
2. Download gradle-wrapper.jar version 2.10 and place it in the fineract-provider/gradle/wrapper folder.
3. Change the current working directory to fineract-provider.
4. Run `./gradlew clean war` or `./gradlew build` to build deployable war file which will be created at fineract-provider/build/libs directory.


Instructions to execute Integration tests
============
1. Login to mysql DB using `mysql -u root -pmysql`
2. Create the mifosplatform-tenants database using `CREATE DATABASE mifosplatform-tenants`.
3. Create the default tenant database using `CREATE DATABASE mifostenant-default`.
4. With fineract-provider as current working directory run the following commands:
	1. `./gradlew migrateTenantListDB -PdbName=mifosplatform-tenants`
	2. `./gradlew migrateTenantDB -PdbName=mifostenant-default`
5. Run `./gradlew clean integrationTest`

Version
============

The latest stable release can be viewed on the develop branch: [Latest Release on Develop](https://github.com/apache/incubator-fineract/tree/develop "Latest Release"), [View change log](https://github.com/apache/incubator-fineract/blob/develop/CHANGELOG.md "Latest release change log")

License
============

This project is licensed under Apache License Version 2.0. See <https://github.com/apache/incubator-fineract/blob/develop/LICENSE.md>.

Apache Fineract Platform API
============

The API for the Fineract-platform (project named 'Apache Fineract') is documented in the API-docs under <b>Full API Matrix</b> and can be viewed [here](https://demo.openmf.org/api-docs/apiLive.htm "API Documentation").

Online Demos
============

* [Community App](https://demo.openmf.org "Reference Client App")

Developers
============
Please see <https://cwiki.apache.org/confluence/display/FINERACT/Contributor%27s+Zone> for the developers wiki page.

Please see <https://cwiki.apache.org/confluence/display/FINERACT/How-to+articles> for technical details to get started.

Roadmap
============

[Project Release Roadmap on JIRA (Detailed View)](https://issues.apache.org/jira/browse/FINERACT-268?jql=project%20%3D%20FINERACT "Project Release Roadmap on JIRA (Detailed View)")

Video Demonstration
============

Apache Fineract / Mifos X Demo (November 2016) - <https://www.youtube.com/watch?v=h61g9TptMBo>

More Information
============
More details of the project can be found at <https://cwiki.apache.org/confluence/display/FINERACT>.