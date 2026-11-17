# CLOUD-DATA-STORAGE-SERVER
# CLOUD-DATA-STORAGE-SERVER

### NAME: Himadri S
### REG NO: 212225040128

## Aim

To create and configure an Amazon Relational Database Service (Amazon RDS) instance as a cloud data storage server, configure the required security settings, connect it to a web application, and perform database operations using the application.

## Algorithm / Steps

1. Create a Security Group for the RDS database.
2. Add an inbound rule to allow MySQL (Port 3306) access from the Web Security Group.
3. Create a DB Subnet Group using two Availability Zones.
4. Launch an Amazon RDS MySQL database instance.
5. Configure the database with the required identifier, username, password, storage, and instance class.
6. Associate the database with the created Security Group and Subnet Group.
7. Wait until the database status becomes **Available**.
8. Copy the RDS endpoint.
9. Open the web application using the provided Web Server IP address.
10. Enter the RDS endpoint, database name, username, and password.
11. Connect the application to the database.
12. Verify the connection by adding, editing, and deleting records in the Address Book application.


## Program

### Security Group Configuration

* Security Group Name: **DB Security Group**
* Inbound Rule: **MySQL/Aurora (3306)**
* Source: **Web Security Group**

### DB Subnet Group

* Name: **DB-Subnet-Group**
* VPC: **Lab VPC**

### Amazon RDS Configuration

* Engine: **MySQL**
* Template: **Dev/Test**
* Availability: **Multi-AZ**
* DB Instance Identifier: **lab-db**
* Username: **main**
* Password: **lab-password**
* Instance Class: **db.t3.micro**
* Storage: **20 GB (General Purpose SSD)**

### Connect the Application

```text
Endpoint : <RDS Endpoint>
Database : lab
Username : main
Password : lab-password
```

After submitting the above details, perform Add, Edit, and Delete operations on the Address Book application.

## Output
<img width="1906" height="977" alt="Screenshot 2026-11-17 160432" src="https://github.com/user-attachments/assets/97590eff-ba84-4651-8de5-9757ff19fe97" />

<img width="1917" height="1010" alt="Screenshot 2026-11-17 160946" src="https://github.com/user-attachments/assets/5987ea69-e29d-4a3c-a3ca-a3f614a07cbe" />
<img width="1917" height="1041" alt="Screenshot 2026-11-17 161809" src="https://github.com/user-attachments/assets/2226a646-e369-4716-8f60-5c7215e95dc7" />
<img width="1916" height="1031" alt="Screenshot 2026-11-17 164003" src="https://github.com/user-attachments/assets/6058c363-411d-4a40-9bb5-76a04a34e278" />
<img width="1917" height="1027" alt="Screenshot 2026-11-17 164341" src="https://github.com/user-attachments/assets/74ef05b1-c932-41b9-b5c3-b62c426dfa2c" />
<img width="1917" height="1028" alt="Screenshot 2026-11-17 165900" src="https://github.com/user-attachments/assets/22de7c9d-c37d-47b6-b4f7-e04d903a3ccc" />

<img width="1903" height="1027" alt="Screenshot 2026-11-17 170021" src="https://github.com/user-attachments/assets/c14e467f-e751-452a-b4db-8b9671982a81" />

## Result

Thus, an Amazon RDS database instance was successfully created and configured as a cloud data storage server. The database was securely connected to a web application, and data operations such as inserting, updating, and deleting records were successfully performed through the application.



