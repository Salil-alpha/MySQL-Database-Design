# MySQL-Database-Design

Section 1


Context:

Any ecommerce company especially the ones that are having bulk orders on a daily basis and have their business setup across any country or nation, it gets difficult for them to keep their data safe, secure, arranged, and free from any distortion or anomalies. The need for having a sacrosanct data management system emerges at this point and calls for building one. Now, when it comes to product creation, marketing, pricing strategies, manufacturing time, historical analysis, and forecasting, as well as overall consumer happiness, businesses that employ data warehouses have a distinct edge. One may configure the pipeline to either import data directly into the warehouse or acquire it from other sources, depending on the time and money one can devote to its development. For the former, we may consider both scheduled cron tasks and ad hoc data uploads. Keep in mind that developer involvement is needed for the latter, which would otherwise be automated. As for the second choice, one does not need to hire programmers to make these kinds of app-to-app and service-to-service connections since there are already tools available, like Hevo and Zapier, that do the heavy lifting for the company or firm. There's no question this is yet another part of the pipeline, but it might be well worth it if it frees the company and management from having to do the grunt work alone.


Need and Benefits of RDBMS or Data Warehouse:

The ability to store, analyse, and extract value from enormous volumes of data while maintaining access to previous data for documenting of prior patterns and choices is without a doubt the most important advantage of using this technology. Other advantages of possessing a data warehouse include the following list:

1.	Information in its entirety: thanks to data management, decision-makers have access to data from a single perspective that comes from a variety of sources, together with a broad range of attributes that can be used to do analysis on this data (Osborne, 2022).
2.	Queries that run quickly; data warehouses make it possible to get and analyse massive volumes of aggregated data quickly and without the intervention of developers.
3.	The quality of the data is ensured by the transformation of all of the data into a standardised format by the data warehousing systems (MUS, 2019). This ensures that the data is of the highest possible standard and accuracy at all times.
4.	Scalability: With cloud-based data storage, it is conceivable to acquire almost infinite data retention, flexibly scale it up or down, and utilise it from anywhere in the world. Additionally, this flexibility may be scaled up or down as needed (MUS, 2019).
5.	Cloud data warehouses make it simple to incorporate cutting-edge technology like machine learning and artificial intelligence into your operations (Osborne, 2022).


System Requirement for the Business Use-Case:

There should be sections for Customers, Orders, Restaurants, Items, Drivers, and their Vehicles in the database. The drivers' National Insurance (NI) numbers are kept on file for payroll purposes. The database should keep track of the Client ID, the First Name, the Last Name, the Email Address, and the Contact Information for each customer. The specifics of each driver's licence are recorded, including the driver's name, salary, email address, and manager, as well as the license's issue date, country of issuance, expiration date, and number. When a rider first starts working for the organisation, they are often given a motorcycle to use for the life of their contract. Motorbike specifics such as VIN, colour, purchase date, engine size, etc. are recorded. In most restaurants, numerous drivers work for only one restaurant, yet each Manager is responsible for at least one driver. There are three pieces of information collected for each restaurant: the restaurant's unique identifier, the restaurant's or hotel's name, and the restaurant's physical location. It is necessary to record the Order ID, Order date, and Products ordered in conjunction with each order. For each order, at least one product must be purchased by the consumer. A consumer may place orders from a single restaurant or from many eateries. Although a single driver may make many deliveries, each driver is responsible for just one order at a time.

The major goal of this project was to use Chen's or Crow Foot's instructions to organise a social data collection and save the information supplied in the sample data record so that it could be used in the stated business scenario. The plan took into account interests, as well as the needs and relationships of those interested. The next step was to use MySQL to create the database and write the necessary SQL queries to import the data. The code has components typical of commercial settings, such as imperatives, default values, and ON DELETE clauses. The last step included writing some SQL code to check that the data set in question followed all of the required business processes.


Section 2

Task One:

We have used Crow’s Foot Notation to design the schema for the use case. (Refer to the image attached)

Your first order of business in the relational database that you are using is to create the table that will serve as its foundation. Because of the specific nature of this situation, we are going to refer to this table as the "customers." It has to contain these columns: an ID number (an integer), a name (a text), an email address (also a text), and a phone number (also a text) (number).

Now create a second table that is in accordance with your ER design and name it the "items table." This should be broken out into three columns: ID reward, Name (text), and category (text). After that, we will develop some further tables, which will be referred to as "Orders," "Drivers," "Restaurants," "Vehicles," and "Manager." Each of these tables is constructed in order to save the specific data that is indicated by the table's name. For example, the data for orders are stored in the Orders database, whereas the Drivers table holds information about the individuals responsible for delivering the packages, and so on.

The creation of the appropriate associations between two tables based on the use case and the use of suitable foreign keys to define these relationships is one of the most important aspects of this procedure as a whole.


Task 2:

To verify that the database is capable of supporting the aforementioned business operations, one might use the SQL code that is provided below:

1.	At this step, the information about a new client is added to the system. This information, together with the commencement of the order and any other details about the drivers, restaurants, or cars, as well as any data that may be retrieved from the instance, are also included.
2.	The second step of the business process is to compile a list of all of the orders and determine the highest and lowest value orders with all of the granularities of the order and the restaurants from which the orders are placed. This is done to have an understanding of the top and bottom performing restaurants so that the decision-makers of the company can delist or promote a restaurant or take other possible actions based on the information they have gathered.
3.	The third step of the business process is to compile a list of all of the customers and the region that they place the majority of their orders from as well as the times of day when the majority of the customers are active as well as the top restaurants that they search for on a daily basis and ultimately place their orders from. On the basis of all of this information, the firm may choose to only run advertisements at the periods when the consumers are the most active in order for the advertisements to produce results in the shape of purchases and subscriptions.
4.	The fourth step of the company is to identify the top-performing managers and drivers so that consistent awards may be bestowed upon them based on the goals they have been successful in achieving.

