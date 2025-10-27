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

Validations applied for Name,DateofBirth,Occupation,DeathSumInsurred. For wrong input eg : Occupation, you will get below response

  "type": "https://tools.ietf.org/html/rfc9110#section-15.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "errors": {
    "Occupation": [
      "Occupation 'Dancer' is not valid. Choose from: Cleaner, Doctor, Author, Farmer, Mechanic, Florist, Other."
    ]
  },
  "traceId": "00-f1f095e06bc7d4a332e162548b5126a9-84cc2ede8ed92b76-00"
}
