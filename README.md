# CLOUD-DATA-STORAGE-SERVER

## NAME: SANTHOSH R
## REG NO: 212224230249

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

<img width="1146" height="665" alt="Screenshot 2026-08-21 093724" src="https://github.com/user-attachments/assets/1bf05c7c-5f20-4d65-9524-181d7ff20a15" />
<img width="1143" height="662" alt="Screenshot 2026-08-21 093800" src="https://github.com/user-attachments/assets/f6b46acf-8663-4c8e-a554-91642dd8b0ec" />
<img width="2518" height="1214" alt="image" src="https://github.com/user-attachments/assets/4ca7d809-0f45-4329-8224-140a0c7a5c30" />
<img width="2522" height="1220" alt="image" src="https://github.com/user-attachments/assets/f09b6784-5b7d-466c-b0d0-53af1d20415f" />
<img width="2521" height="1221" alt="image" src="https://github.com/user-attachments/assets/5eeaa98a-d45a-4a38-82c5-ac104fa07371" />
<img width="2527" height="1297" alt="image" src="https://github.com/user-attachments/assets/ececfa6a-62a3-4a4a-b560-2de5a1c0e9f7" />

<img width="2559" height="1599" alt="image" src="https://github.com/user-attachments/assets/8931181b-09e1-4a5b-84df-41b898aaa65c" />
<img width="2559" height="1599" alt="image" src="https://github.com/user-attachments/assets/19739dd3-7e56-43b7-9748-4b0ca32ec16b" />

## Result

Thus, an Amazon RDS database instance was successfully created and configured as a cloud data storage server. The database was securely connected to a web application, and data operations such as inserting, updating, and deleting records were successfully performed through the application.

