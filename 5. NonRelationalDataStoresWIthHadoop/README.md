## Why NoSQL ?

Random Access to Planet-Size Data

Scaling up MySQL etc. massive loads requires extreme measures:
- Denormalization
- Caching layers
- Master/slave setups
- Sharding
- Materialized views
- Removing stored procedures

Do you really need SQL?
- your high-transaction queries are probably preety simple once de-normalized.
- A simple get/put API may meet your needs.
- Looking up values for a given key is simple, fast, and scalable.
- You can do both.....

Sample Architecture:

![Sample Architecture](https://github.com/Kavita-Yadav/Learning-Hadoop-and-bigData/blob/master/Images/Sample_architecture.png)
                           
Use the right tool for the job:

- For analytic queries, Hive, Pig, Spark, etc. work great.
- Exporting data to MySQL is plenty fast for most applications too.
- But if you work at giant scale- export your data a non-relational database for fast and scalable serving of that data to
  web applications, etc.
  
Sample application architecture:

![Sample Application Architecture](https://github.com/Kavita-Yadav/Learning-Hadoop-and-bigData/blob/master/Images/SampleAppArchitecture.png)
                           
#### Choosing your Database:
- When you don't even need some external database. Following factor can help to make decision for this case:
- Integration considerations.
- Scaling requirements.
- Support considerations.
- Budget considerations.
- CAP(Consitency, Availability, Partition-Tolerance) consideration. 
- Simplicity.
- Example: 
           building an internal phone directory app
              - Scale: limited
              - Consistency: Eventual is fine
              - Availability requirements: not mission critical
              - MySQL is probably already installed on your web server...
  
