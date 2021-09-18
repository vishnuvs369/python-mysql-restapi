# Python-Mysql-RestAPI

HTTP methods are mapped to CRUD (create, read, update and delete) actions for a resource. Although you can make slight modifications such as making the PUT method to be create or update, the basic patterns are listed as follows.

GET: Get/List/Retrieve an individual resource or a collection of resources.
POST: Create a new resource or resources.
PUT: Update an existing resource or collection of resources.
DELETE: Delete a resource or collection of resources.

# Create MySQL database table – tbl_user with the following structure.

CREATE TABLE `tbl_user` (
  `user_id` bigint COLLATE utf8mb4_unicode_ci NOT NULL AUTO_INCREMENT,
  `user_name` varchar(45) COLLATE utf8mb4_unicode_ci DEFAULT NULL,
  `user_email` varchar(45) COLLATE utf8mb4_unicode_ci DEFAULT NULL,
  `user_password` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL,
  PRIMARY KEY (`user_id`)
) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;



Display All Users
GET : http://localhost:5000/users

Add New User
POST  : http://localhost:5000/add

{
	"name":"vishnu",
	"email":"contact@vishnu.com",
	"pwd":"pwd"
}

Update User
POST : http://localhost:5000/update

Request body

Delete a User
GET : http://localhost:5000/delete/2