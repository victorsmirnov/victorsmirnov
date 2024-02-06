# Victor Smirnov
## Full Stack developer

## Overview

Victor has vast experience in the back-end (NodeJs and TypeScript, PHP and GoLang), front-end (React stack) development, and DevOps for the AWS Cloud. He worked in distributed multilingual teams as a software architect, developer and DevOps. In his work, Victor follows coding standards, writes tests for the code and, in general, likes the TDD approach. In addition, Victor is familiar with standard software development processes and knows how to write documentation.

Victor's primary focus for the last five years was developing and supporting services that automate the company's business processes. The services provided REST API for the front-end application (corporate admin or website) or communicated with external services (Amazon API, CDON API, Facebook API, etc.).

Victor developed several micro-services (GoLang and TypeScript) and one regular-size service (TypeScript) and maintained the monolith over-size application (PHP).

Every service generally included infrastructure definition (AWS Cloud Formation templates or AWS CDK application) and pipeline to build, test and deploy the service to a staging or production environment. The services ran as AWS Lambda functions or docker containers in AWS Elastic Container Service.

The applications communicate with other internal applications, AWS services, including S3 storage, DynamoDb database, Document DB database (alternative to MongoDb), Open Search (alternative to ElasticSearch), Cloud Front, SNS and SQS, and other external services, including payment and shipment solutions (Klarna, Adyen) and marketplaces (Facebook, Amazon, Google, CDON).

### GoLang Overview

The company experimented with GoLang as a platform for future lambda functions and back-end services development. While working on the project, Victor studied GoLang courses and developed several microservices.

The company decided not to use GoLang for future development mainly for the following reasons.

* It takes a lot of work for the company to hire qualified GoLang programmers.
* It's difficult for the team to program using GoLang.
* The company considered the risk of difficulties integrating the GoLang application with external services because of missing libraries.

The only significant service in production developed by Victor is the web application for converting images. It converts the original high-resolution image to the requested format, returns the resulting image and uploads it to the S3 bucket. The application runs behind the CloudFront distribution, which first checks the S3 bucket for the image and falls back to the service in case of a miss for the newly uploaded high-resolution photos.

Victor developed the service to replace the legacy lambda function written in JavaScript directly in the AWS console. The company decided to keep the service and skip migrating it to TypeScript despite the risk of having no developers to support the code.

### TypeScript Overview

Victor developed in TypeScript and supported two services to automatize company business processes. The services communicate with others by listening to AWS SNS topics, reading messages from AWS SQS queues and sending messages to AWS SNS topics.

The services do not share any common database, and communication happens asynchronously. The company decided to extract parts of the extensive monolith application as services to improve performance and fix defects.

Victor developed integration tests for both services. He developed tests for new functionality and regression tests for fixed defects (TDD approach).

The services have automated CI/CD pipelines and monitoring dashboards in AWS CloudWatch. The build script creates Swagger REST API documentation from the source code. The front-end team uses the documentation to integrate the website with the services.

### DevOps Overview

Victor started supporting company infrastructure in the AWS Cloud with all resources created manually in the AWS Console. In five years, Victor completed the following DevOps tasks.

Victor migrated all AWS resources to the CDK template. The same CDK template creates staging and production environments, allowing testing configuration changes on the staging.
Victor migrated all company websites from the EC2 instances to docker containers.
Victor developed CI/CD pipelines for the company applications.
Victor migrated the monolith application from PHP 5.5 to PHP 7.4.
Victor developed CDK scripts for several new projects, including WordPress with custom plugins and NodeJs REST API. He also helped to create a standard CDK template for the TypeScript REST API application running in the AWS Elastic Container Service.
Victor moved some AWS services to a different AWS account because of the business decision to spin off a non-primary business.

## Work Experience

### 2018-04 — 2023-12, RugVista (Malmö, Sweden)

Victor started with system administrator tasks configuring different servers located on-premise and Amazon AWS Cloud. For example, Victor configured the service to send cron job logs to the AWS CloudWatch, installed a new version of a library on the Amazon EC2 autoscaled instance, etc.

Then Victor switched to DevOp tasks in the AWS Cloud. For example, migrate infrastructure from the EC2 autoscaled instance to ECS containers, define AWS Pipelines to build and deploy different applications automatically, migrate the website and admin to other Amazon accounts, and define AWS infrastructure as CloudFormation templates and CDK application.

Victor supports the local development environment for the admin, the website and the new services. For example, he adds new services and configures integration between services in the local stack. Another example is Victor's configured support for HTTPS protocol in the development environment. As a result, we make development and production environments behave the same.

Victor developed services in GoLang — for example, CDON and BygHemma integration. The application went through development, deployment, integration with existing admin and CDON, support, bug fixing, and discontinuation.

