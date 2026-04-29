Question 1

A schema-less database is a database that does not require a fixed structure before storing data. Unlike traditional SQL databases where you must define tables and columns first, MongoDB allows data to be stored in flexible formats such as JSON documents. This means each record can have different fields and does not need to follow a strict structure.

This feature is very useful during the early development of an IoT system because the sensor data may change frequently. For example, at first the sensor might only send temperature and humidity, but later it could include other data like pressure or battery level. With a schema-less database, there is no need to redesign the database every time the data changes. This makes development faster, more flexible, and easier to manage when experimenting with different sensor data.

Question 2

Using Node-RED as a middleware between the ESP32 and the MongoDB database is important for security and system design. The ESP32 does not communicate directly with the database but instead sends requests to Node-RED through HTTP endpoints. Node-RED then handles the database operations.

If the MongoDB port is exposed directly to the internet, it creates a serious security risk. Hackers could easily access the database, steal data, modify information, or delete everything. There would also be no proper control over who can access the database.

By using Node-RED, it acts as a protective layer. It can control and validate incoming requests, ensure only authorized users can access the system, and process the data before storing it. This also makes the system easier to maintain and update because changes can be handled in Node-RED without affecting the devices. Overall, this approach improves security, reliability, and scalability of the system.
