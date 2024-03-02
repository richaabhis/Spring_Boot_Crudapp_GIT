## Spring-boot-thymeleaf
 Simple crud application to perform basic tasks, that we have to know while learning spring boot.Best practice for beginners.

## Features
  1. Image Uplaod
  2. Password encoder
  3. Pagination links
  4. Flash messages
  5. Error pages to handle error code such as 404, 500 etc.

## Technolgies Used 
  1. Spring-boot 3.0.0
  2. Thymeleaf template engine
  3. Spring data jpa
  4. Spring mvc
  5. MySQL database
  6. Developed in SpringToolSuite4 (STS) IDE
  
## HOW TO USE?

Fistly you need to set-up your database. Make sure you have MySQL installed in your PC. 
Database Setup : to setup your database you can use the file database/boot_crud_db.sql. using phpmyadmin = if you are using php myadmin then simpley create a new database with the name of 'chat' and then you can import file database/boot_crud_db.sql from your import tab.
    
creating a database :
    
```sql
CREATE DATABASE boot_crud_db;
```

using the database :

```sql
USE boot_crud_db;
```

creating database table :

```sql
CREATE TABLE `users` (
  `id` bigint(20) NOT NULL,
  `dob` date DEFAULT NULL,
  `email` varchar(255) DEFAULT NULL,
  `name` varchar(255) DEFAULT NULL,
  `password` varchar(255) DEFAULT NULL,
  `image` varchar(255) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;
```

```
  set the unique id to handle big requests as well:

```sql
ALTER TABLE `users`
  MODIFY `id` bigint(20) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=40;
COMMIT;
```
dummy data:

```sql
INSERT INTO `users` (`id`, `dob`, `email`, `name`, `password`, `image`) VALUES
(20, '2024-02-23', 'raj@gmail.com', 'Raj kumar', '$2a$10$NI5IFvnLxpXlkjSplgsB2e2bOjHkEHtCZ7kfVzdRDPTVpJk9WH.Iu', 'cfb47473-369c-4be9-b3d0-a2bdbcdcfe38.jpg'),
(21, '2024-01-31', 'mysql@gmail.com', 'SpaceX', '$2a$10$9Oal.rc7J/0qewwsPbFOIuNgjTNGMRE2Zh1nxmY0CRTsiEK1IFRFO', 'adefefb9-b7c6-43d6-a661-c4a1ae42cc53.png');
```