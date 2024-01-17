# Notes and stuff from Cloud-Native-Spring-In-Action

Flyway doesn’t support R2DBC yet, so we need to provide a 
JDBC driver to communicate with the database. The Flyway 
migration tasks are only run at application startup and in 
a single thread, so using a nonreactive communication approach 
for this one case doesn’t impact the overall application’s 
scalability and efficiency.
That's why JDBC dependency is implemented to configure the
db through flyway.