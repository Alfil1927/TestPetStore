# TestPetStore
Postman
1. You should be able to explain why you’ve chosen a particular service opposite
to the others:
Select the web service called "Store" because it is the easiest to understand, it has only 3 types of requests "POST", "GET" and "DELETE", also because I think that the store where you have all the inventory of your products is the most important.
2. Provide a README document as a summary with the guidelines of the taken
approach, the decisions made (e.g. selection criteria for tool, language,
framework, etc.):
- I Select the Postman tool because it allows the creation of requests about web services or APIs in a way that is easier to understand and easier, and allows testing and automation.
- Select the web service called "Store" because it is the easiest to understand, it has only 3 types of requests "POST", "GET" and "DELETE", also because I think that the store where you have all the inventory of your products is the most important.
- The service "POST: Make an order for a pet" was validated with a CSV file with several records, testing your answer and validating the response code 200.  

       “pm.test("Status code is 200", function () {
        pm.response.to.have.status(200);
       });”

- The other services were tested with global variables, example:

  GET: Find purchase order by
  
       "{ 
         "orderId" : {{orderId}}
       }"
   
   DELETE: Delete purchase order by ID
   
        "{ 
           "orderId" : {{orderId}} 
        }"
     
•	Share any test notes, bugs and confusion you've taken notice of while exploring your chosen service of the API in a TEST-NOTES document.

When I started learning about the service, I did not understand how to enter a new order, since there is no request within the "Store" service that it did, but when validating the other services, I discovered that to add a new order to the store, since It's done. by the "Pets" service with the request "POS updates for pets in the store with form data".
