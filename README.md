Open the application using  VS Code.

In VS Code Go to Terminal--> New Terminal 

command : PS C:\.NetApp\PremiumCalculatorApp> dotnet run

After running successfully access below URL
http://localhost:5252/Premium

clarification: Only Name, DOB, Occupation are required fields.
Don't have access to SSMS to create DB.
Don't have access to Azure.
To test API using Swagger Use link http://localhost:5252/swagger.
Request body sample :
{
  "name": "Sheela",
  "dateOfBirth": "1990-10-27T12:16:15.383Z",
  "occupation": "Cleaner",
  "deathSumInsured": 100000
}
