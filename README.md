# Rental-Management-System

PROBLEM STATEMENT:
In this fast-paced world, with so many ways to generate data, it is very essential the data being generated is collected and managed in a structured manner so that it can be converted into useful information. Storing such an enormous amount of data is a cause of concern for many stakeholders. Such problems are faced even by real estate firms where they have multiple customers looking for rental housing. Thus, it requires a robust database management system that facilitates connecting the customers with the appropriate property that suits their needs. The firms have multiple customers approaching to search for a rental property and storing their data and analyzing it accurately can help them gain revenues. This can only be possible if they have an organized process where the data is stored appropriately. The aim of our system is to design such a model that can help the organization to manage all the customers who are on lease or searching for a property along with keeping the track of organization’s profit and has a hassle-free experience.

PROPOSED SOLUTION:
• Using MIN_AMOUNT and MAX_AMOUNT, availability of the apartment can be
shown to customers as per their budget preferences.
• To know about utilities included in rent for each apartment, we are using association entity APARTMENT_UTILITY having PRIMARY KEY (APARTMENT_ID, UTILITY_ID) which connects APARTMENT and UTILITY entity
• For each apartment in APARTMENT entity, there is a LEASE_ID associated through which we can find the current tenants from the CUSTOMER entity using FOREIGN KEY(LEASE_ID). This can further help to track the payments using FOREIGN KEY (LEASE_ID) in PAYMENT entity
• Each landlord can view the current tenants living in associated apartments by creating VIEWS using APARTMENT-> LEASE_DETAILS-> CUSTOMER relationship
• Tracking the maintenance required for each apartment we are using FOREIGN KEY APARTMENT_ID in MAINTENANCE_REQUESTS entity

BUSINESS RULES:
1. Employee can check the availability of one or more rooms according to customer preferences
2. Each landlord can check the number of apartments he/she is leasing
3.  Each landlord can check the details of one or more tenants associated with one or more
apartments
4. Each landlord can keep a track on one or more apartment’s rent under him/her
5.  Employee can track history of lease details for every apartment for each year using
Lease_Details entity
6. Employee can keep a check on whether the payment for a particular month for an
apartment is done or not with the help of Payment entity based on the transaction date
7. Employee can manage multiple apartments
8. Once the apartment has been rented, the customer is assigned lease_id
9. Customer can keep a track on their payment dues
10. Each payment can belong to one or more tenants but only one lease_id
11. One booking can only be processed by one payment_id
12. Each customer can choose the apartment according to their preferences based on locality
and budget
13. Each apartment can have multiple utilities which may or may not be included in rent
14. Employee can view and manage maintenance requests
15. Once the lease date is assigned to a customer, the status of the apartment is changed
accordingly
16. According to maintenance request closed date, maintenance status can be tracked

SECURITY CONSTRAINTS: (USER LEVEL/PERMISSIONS) ADMIN:
1. Has full access i.e., READ/WRITE/UPDATE all the entities in the database
MANAGER:
1. Has read access for all the entities in the database.
2. Has UPDATE access to customer, lease, payment, and maintenance requests.
