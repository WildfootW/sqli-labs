# README

SQLI-LABS is a platform to learn SQL Injections.


Following labs are covered for GET and POST scenarios:

1. Error Based Injections (Union Select)
	1. String
	2. Integer
2. Error Based Injections (Double Injection Based)
3. BLIND Injections:
	1. Boolian Based
	2. Time Based
4. Update Query Injection.
5. Insert Query Injections.
6. Header Injections.
	1. Referer based.
	2. UserAgent based.
	3. Cookie based.
7. Second Order Injections
8. Bypassing WAF
	1. Bypassing Blacklist filters
		- Stripping comments
		- Stripping OR & AND
		- Stripping SPACES and COMMENTS
		- Stripping UNION & SELECT
	2. Impidence mismatch
9. Bypass addslashes()
10. Bypassing mysql_real_escape_string. (under special conditions)
11. Stacked SQL injections.
12. Secondary channel extraction

---

## Installation

### The easy way (with docker)

Using [docker-compose](https://docs.docker.com/compose/) you can simply:

```
docker-compose up
```

Browse to the labs on http://localhost:8080, then click on `Setup/reset Database for labs` and follow up the instructions in the [YouTube video series](https://www.youtube.com/watch?v=NJ9AA1_t1Ic&list=PLkiAz1NPnw8qEgzS7cgVMKavvOAdogsro&index=23).

![Lessons](index.html_files/injection_types.png)

#### connect in to sql server
1. Use `docker ps` find `mysql:5.7`'s container ID
2. use `docker inspect {{ID}}` check the container's IPAddress
3. `mysql -u root -P 3306 -h {{IPAddress}} -p` password: toor

### The hard way (deploy in your own environment)

1. Unzip the contents inside the apache folder, for example under `/var/www`
2. This will create a folder sql-labs under it. else you can use git command from within `/var/www` folder.
`/var/www` folder and then use following command> git clone https://github.com/Audi-1/sqli-labs.git sqli-labs
3. Open the file `db-creds.inc` which is under sql-connections folder inside the sql-labs folder.
4. Update your MYSQL database username and password.(default for Backtrack are used root:toor)
5. From your browser access the sql-labs folder to load `index.html`
6. Click on the link `setup/resetDB` to create database, create tables and populate Data.
7. Labs ready to be used, click on lesson number to open the lesson page.
8. Enjoy the labs

---

Corresponding walkthrough video tutorials and explainations can be found at:

1. [YouTube Video Series](https://www.youtube.com/watch?v=NJ9AA1_t1Ic&list=PLkiAz1NPnw8qEgzS7cgVMKavvOAdogsro&index=23)
1. http://dummy2dummies.blogspot.com 
2. http://www.securitytube.net/user/Audi
3. https://www.facebook.com/sqlilabs

You can also find the read along book at https://leanpub.com/SQLI-LABS, work is under process.

---

Challenge Section added:
Less-54 to Less - 61 special challenge lessons added to repository for testing skills learnt from the other Lab lessons.

---

