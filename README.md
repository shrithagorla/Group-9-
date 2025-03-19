# Group 9 MIST 4610 Project 1

## Team Name: 
21482 Group 9

## **Team Members:**

1. Shritha Gorla [@shrithagorla](https://github.com/shrithagorla)
2. Ella Ransell [@edr82569](https://github.com/edr82569)
3. Logan Dwyer [@logandwyer](https://github.com/logandwyer)
4. Matthew Robertson [@matthewROB](https://github.com/matthewROB)

## **Problem Description:**

The task at hand is to model and build a relational database for the operations of a zoo. The central entity in the model is the Resident Animals entity, representing all animals currently housed at the zoo. These animals belong to specific species and are assigned enclosures in designated sections of the zoo.

The zoo operates in conjunction with veterinary services, food supply management, ticket sales, and employee administration to ensure smooth operations. The database aims to accurately model these relationships, generate sample data, and populate entities with relevant attributes. Additionally, this system will allow for querying data to gain business insights into zoo operations, including animal care, resource allocation, revenue from ticket sales, and event management.

## **Data Model:**

Our model is based on the structure of a zoo management system, where different entities represent key operations such as animal care, veterinary needs, food sourcing, ticketing, and employee assignments.

The Resident Animals entity represents animals housed in the zoo. Each animal belongs to a specific species and is assigned to an Enclosure that provides details on where the animal is housed. The Animal Species entity ensures each animal is classified correctly and specifies food types and veterinary needs unique to that species. The Vet Needs table stores medical procedures and associated costs. Since different species have different medical requirements, a many-to-many relationship is established between Animal Species and Vet Needs via an associative entity. The Vet Transactions entity tracks actual veterinary operations performed on individual animals, recording details such as procedure type, date, and cost. To ensure proper nutrition, the zoo database includes a Food Source entity, which manages suppliers and pricing. Different species require specific food types, so a many-to-many relationship exists between Food Types and Food Sources. Additionally, Food Transactions track food purchases to maintain inventory records.

Employee management is handled through the Zoo Employees entity, where each employee has a specific role within the zoo. Employees are responsible for overseeing animal care, veterinary needs, event organization, and administrative tasks. The zoo offers educational and recreational events, recorded in the Zoo Events table. Each event is associated with a specific animal, creating engagement opportunities for visitors. The Ticket Sales entity tracks revenue and visitor data, with different Ticket Types offering various pricing and access levels. The system maintains sale dates, the number of tickets sold, and pricing information.

![image](https://github.com/user-attachments/assets/1442fb69-40f7-4c35-bd48-1cfc410d536a)

## **Data Dictionary:**
[Final Data Dictionary.pdf](https://github.com/user-attachments/files/19330541/Final.Data.Dictionary.pdf)
![Animal Species-Enclosure](https://github.com/user-attachments/assets/e0356ee3-1e90-4476-9ab6-b05429194752)
![Food Source-Transaction-Type](https://github.com/user-attachments/assets/caf2f8fe-4631-4119-b7da-5e7714d263c6)
![Resident Animals-Section](https://github.com/user-attachments/assets/d97b2f3e-33c3-41b8-9f92-0e14c7305615)
![Ticket Sales-Types, Vet Needs](https://github.com/user-attachments/assets/991a2221-0685-4133-8a40-0f0f744a9481)
![Vet Transactions, Zoo Employees-Events](https://github.com/user-attachments/assets/bf4ecc05-6dd0-435b-a7b9-b8b99e11e080)


## **Queries:**
<img width="567" alt="Screenshot 2025-03-18 at 8 57 18 PM" src="https://github.com/user-attachments/assets/c53c3fff-fddf-4697-af3b-ee4788207863" />

1. #Finds total vet cost per species type and compares it to the overall average vet cost, with rounding.
![image](https://github.com/user-attachments/assets/dde59cc5-fae8-4226-82cd-198028736466)
Imagine you're managing a zoo and need to assess the veterinary expenses for each type of animal. This procedure calculates the total cost of veterinary procedures for every species type (e.g., reptiles, birds) and compares it to the overall average cost across all species. This helps identify which animal groups are the most expensive to care for medically.

2. #Counts animals per species type, filtering for mammals and birds with more than one animal.
   ![image](https://github.com/user-attachments/assets/f6f59780-7d4d-42ee-b2bd-a6da470e1666)
If you're focused on mammals and birds, this procedure helps count how many animals fall into these categories, but only if there are more than one of them. For instance, it might tell you that you have 10 lions and 3 eagles, ensuring that you’re aware of significant groupings in these species types.

3. #Calculates total revenue per ticket type based on price and amount sold.
![image](https://github.com/user-attachments/assets/ee0dea8b-6693-4994-a2c8-b7b2b959c3c7)
This is a way for zoos, parks, or any venue selling tickets to calculate total revenue by ticket type (e.g., adult, child, VIP). By multiplying the ticket price by the number of tickets sold and summing them, it provides a clear picture of which ticket types bring in the most money.

4. #Computes total food cost per species, food type, and source.
   ![image](https://github.com/user-attachments/assets/5f8eae22-f20f-4da7-ab30-d57b5641ceaf)
This is used for managing feeding expenses. For each species, it breaks down the total food cost by type (e.g., meat, fruits) and source (e.g., local suppliers, imported goods). This allows the zoo to identify the most expensive diets and optimize purchasing.

5. #Counts the total number of animals per zoo section.
![image](https://github.com/user-attachments/assets/c277bdbe-176a-45b4-bd03-6d3008bb4d19)
Zoos are typically divided into sections like "Rainforest," "Savannah," or "Arctic." This procedure tallies up the number of animals in each section, helping managers balance animal populations and plan exhibits.

6. #Counts employees per section
   ![image](https://github.com/user-attachments/assets/e3357e89-e17d-44eb-8cf7-a806c122d1ec)
Workforce management is key in a zoo. This counts how many employees are assigned to each section, ensuring enough staff are available to care for the animals and interact with visitors in every area

7. #Finding resident animals whose species name contains the word "Fox"
![image](https://github.com/user-attachments/assets/a80883ed-407c-4ce5-9168-0b2e1d49572e)
If your zoo has animals with species names like "Arctic Fox" or "Fennec Fox," this procedure pulls their details. It’s a useful query for quickly identifying animals of a particular family or genus within a database

8. #Find all employees who are not assigned to any events.
   ![image](https://github.com/user-attachments/assets/48c151b7-4d98-4c00-8e3e-07fcd14c028b)
Zoos often hold events like animal feedings or educational shows, requiring specific staff. This query identifies employees who aren’t currently assigned to events, helping managers allocate them where they’re needed.
 
9. #Find the employee assigned to the animal named 'Simba'
   ![image](https://github.com/user-attachments/assets/89406919-5768-4533-a49c-91b5f9291431)
Let’s say someone asks, “Who takes care of Simba?”—a lion at the zoo. This query pinpoints the employee responsible for Simba, streamlining communication and accountability

10. #Find animals that require a 'Dental Check'
![image](https://github.com/user-attachments/assets/e6389338-c37a-431e-b785-d4067b8a5a15)
Animal healthcare is crucial, and this query finds animals due for specific procedures, like dental checks. It's helpful for veterinary scheduling and ensuring every animal gets the care they need.

## **Database infromation:**

Name of the database: ns_Sp25_21482_Group9
