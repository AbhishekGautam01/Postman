# Creating REST API requests with Postman
* A postman `collection` is a place where we can store our requests. 
* A postman `request` will have default name of URL but it is good to give meaningful names. If we can any changes to collection/request we need to save this as well. 

## Storing Configuration in Variables
* let say we have 20 request in a collection and base url changes so it is good to store it in variable. 
* If you select a text then postman would be pop an option to set it as variable.
![variable](./img/variable-1.png)
![variable](./img/variable-2.png)
* We can choose the scope of the variable. 
* **Variable syntax**: `{{variableName}}`
* You need to save request after creating a variable

## Modifying Collection variables
* You need to go to this collection by clicking on the 3 dots when you hover over collection name then from context menu click on edit. 
* Then you can go to variables tab and edit the variable
![variable](./img/variable-3.png)
* The `initial-value` will be used when you share the collection. The `current-value` is a local private variable for your collection visible to only you even if team is collaborating on same collection. 
* If your variable has secret data then you can set some dummy initial value.

## Get Request