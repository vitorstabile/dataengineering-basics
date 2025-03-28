<h1 align="center"> Data Engineering </h1>

# Content

1. [Chapter 1: Introduction to Data Engineering](#chapter1)
    - [Chapter 1 - Part 1: What is Data Engineering?](#chapter1part1)
      - [Chapter 1 - Part 1.1: Core Principles of Data Engineering](#chapter1part1.1)
      - [Chapter 1 - Part 1.2: Key Concepts in Data Engineering](#chapter1part1.2)
      - [Chapter 1 - Part 1.3: Practical Examples and Demonstrations](#chapter1part1.3)
    - [Chapter 1 - Part 2: Data Engineer Roles and Responsibilities](#chapter1part2)
      - [Chapter 1 - Part 2.1: Core Responsibilities of a Data Engineer](#chapter1part2.1)
      - [Chapter 1 - Part 2.2: Specific Roles Within Data Engineering](#chapter1part2.2)
      - [Chapter 1 - Part 2.3: Skills Required for Data Engineering Roles](#chapter1part2.3)
      - [Chapter 1 - Part 2.4: Real-World Application](#chapter1part2.4)
    - [Chapter 1 - Part 3: The Data Engineering Lifecycle](#chapter1part3)
      - [Chapter 1 - Part 3.1: The Data Engineering Lifecycle Stages](#chapter1part3.1)
      - [Chapter 1 - Part 3.2: Real-World Application](#chapter1part3.2)
    - [Chapter 1 - Part 4: Introduction to Data Architecture](#chapter1part4)
      - [Chapter 1 - Part 4.1: What is Data Architecture?](#chapter1part4.1)
      - [Chapter 1 - Part 4.2: Data Architecture Patterns](#chapter1part4.2)
      - [Chapter 1 - Part 4.3: Data Architecture vs. Data Modeling](#chapter1part4.3)
      - [Chapter 1 - Part 4.4: The Role of a Data Architect](#chapter1part4.4)
    - [Chapter 1 - Part 5: Data Engineering vs. Data Science vs. Data Analytics](#chapter1part5)
      - [Chapter 1 - Part 5.1: Defining Data Engineering](#chapter1part5.1)
      - [Chapter 1 - Part 5.2: Defining Data Science](#chapter1part5.2)
      - [Chapter 1 - Part 5.3: Defining Data Analytics](#chapter1part5.3)
      - [Chapter 1 - Part 5.4: Key Differences and Overlaps](#chapter1part5.4)
    - [Chapter 1 - Part 6: Setting up Your Data Engineering Environment (Cloud or Local)](#chapter1part6)
      - [Chapter 1 - Part 6.1: Cloud vs. Local Environments: A Detailed Comparison](#chapter1part6.1)
      - [Chapter 1 - Part 6.2: Setting Up a Local Data Engineering Environment](#chapter1part6.2)
      - [Chapter 1 - Part 6.3: Setting Up a Cloud Data Engineering Environment](#chapter1part6.3)
      - [Chapter 1 - Part 6.4: Practice Activities](#chapter1part6.4)
  
<div align="center"><img src="img/example-w1054-h609.png" width=1054 height=609><br><sub>Example - (<a href='https://github.com/vitorstabile'>Work by Vitor Garcia</a>) </sub></div>
  
## <a name="chapter1"></a>Chapter 1: Introduction to Data Engineering

### <a name="chapter1part1"></a>Chapter 1 - Part 1: What is Data Engineering?

Data engineering is the backbone of any data-driven organization. 
It encompasses the design, construction, and management of the infrastructure that allows us to collect, store, process, and analyze data at scale. Without robust data engineering practices, data science and data analytics efforts would be severely limited, as they rely on the availability of clean, reliable, and accessible data. 
This lesson will provide a comprehensive introduction to the field of data engineering, covering its core principles, key concepts, and essential skills.

#### <a name="chapter1part1.1"></a>Chapter 1 - Part 1.1: Core Principles of Data Engineering

Data engineering is guided by several core principles that ensure data systems are reliable, scalable, and maintainable. 
These principles are crucial for building effective data solutions that meet the evolving needs of an organization.

**Reliability**

Reliability refers to the ability of a data system to consistently perform its intended functions without failure. This includes ensuring data is accurate, complete, and available when needed.

- **Data Quality**: Maintaining high data quality is paramount. This involves implementing data validation checks, data cleansing processes, and data monitoring systems to identify and correct errors or inconsistencies. For example, a data pipeline that ingests customer data from various sources should include checks to ensure that email addresses are valid, phone numbers are correctly formatted, and duplicate records are identified and removed.

- **System Stability**: Data systems should be designed to withstand failures and unexpected events. This can be achieved through redundancy, fault tolerance, and robust error handling mechanisms. For instance, a data warehouse should be configured with backup and recovery procedures to ensure data can be restored in the event of a hardware failure or data corruption.

- **Monitoring and Alerting**: Continuous monitoring of data systems is essential for detecting and resolving issues promptly. This involves tracking key metrics such as data latency, data volume, and system performance, and setting up alerts to notify engineers when anomalies are detected. For example, an alert could be triggered if the data ingestion pipeline experiences a sudden drop in data volume, indicating a potential problem with the data source.

**Scalability**

Scalability refers to the ability of a data system to handle increasing amounts of data and user traffic without compromising performance. This is particularly important in today's data-rich environment, where data volumes are growing exponentially.

- **Horizontal Scaling**: Horizontal scaling involves adding more machines to a data system to distribute the workload. This approach is often preferred over vertical scaling (increasing the resources of a single machine) because it is more cost-effective and provides better fault tolerance. For example, a distributed database like Cassandra can be scaled horizontally by adding more nodes to the cluster, allowing it to handle larger amounts of data and higher query loads.

- **Elasticity**: Elasticity refers to the ability of a data system to automatically scale up or down based on demand. This is particularly useful for handling fluctuating workloads, such as those experienced during peak seasons or promotional periods. Cloud-based data platforms like AWS, Azure, and Google Cloud provide elasticity through auto-scaling features that automatically adjust resources based on real-time demand.

- **Performance Optimization**: Optimizing the performance of data systems is crucial for ensuring scalability. This involves techniques such as data partitioning, indexing, query optimization, and caching. For example, a data warehouse can be optimized by partitioning large tables based on date or region, creating indexes on frequently queried columns, and using caching mechanisms to store frequently accessed data in memory.

**Maintainability**

Maintainability refers to the ease with which a data system can be modified, updated, and repaired over time. This is essential for ensuring the long-term viability of a data solution.

- **Modularity**: Designing data systems with modular components makes it easier to modify or replace individual parts without affecting the entire system. This can be achieved through microservices architecture, where each component is a self-contained service with a well-defined API. For example, a data pipeline can be designed with separate modules for data ingestion, data transformation, and data loading, allowing each module to be updated independently.

- **Automation**: Automating repetitive tasks such as data backups, system monitoring, and deployment processes reduces the risk of human error and improves efficiency. This can be achieved through scripting, configuration management tools, and continuous integration/continuous deployment (CI/CD) pipelines. For example, a data engineer can automate the process of creating daily backups of a database using a cron job or a dedicated backup tool.

- **Documentation**: Comprehensive documentation is essential for understanding how a data system works and how to maintain it. This includes documenting the system architecture, data models, data pipelines, and configuration settings. For example, a data warehouse should have detailed documentation that describes the schema of each table, the data lineage of each field, and the purpose of each stored procedure.

#### <a name="chapter1part1.2"></a>Chapter 1 - Part 1.2: Key Concepts in Data Engineering

Data engineering involves a wide range of concepts and technologies. Understanding these concepts is essential for building effective data solutions.

**Data Ingestion**

Data ingestion is the process of collecting data from various sources and bringing it into a data system. This can involve extracting data from databases, APIs, log files, and other sources.

- **Batch Ingestion**: Batch ingestion involves collecting data in batches at regular intervals. This approach is suitable for data sources that are updated infrequently or that generate large volumes of data at once. For example, a data pipeline might ingest daily sales data from a relational database into a data warehouse.

- **Stream Ingestion**: Stream ingestion involves collecting data in real-time as it is generated. This approach is suitable for data sources that generate a continuous stream of data, such as sensor data, social media feeds, or website clickstreams. For example, a data pipeline might ingest real-time sensor data from IoT devices into a data lake for analysis.

- **Change Data Capture (CDC)**: CDC is a technique for capturing changes made to data in a database and propagating those changes to other systems. This is often used to keep a data warehouse or data lake synchronized with a source database. For example, a CDC system might capture changes made to a customer database and replicate those changes to a data warehouse in real-time.

**Data Transformation**

Data transformation is the process of cleaning, transforming, and enriching data to make it suitable for analysis. This can involve tasks such as data cleansing, data normalization, data aggregation, and data enrichment.

- **Data Cleansing**: Data cleansing involves identifying and correcting errors or inconsistencies in data. This can include tasks such as removing duplicate records, correcting spelling errors, and filling in missing values. For example, a data cleansing process might remove duplicate customer records from a database and correct any spelling errors in customer names.

- **Data Normalization**: Data normalization involves organizing data into a standard format. This can include tasks such as converting data types, standardizing units of measure, and encoding categorical variables. For example, a data normalization process might convert all dates to a standard format (e.g., YYYY-MM-DD) and standardize the units of measure for product weights (e.g., kilograms).

- **Data Aggregation**: Data aggregation involves summarizing data to create higher-level insights. This can include tasks such as calculating averages, sums, and counts. For example, a data aggregation process might calculate the average sales per customer, the total revenue per product category, and the number of customers who made a purchase in the last month.

- **Data Enrichment**: Data enrichment involves adding additional information to data to make it more useful. This can include tasks such as geocoding addresses, adding demographic data, and linking data to external sources. For example, a data enrichment process might geocode customer addresses to add location data and link customer data to demographic data from a third-party provider.

**Data Storage**

Data storage involves storing data in a way that is efficient, reliable, and accessible. This can involve using databases, data warehouses, data lakes, and other storage technologies.

- **Relational Databases**: Relational databases are a type of database that stores data in tables with rows and columns. They are well-suited for storing structured data and providing ACID (Atomicity, Consistency, Isolation, Durability) properties. Examples include MySQL, PostgreSQL, and Oracle.

- **NoSQL Databases**: NoSQL databases are a type of database that does not use the traditional relational model. They are well-suited for storing unstructured or semi-structured data and providing high scalability and performance. Examples include MongoDB, Cassandra, and Redis.

- **Data Warehouses**: Data warehouses are a type of database that is optimized for analytical queries. They typically store historical data from multiple sources and are used for business intelligence and reporting. Examples include Amazon Redshift, Google BigQuery, and Snowflake.

- **Data Lakes**: Data lakes are a type of storage repository that stores data in its raw, unprocessed form. They are well-suited for storing large volumes of data from various sources and are used for data exploration and machine learning. Examples include Amazon S3, Azure Data Lake Storage, and Google Cloud Storage.

**OBS**: CSV as a Storage Format: While CSV files might not offer the advanced features of a database (like indexing, querying, or complex data relationships), they still serve as a way to store data in a structured, tabular format. They are often used for:

- Simple data sets
- Data exchange between systems
- Archiving data
- Loading data into other systems

**Data Processing**

Data processing involves transforming and analyzing data to extract insights. This can involve using batch processing, stream processing, and other processing techniques.

- **Batch Processing**: Batch processing involves processing data in batches at regular intervals. This approach is suitable for processing large volumes of data that do not require real-time analysis. For example, a batch processing job might calculate daily sales reports from a data warehouse.

- **Stream Processing**:Stream processing involves processing data in real-time as it is generated. This approach is suitable for processing data that requires immediate analysis, such as fraud detection or real-time monitoring. For example, a stream processing application might analyze real-time website clickstreams to detect fraudulent activity. Kafka is primarily designed for real-time data streams and message passing. Applications can subscribe to topics and consume messages as they arrive.

- **MapReduce**: MapReduce is a programming model for processing large datasets in parallel. It involves dividing the data into smaller chunks, processing each chunk independently, and then combining the results. Hadoop is a popular open-source implementation of MapReduce.

- **Spark**: Spark is a fast and general-purpose cluster computing system for big data processing. It provides a unified platform for batch processing, stream processing, machine learning, and graph processing.

#### <a name="chapter1part1.3"></a>Chapter 1 - Part 1.3: Practical Examples and Demonstrations

To illustrate the concepts discussed above, let's consider a hypothetical scenario involving an e-commerce company called "ShopSphere". ShopSphere collects data from various sources, including website clickstreams, sales transactions, customer profiles, and marketing campaigns.

**Data Ingestion Example**

ShopSphere uses a combination of batch and stream ingestion to collect data from its various sources.

- **Batch Ingestion**: Daily sales transactions from a relational database are ingested into a data warehouse using a batch process. This process extracts the data from the database, transforms it into a suitable format, and loads it into the data warehouse.

- **Stream Ingestion**: Website clickstreams are ingested into a data lake in real-time using a stream processing platform like Apache Kafka. This allows ShopSphere to analyze user behavior and personalize the website experience in real-time.

**Data Transformation Example**

ShopSphere performs various data transformation tasks to prepare the data for analysis.

- **Data Cleansing**: Customer data is cleansed to remove duplicate records and correct any spelling errors in customer names and addresses.

- **Data Normalization**: Product prices are normalized to a standard currency (e.g., USD) and product weights are normalized to a standard unit of measure (e.g., kilograms).

- **Data Aggregation**: Daily sales data is aggregated to calculate total revenue per product category and average sales per customer.

- **Data Enrichment**: Customer addresses are geocoded to add location data, which is then used to analyze sales trends by region.

**Data Storage Example**

ShopSphere uses a combination of data warehouses and data lakes to store its data.

- **Data Warehouse**: A data warehouse is used to store historical sales data, customer data, and marketing campaign data. This data is used for business intelligence and reporting.

- **Data Lake**: A data lake is used to store raw website clickstream data, log files, and sensor data. This data is used for data exploration and machine learning.

**Data Processing Example**

ShopSphere uses a combination of batch processing and stream processing to analyze its data.

- **Batch Processing**: Daily sales reports are generated from the data warehouse using a batch processing job. These reports provide insights into sales trends, customer behavior, and marketing campaign performance.

- **Stream Processing**: Real-time website clickstreams are analyzed using a stream processing application to detect fraudulent activity and personalize the website experience.

### <a name="chapter1part1"></a>Chapter 1 - Part 2: Data Engineer Roles and Responsibilities

Data engineers are the architects and builders of data infrastructure. They design, build, and maintain the systems that collect, store, process, and analyze data. This lesson will explore the diverse roles and responsibilities of a data engineer, providing a comprehensive understanding of what this critical function entails in modern organizations. Understanding these roles and responsibilities is crucial for anyone aspiring to become a data engineer or for those who want to collaborate effectively with data engineering teams.

#### <a name="chapter1part2.1"></a>Chapter 1 - Part 2.1: Core Responsibilities of a Data Engineer

The responsibilities of a data engineer can vary depending on the size and structure of the organization, the industry, and the specific projects they are working on. However, some core responsibilities are common across most data engineering roles.

**Data Pipeline Development and Maintenance**

Data engineers are primarily responsible for building and maintaining data pipelines. These pipelines are automated systems that move data from various sources to destinations where it can be analyzed and used for decision-making.

- **Extraction**: This involves retrieving data from diverse sources, such as databases, APIs, web logs, and sensors.

- **Transformation**: This step cleans, transforms, and prepares the data for analysis. It may involve data cleansing, data type conversions, data aggregation, and data enrichment.

- **Loading**: This involves loading the transformed data into data warehouses, data lakes, or other storage systems.

**Example**: Imagine a marketing company that collects data from various sources, including website traffic, social media platforms, and email marketing campaigns. A data engineer would build a pipeline to extract data from these sources, transform it into a consistent format, and load it into a data warehouse for analysis.

**Advanced Example**: Consider a financial institution that needs to process real-time stock market data. A data engineer would design a streaming data pipeline using technologies like Apache Kafka and Apache Flink to ingest, process, and store the data with minimal latency.

**Data Storage and Management**

Data engineers are responsible for designing, implementing, and managing data storage systems. This includes selecting the appropriate storage technologies, optimizing performance, ensuring data security, and managing data retention policies.

- **Database Management**: Managing relational databases (e.g., PostgreSQL, MySQL) and NoSQL databases (e.g., MongoDB, Cassandra).

- **Data Warehouse Design**: Designing and implementing data warehouses using technologies like Snowflake, Amazon Redshift, or Google BigQuery.

- **Data Lake Implementation**: Building and managing data lakes using technologies like Apache Hadoop, Apache Spark, and cloud storage services (e.g., Amazon S3, Azure Data Lake Storage).

**Example**: A retail company might use a data warehouse to store sales data, customer data, and product data. A data engineer would be responsible for designing the data warehouse schema, optimizing query performance, and ensuring data quality.

**Advanced Example**: An IoT company that collects data from thousands of sensors might use a data lake to store the raw data. A data engineer would be responsible for designing the data lake architecture, implementing data governance policies, and ensuring data security.

**Data Quality and Governance**

Data engineers play a crucial role in ensuring data quality and implementing data governance policies. This includes:

- **Data Validation**: Implementing data validation rules to ensure data accuracy and consistency.

- **Data Monitoring**: Monitoring data pipelines and storage systems to identify and resolve data quality issues.

- **Data Lineage**: Tracking the origin and flow of data to understand how it is transformed and used.

- **Data Security**: Implementing security measures to protect data from unauthorized access.

**Example**: A healthcare organization needs to ensure the accuracy and completeness of patient data. A data engineer would implement data validation rules to check for missing or invalid data and monitor data pipelines to identify and resolve data quality issues.

**Advanced Example**: A large enterprise might implement a data governance framework to ensure that data is used ethically and responsibly. A data engineer would be responsible for implementing data lineage tracking, data access controls, and data masking techniques to comply with data governance policies.

**Infrastructure Management**

Data engineers are often responsible for managing the infrastructure that supports data pipelines and storage systems. This includes:

- **Cloud Infrastructure**: Managing cloud resources using platforms like AWS, Azure, or Google Cloud.

- **Automation**: Automating infrastructure provisioning, deployment, and monitoring using tools like Terraform, Ansible, or Kubernetes.

- **Performance Tuning**: Optimizing the performance of data pipelines and storage systems.

**Example**: A startup might use AWS to host its data infrastructure. A data engineer would be responsible for provisioning EC2 instances, configuring S3 buckets, and setting up monitoring alerts.

**Advanced Example**: A large enterprise might use Kubernetes to orchestrate its data pipelines. A data engineer would be responsible for defining Kubernetes deployments, managing resource allocation, and ensuring high availability.

#### <a name="chapter1part2.2"></a>Chapter 1 - Part 2.2: Specific Roles Within Data Engineering

Within the field of data engineering, there are several specialized roles that focus on specific aspects of the data lifecycle.

**ETL Developer**

ETL (Extract, Transform, Load) developers specialize in building and maintaining data pipelines that extract data from various sources, transform it into a usable format, and load it into a data warehouse or data lake. They are proficient in using ETL tools and programming languages like Python or Java.

**Example**: An ETL developer might be responsible for building a pipeline that extracts sales data from a CRM system, transforms it to conform to a specific data model, and loads it into a data warehouse for reporting and analysis.

**Data Warehouse Engineer**

Data warehouse engineers focus on designing, building, and maintaining data warehouses. They are experts in data modeling, schema design, and query optimization. They work with technologies like Snowflake, Amazon Redshift, and Google BigQuery.

**Example**: A data warehouse engineer might be responsible for designing a star schema for a data warehouse that stores sales data, customer data, and product data. They would also be responsible for optimizing query performance and ensuring data quality.

**Data Lake Engineer**

Data lake engineers specialize in building and managing data lakes. They are proficient in working with large volumes of unstructured and semi-structured data. They use technologies like Apache Hadoop, Apache Spark, and cloud storage services.

**Example**: A data lake engineer might be responsible for designing a data lake architecture that can store data from various sources, including web logs, social media feeds, and sensor data. They would also be responsible for implementing data governance policies and ensuring data security.

**Data Infrastructure Engineer**

Data infrastructure engineers focus on building and managing the infrastructure that supports data pipelines and storage systems. They are experts in cloud computing, automation, and performance tuning.

**Example**: A data infrastructure engineer might be responsible for provisioning cloud resources, automating infrastructure deployment, and optimizing the performance of data pipelines.

#### <a name="chapter1part2.3"></a>Chapter 1 - Part 2.3: Skills Required for Data Engineering Roles

To be successful in a data engineering role, you need a combination of technical skills, analytical skills, and soft skills.

**Technical Skills**

- **Programming Languages**: Python, Java, Scala
- **Databases**: SQL, NoSQL
- **Data Warehousing**: Snowflake, Amazon Redshift, Google BigQuery
- **Data Lakes**: Apache Hadoop, Apache Spark, Amazon S3, Azure Data Lake Storage
- **ETL Tools**: Apache Airflow, Apache NiFi, Informatica PowerCenter
- **Cloud Computing**: AWS, Azure, Google Cloud
- **Operating Systems**: Linux, Windows
- **Version Control**: Git

**Analytical Skills**

- **Data Modeling**: Designing data models that meet the needs of the business.
- **Problem Solving**: Identifying and resolving data quality issues and performance bottlenecks.
- **Critical Thinking**: Evaluating different data engineering solutions and choosing the best option.

**Soft Skills**

- **Communication**: Communicating technical concepts to non-technical audiences.
- **Collaboration**: Working effectively with other data engineers, data scientists, and business stakeholders.
- **Teamwork**: Contributing to a positive and productive team environment.

#### <a name="chapter1part2.4"></a>Chapter 1 - Part 2.4: Real-World Application

Consider a large e-commerce company like Amazon. Data engineers at Amazon play a crucial role in building and maintaining the data infrastructure that supports its vast operations.

- **Recommendation Systems**: Data engineers build pipelines to collect and process data on customer behavior, product information, and purchase history. This data is used to train machine learning models that power Amazon's recommendation systems.

- **Supply Chain Optimization**: Data engineers build pipelines to collect and process data on inventory levels, shipping times, and demand forecasts. This data is used to optimize Amazon's supply chain and ensure that products are delivered to customers on time.

- **Fraud Detection**: Data engineers build pipelines to collect and process data on transactions, user activity, and device information. This data is used to detect and prevent fraudulent activity.

In each of these scenarios, data engineers are responsible for ensuring that data is accurate, reliable, and accessible to the teams that need it. They work closely with data scientists, machine learning engineers, and business stakeholders to build data-driven solutions that improve Amazon's operations and customer experience.

### <a name="chapter1part1"></a>Chapter 1 - Part 3: The Data Engineering Lifecycle

#### <a name="chapter1part3.1"></a>Chapter 1 - Part 3.1: The Data Engineering Lifecycle Stages

**1. Planning**

**2. Data Acquisition**

**3. Data Storage**

**4. Data Processing**

**5. Data Analysis**

**6. Deployment and Monitoring**

#### <a name="chapter1part3.2"></a>Chapter 1 - Part 3.2: Real-World Application

### <a name="chapter1part1"></a>Chapter 1 - Part 4: Introduction to Data Architecture

#### <a name="chapter1part4.1"></a>Chapter 1 - Part 4.1: What is Data Architecture?

**Key Principles of Data Architecture**

**Components of a Data Architecture**

#### <a name="chapter1part4.2"></a>Chapter 1 - Part 4.2: Data Architecture Patterns

**Data Warehouse Architecture**

**Data Lake Architecture**

**Lambda Architecture**

**Kappa Architecture**

#### <a name="chapter1part4.3"></a>Chapter 1 - Part 4.3: Data Architecture vs. Data Modeling

#### <a name="chapter1part4.4"></a>Chapter 1 - Part 4.4: The Role of a Data Architect

### <a name="chapter1part1"></a>Chapter 1 - Part 5: Data Engineering vs. Data Science vs. Data Analytics

#### <a name="chapter1part5.1"></a>Chapter 1 - Part 5.1: Defining Data Engineering

**Key Responsibilities of a Data Engineer**

**Tools and Technologies Used by Data Engineers**

**Example Scenario: Building a Data Pipeline for an E-commerce Company**

**Example Scenario: Managing a Data Lake for a Media Streaming Service**

#### <a name="chapter1part5.2"></a>Chapter 1 - Part 5.2: Defining Data Science

**Key Responsibilities of a Data Scientist**

**Tools and Technologies Used by Data Scientists**

**Example Scenario: Building a Recommendation System for an Online Retailer**

**Example Scenario: Predicting Customer Churn for a Subscription Service**

#### <a name="chapter1part5.3"></a>Chapter 1 - Part 5.3: Defining Data Analytics

**Key Responsibilities of a Data Analyst**

**Tools and Technologies Used by Data Analysts**

**Example Scenario: Analyzing Sales Data to Identify Top-Performing Products**

**Example Scenario: Analyzing Website Traffic to Improve User Engagement**

#### <a name="chapter1part5.4"></a>Chapter 1 - Part 5.4: Key Differences and Overlaps

**Overlaps**

**Collaboration**

### <a name="chapter1part1"></a>Chapter 1 - Part 6: Setting up Your Data Engineering Environment (Cloud or Local)

#### <a name="chapter1part6.1"></a>Chapter 1 - Part 6.1: Cloud vs. Local Environments: A Detailed Comparison

**Cloud Environments**

**Advantages:**

**Disadvantages:**

**Local Environments**

**Advantages:**

**Disadvantages:**

**Choosing the Right Environment**

#### <a name="chapter1part6.2"></a>Chapter 1 - Part 6.2: Setting Up a Local Data Engineering Environment

**Example: Setting up PostgreSQL Locally**

**Example: Using Python to Connect to PostgreSQL**

#### <a name="chapter1part6.3"></a>Chapter 1 - Part 6.3: Setting Up a Cloud Data Engineering Environment

**Example: Setting up an AWS EC2 Instance**

**Example: Setting up an AWS RDS PostgreSQL Instance**

#### <a name="chapter1part6.4"></a>Chapter 1 - Part 6.4: Practice Activities
