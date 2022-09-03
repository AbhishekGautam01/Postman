# Automatically running tests
* We can automate using
    1. Collection running 
    2. Postman monitors (Pro feature)
    3. Newman 
    4. Newman + Jenkins 
    5. Newman + other CI servers

## Postman Collection runner 
* After clicking on a collection you will get a **Run** Button and clicking on it will open the collection runner. 
* You need to select the environment, all requests you want to run , iterations, delay, etc
![Collection runner](./img/collection-runner.png)
* Once run is completed you will get the run summary and you can export the report as well. 
![summary](./img/collection-runner-summary.png)

## Postman Monitor 
* It allows to run api calls at regular intervals. This is pro feature but currently we can make 1000 call/month. 
* You need to go monitor tabs and create a monitor by filling in all details. 
* Postman server are not in the same network as you are. 
* We cannot import global variables but they can be created from scripts. 
* Global and environment variables are not persisted for later runs. 