It is worth noting that Victor also solved related DevOp tasks by defining necessary infrastructure as AWS CloudFormation templates and creating an automatic build and deployment pipeline.

Victor develops services in TypeScript, such as the warehouse and Back-end API services. Integrating the new services with the existing admin application was the most challenging task. The service also has the AWS infrastructure defined as AWS CloudFormation templates and CDK application, automatic deployment pipelines and CloudWatch dashboard for monitoring the services.

The TypeScript services have good unit and integration test coverage; Victor employs the TDD process when fixing service issues.

Victor fixes bugs and develops new features in the admin and website in PHP, such as migrating to PHP version 7.4 and moving application logs to AWS CloudWatch. Most of his work in the PHP code is related to integrating the new services and the infrastructure changes. For example, he migrated cron jobs to the AWS Batch. As part of this task, Victor did automatic job deployment. The admin deployment pipeline synchronises job definitions from the PHP code with the AWS Batch and updates the AWS CloudWatch schedule.

Victor is involved in architecture planning — for example, he suggests what programming languages and tools to use in development, how to integrate new services, and how to implement new functionality.

### 2017-11 — 2018-04, Lagafors (Stockholm, Sweden)

Victor developed server-side code and participated in developing client-side code for the online equipment monitoring application.

Victor developed Java REST API to manage and present application settings, Java server-side code to fetch data from the eWon devices and provide this data to the client SPA application, client-side code to manage SPA application state in Redux, client-server communication using Redux-Saga, bind ReactJS components with application data and actions using Keajs, React and Redux.

Victor used Java and Java Spring framework on the server side and JavaScript, ReactJS, Redux, Redux-Saga, Keajs and Reselect on the client side.

### 2017-04 — 2017-11, Cresto (Stockholm, Sweden)

Victor developed a plugin for Cresto WordPress and implemented some features: synchronising products between Microsoft Navision and WooCommerce using SOAP API to fetch data from Navision and WordPress/WooCommerce programming API to update the products; implementing custom checkout process in WooCommerce, orders registration in Navision, calculating freight cost for an order in Navision; implementing a list of shipment addresses taken from Navision; implementing custom user registration from invitations by Navision; implementing a custom product details page, mini shopping cart and user information pages.

Victor created an extended WordPress admin interface to manage Cresto products (extended properties) and categories, checking synchronisation results and errors.

Victor used PHP 7.2 to run WordPress with the WooCommerce plugin and Grunt to compile front-end JavaScript and CSS.

### 2017-03 — 2017-04, Greenely AB (Stockholm, Sweden)

Victor developed REST API to aggregate electricity usage data and provide different reports.

Victor used Java 8 Spring framework, including subprojects (Spring Boot, MVC, AMPQ, Data JPA), Apache Common Math library JPA and Hibernate.

### 2016-07 — 2017-02, Ascom (Skellefteå, Sweden) Ascom

Victor worked in a team and developed the front-end part of the application.

Victor worked with C#, JavaScript (ECMAScript 6), React, Redux Webpack, Babel and Bootstrap CSS.

### 2014-10 — 2017-10, and Mobiplus (Göteborg, Sweden).

Victor worked on extending an SMS marketing application to support email marketing. The team developed an email constructor based on drag-and-drop functionality and a valid HTML code generator.

We used PHP Yii 1, Vagrant, Puppet, Angular1.3, Coffee script, SASS and Grunt in the project.

### 2009-09 — 2014-04, SoftRose (Ekaterinburg, Russia)

Victor worked as a CTO for the SoftRose company and also owned it.

The company developed the job listings inventory application. We aimed to spider job boards and employer and recruiter sites, extract job listings, build the jobs database, and analyse job data.

We developed the website http://www.jobinventory.com/, a spider application to extract job listings, an API to search for jobs according to indexes, and an application to send new job listings to job seekers.

Data from 5 thousand sources was collected by the spider and processed four times per day.

Other characteristics:
* 5 million jobs in the index;
* 2 million email messages per day;
* 5 million subscribers;
* Millions of API requests per hour;
* Up to 12 servers in the Elasticsearch cluster;
* Web server's farm for API with automatic load balancing.

We used PHP 5, Zend Framework, Elasticsearch, Redis, Gearman, AWS Services (EC2, RDS, SES, ElastiCache, etc.)

### 2005-11 — 2009-05, MegaFon OJSC (Ekaterinburg, Russia)

Victor worked as a lead in the billing support team.

The team developed and maintained the application to monitor the mobile phone company's services and processes' stability and performance. For example, it checks whether the service handles USSD requests without errors and delays or whether the other service charges phone calls correctly and on time. The goal was to ensure the company provided customers with high-quality service.

We developed monitoring using Java and did a lot of Oracle PL/SQL programming.
