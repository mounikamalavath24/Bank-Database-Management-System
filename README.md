Designing a relational database for an online banking system is an important and interesting task that requires careful planning and consideration. The database serves as the backbone of the banking system that stores and organizes large amounts of financial data securely.

The database for the Online Banking System must efficiently manage Account Details, Customer Details, and Transactions. Users should be able to log in to the system and perform banking operations like balance check, deposit, withdraw and money transfer. 

Let’s understand the overview of the Online Banking System through the below terms.


**User Management:**

We should manage user accounts which include registration, login and authentication.
Store user details such as name, email, address, and contact information securely.

**Account Management:**

Maintain records of bank accounts associated with each user.
Track account balances, transaction history, and account status (active, closed, etc.).

**Transaction Processing:**

Handle various types of transactions, including deposits, withdrawals, transfers, and bill payments.
Ensure transactions are secure, accurate, and recorded in real time.

**Security Features:**

Implement robust security measures to protect sensitive data and prevent unauthorized access.
Use encryption techniques to secure data transmission over the network.

**Reporting and Analytics:**

Generate reports on account activity, transaction history, and user behavior.
Use analytics to identify trends, detect fraud, and improve service offerings.

**Customer Support:**

Provide customer support features, such as chat support, FAQs, and helpdesk services.
Maintain records of customer interactions and feedback for improving services.

**Online Banking System Features**

User Login:The user login feature is a important component of online banking systems by providing a secure gateway for users to access their accounts. Users must authenticate themselves with a valid user ID and password and sometimes additional security measures like OTP or biometric authentication are used for added security.
Check Balance: After logging in the users can check the available balance in their bank accounts. This feature provides users with real-time information about their finances and helping them to manage their funds more effectively.
Send Money: Online banking systems allow users to transfer money from their account to another valid account. Users need to provide the recipients account number and other necessary details to complete the transaction securely.
Add Beneficiary: To make fund transfers easier and faster users can add beneficiaries to their account. Adding a beneficiary requires providing the recipient’s account details and verifying the relationship, ensuring that the transfer is authorized.

Receive Money: When a user receives money into their account, the transaction is recorded and the account balance is updated accordingly. This feature allows users to receive funds from other users or external sources.
Transaction History: Users can view their transaction history, which includes details such as the amount, time and type of transaction like deposit, withdrawal, fund transfer. This feature helps users keep track of their financial activities and monitor their spending patterns.

**Entities and Attributes of Online Banking System**

**1. Customer**

CustomerID (primary key): Unique identifier for each customer
Name: Name of the customer.
Address: Address of the customer.
Contact: Contact details of the customer (e.g.: Phone number).
Username (Unique) : username to login to the banking system.
Password: Encrypted password of the user.

**2. Account**

AccountID (primary key): Unique identifier of account.
CustomerID (foreign key referencing Customer): Identifier of the customer who owns the account.
Type: Defines the account type whether savings, current etc.
Balance: Amount of money available in the account.

**3. Transaction**

TransactionID (primary key): Unique identifier of the transaction, automatically increments.
AccountID (foreign key referencing Account): Identifies the account where the transaction took place.
Type: Defines the transaction type i.e. deposit or withdrawal.
Amount: Shows the balance amount used for the transaction.
Timestamp: The date and time of the transaction.

**4. Beneficiary**

BeneficiaryID (primary key): Unique identifier of the beneficiary.
CustomerID( foreign key referencing Customer): Identifies the customer who added the beneficiary.
Name: Name of the beneficiary.
AccountNumber: Account Number of the beneficiary.
BankDetails: Bank Name of the Beneficiary added.
Relationships Between These Entities
Customer – Account relationship
One to Many Relationship: One customer is allowed to create many accounts.
Foreign Key: CustomerID in Account Table is referencing CustomerID in Customer Table.
Customer – Beneficiary Relationship
One to Many Relationship: A customer can add multiple beneficiaries.
Foreign Key: CustomerID in Beneficiary is referencing to CustomerID in Customer Table.
Account – Transaction Relationship
Many to Many Relationship: An account can have multiple transactions and a transaction can involve multiple account numbers.
Foreign Key: AccountID in Transaction is referencing to AccountID in Account Table.

