================
bank_application
================

Description
-----------

The goal is to create a simple and user-friendly application with the ability 
to manage customers, accounts and the bank's daily tasks.

Requirements
------------

This section is a list of specific things the program must be able to do in 
order to be minimally functional. It can include both functional and 
non-functional requirements.

Functional Requirements:

  * Bank:
    + PASS:
      - Print a list of the bank's customers (social security number, first and 
        last name)
      - Adding a new customer with a unique social security number (yyyymmdd).
      - Change a customer's name (social security number cannot be changed).
      - Remove an existing customer, existing accounts must also be terminated.

    + PASS WITH DISTINCTION:
      - Create account for an existing customer, a unique account number is 
        generated.
      - Accounts must also be able to be closed via the account number 
        attribute, balance is printed and the account is deleted.
      - View all transactions a customer has made with a specific account.

    + The Bank class must contain a list of all customers. The class should 
      contain a number of methods that manage customers and its accounts.

    + def _load():
      Loads the text file and populates the list that should contain the 
      customers.

    + def get_customers():
      Returns all the bank's customers (social security number and name)

    + def add_customer(name, pnr):
      Creates a new customer with name and social security number. The customer
      is created only if not is there a customer with the personal 
      identification number entered. Returns True if the customer was created 
      otherwise False is returned.

    + def get_customer(pnr):
      Returns information about the customer including their accounts. First 
      place in the list is reserved for the customer's name and social security
      number, then the information follows about the customer's accounts.

    + def change_customer_name(name, pnr)
      Renames customer, returns True if name was changed otherwise returns 
      False (if the customer did not exist).

    + def remove_customer(pnr)
      Deletes the customer with the social security number entered from the 
      bank, all of the customer's possible accounts is also removed and the 
      result is returned. The list returned should contain information in the 
      case of all accounts that were removed, the balance that the customer 
      receives back.

    + def add_account(pnr)
      Creates an account for the customer with the social security number 
      entered, returns the account number as the account created could 
      alternatively return -1 if no account was created.

    + def get_account(pnr, account_id)
      Returns Textual presentation of the account with account number belonging
      to it the customer (account number, balance, account type).

    + def deposit(pnr, account_id, amount)
      Make a deposit to the account, returns True if successful otherwise False.

    + def withdraw(pnr, account_id, amount)
      Make a withdrawal on the account, returns True if successful otherwise 
      False.

    + def close_account(pnr, account_id)
      Terminating an account. Textual presentation of the account's balance 
      shall be generated and is returned.

    + (VG) def get_all_transactions_by_pnr_acc_nr( pnr, acc_nr ):
      Returns all transactions a customer has made with a specific account or 
      -1 if the account does not exist.


  * Customer:
    + PASS:
      - See information about the selected customer including all accounts 
        (account number, balance, account type).
      - Deposit money into an account.
      - Withdraw money from the account (but only if the balance covers the 
        withdrawal amount).

      - The Customer class must handle the following information:
      - Id.
      - Customer's name.
      - Social security number.
      - All accounts of the customer.
      - (VG) Transactions.

      - For example, you must be able to change the customer's name and 
        retrieve information about the customer (social security number, first 
        and last name and download information about the customer's accounts 
        (account number, balance, account type)). Dessutom ska man kunna 
        hantera kundens konto(n). 

      - Implementera metoder som säkerställer ovanstående krav i klassen Bank 
        nedan. (Bank inkluderar förslag på metoder. Komplettera dessa med fler 
        metoder om det behövs).


  * Account:
    + PASS:
      - Balance.
      - Account type (<class ‘str’>).
      - Account number (there cannot be multiple accounts with the same account 
        number).

      - Start by implementing the Account class to handle the following 
        information:

      - You must be able to carry out transactions (deposit/withdrawal)
      - Retrieve account numbers, and present the account (show account number, 
        balance, account type).

      - Implement methods that ensure the above requirements in the Bank class.
        (Bank class design includes the methods to be used. Complete these with
        an implementation or more methods if needed.)


  * DataSource:
    + PASS WITH DISTINCTION:
      - DataSource (base class)
        The DataSource class must contain methods that manage where the data is
        comes from, e.g. Text file, Json file, Database, API. The DataSource 
        class requires concrete implementations. A requirement is that the 
        implementation must use a text file as data source.
      
      - def datasource_conn():
        This method implements the connection to a generic data source. Returns 
        a <class 'tuple'> with a <class 'bool'> and a <class 'str'> e.g., 
        (True, “Connection successful” [, datasource name])

      - def get_all():
        Returns all customers in the bank.
      
      - def update_by _id( id ):
        Updates a customer based on the id provided as a parameter. Returns 
        info about the customer that has been updated, or -1 if the customer 
        does not exist.

      - def find_by_id( id ):
        Returns a customer based on the id entered or -1 if the customer exists.

      - def remove_by_id( id ):
        Deletes a customer based on the id given as parameter. Returns info if 
        the customer removed or -1 if the customer does not exist.


  * Transaction
    + PASS WITH DISTINCTION:
      - The Transaction class will handle the following information:

      - Id
      - Customers Id
      - Account Id
      - Date
      - Amount

      - The amount attribute can have negative or positive numbers, e.g. if the
        customer has withdrawn SEK 2000 show amount the -2000 attribute. 
        Depositing SEK 300 gives the attribute a value of +300 or 300.
    
Non-functional Requirements:

  * Usesr-friendly terminal interface.
    
Functionality Not Required
--------------------------

The program does not need to:

  * This section is a list of things the program does not need to do; it exists
    to clarify the scope of the software and make sure nobody expects 
    unreasonable things from the application. We don't need to include every
    possible thing our application won't do; naturally, our program won't make 
    toast or or do the lundry. However, if there are features we are not 
    implementing that users might reasonably expect, this is a good place to 
    clarify what wont be done.


Limitations
-----------

The program must:

  * Thsi is a list of constraints under which the program must operate, both 
    technological and human.

Data Dictionary
---------------

  * This is a detailed list of the data fields in the application and their
    parameters. A data dictionary can get quite lengthy, and may be worthy of a
    document of its own. It will not only be useful during the development of 
    our application but will become a critical reference to the data produced 
    by the application as the application expands and the data gets utilized in
    other contexts.
 
+------------+--------+----+---------------+--------------------+
|Field       | Type   |Unit| Valid Values  |Description         |
+============+========+====+===============+====================+
|            |        |    |               |                    |
+------------+--------+----+---------------+--------------------+
