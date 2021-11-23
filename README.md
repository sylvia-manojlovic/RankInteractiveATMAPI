# RankInteractiveATMAPI
The ATM API project for the Rank Interactive Assessment

Notes on the Datasource: The API was written and tested using SqlServer, 
connecting with Server=(localdb)\mssqllocaldb;Database=ATM_API;Trusted_Connection=True; 
For submission, and testing without requiring a physical database, an in-memory database is being used. 
This can easily be switched by changing the line 48/49 in the Startup.cs file 
Use this line (as is) for testing without a physical db: options.UseInMemoryDatabase(databaseName: "ATMAPI"); 
Or, if necessary, uncomment the above, and use this line, changing the connection settings as necessary 
options.UseSqlServer(@"Server=(localdb)\mssqllocaldb;Database=ATM_API;Trusted_Connection=True;");

TO TEST: 1st start up the API by executing ATM.API.exe from the folder ATMWebAPI\MSUnitTest\TestWebAPI\TestWebAPI\bin\Debug\netcoreapp3.1 
With the API running, execute the test scripts in order (I used Visual Studio Test -> Test Explorer menu): 
_01TestATMUpdate (Updates the cash on hand as per spec)
_02TestCustomerAdd (Adds the first customer as per spec) 
_03TestBalanceEnquiry (Does a balance enquiry as per spec) 
_04TestWithdrawal (Does the cash withdrawal as per spec)
