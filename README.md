# Group 9 MIST 4610 Project 1

Team Name:
21482 Group 9

Team Members:

1. Shritha Gorla @shrithagorla
2. Ella Ransell @edr82569
3. Logan Dwyer @logandwyer
4. Matthew Robertson @matthewR0B

Problem Description: 

The task at hand is to model and build a relational database for the operations of a zoo. The central entity in the model is the Resident Animals entity, representing all animals currently housed at the zoo. These animals belong to specific species and are assigned enclosures in designated sections of the zoo.

The zoo operates in conjunction with veterinary services, food supply management, ticket sales, and employee administration to ensure smooth operations. The database aims to accurately model these relationships, generate sample data, and populate entities with relevant attributes. Additionally, this system will allow for querying data to gain business insights into zoo operations, including animal care, resource allocation, revenue from ticket sales, and event management.

Data Model: 

Our model is based on the structure of a zoo management system, where different entities represent key operations such as animal care, veterinary needs, food sourcing, ticketing, and employee assignments.

The Resident Animals entity represents animals housed in the zoo. Each animal belongs to a specific species and is assigned to an Enclosure that provides details on where the animal is housed. The Animal Species entity ensures each animal is classified correctly and specifies food types and veterinary needs unique to that species. The Vet Needs table stores medical procedures and associated costs. Since different species have different medical requirements, a many-to-many relationship is established between Animal Species and Vet Needs via an associative entity. The Vet Transactions entity tracks actual veterinary operations performed on individual animals, recording details such as procedure type, date, and cost. To ensure proper nutrition, the zoo database includes a Food Source entity, which manages suppliers and pricing. Different species require specific food types, so a many-to-many relationship exists between Food Types and Food Sources. Additionally, Food Transactions track food purchases to maintain inventory records.

Employee management is handled through the Zoo Employees entity, where each employee has a specific role within the zoo. Employees are responsible for overseeing animal care, veterinary needs, event organization, and administrative tasks. The zoo offers educational and recreational events, recorded in the Zoo Events table. Each event is associated with a specific animal, creating engagement opportunities for visitors. The Ticket Sales entity tracks revenue and visitor data, with different Ticket Types offering various pricing and access levels. The system maintains sale dates, the number of tickets sold, and pricing information.

This database model ensures an efficient and well-organized zoo operation by integrating animal care, veterinary tracking, food inventory management, employee administration, and ticketing. By generating sample data and executing queries, zoo administrators can extract valuable insights to improve efficiency and ensure the well-being of the animals.

