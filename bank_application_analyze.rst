================
bank_application
================

Analyzing the problem
---------------------

  * The project task is to develop a simple system for a fictitious bank. The 
    bank has a number of customers and each customer can have one or more 
    different bank accounts.

Assessing the problem 
---------------------

  * The management of the application will take place via a terminal.
  * Input will consist of entered text.
  * The output will consist of text.
  * The data will be stored in .csv files.
  * The data must be validated.

Gathering information from about the problem
--------------------------------------------

Who's the 'origiantors' of the data for the application?

  * Bank officials.

Who's the 'users' of the application?

  * Bank officials.
    
Who's the 'consumers' of the data from the application?

  * Bank officials.

Who's the 'support staff' who are involved with the systems that will run or 
consume data from the application?

  * Mikael Zeylon.

Interviewing the interested parties
-----------------------------------

Originators:

  * Valuse accepted for character fields are a-z? 
  * Units represented by numeric fields are int or float?
    Numeric fields are truly number-only fields. 
  * Account number range 1001 - 9999.

Users:

  * Customer number and account number can be automatically populated.
    Automatic popularized values must not be overwritten.
    
Consumers:
 
  * The order of fields in the CSV matter. 
    Use header in CSV (no spaces, mixed case...).

Analyzing what we've foud out
-----------------------------

Begin by writing down the basic information about the workflow:

  * An application for a bank is to be built which will be used by bank 
    officials. The system must be run via terminal. The system must handle 
    input and output data. The input has certain limitations and must be 
    validated. Some data can be automatically popularized. The storage takes 
    place in .csv files. The application will be built by, Yours Truly!


Documenting specification requirements:
  
  * See separate deocument.
