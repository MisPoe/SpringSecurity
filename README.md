# SpringSecurity
Spring MVC

Create Maven Project - web

Spring Architecture  -> Require Dependency need to load


Request -------------> Frontend Controller ---> Application Layer------------------------------------> Persistence Layer
store.com/		 DispatcherServelt ----> index
store.com/viewstore                        -----> StoreController (view method)   ---service -----   Dao (storeDao -ViewMethod)		
store.com/savestore                        -----> StoreController (save Method)                      Store Dao (saveMethod)

Mapping   (/*)              Handle


-----------------------------------------------------------------------------------------------------------------------------------
Withoud Using JPA
===================

Service ---------------------------- Persisternce Layer ----------------------------- Database

Methodcall			     Select * from (looping)			     StoreDB
				     Insert into

JPA
====
Service ---------------------------- Persisternce Layer ----------------------------- Database

repo.save();			     JPARespository (CRUD) .save .findAll
repo.findall();		 	     CRUDRespository (CRUD)


JPA
=====================
Pom.xml -> Require Dependency (ORM, JPA , MYSQL Connector)

Create table and connect to the databse
	Write Entity Class -> user, role, store
	Write application.properties or persistence.xml -> For MYSQL Configuration
	Create JPA Config Class (2) (set the property, load the requrie data manager/transaction manager)
-----------------------------------------------------------------------------------------------------
Spring Secuirty
=====================

Pom.xml -> Require Dependency (Security Core, Config, Web)

	   Write Spring Config (3) extends WebSecurityConfigurerAdapter (SecurityConfig.java)
			- Two Methods
				configure Auth  - (UserDetailServiceImpl.java) -> User Repo & User Entity
				configure Authorize - UserController (mapping & roles) 
	 			
	   To look for the springSecurityFilterChain & Register(SpringSecurityInitializer.java)
	



Unit testing is a form of white box testing, in which test cases are based on internal structure. 
The tester chooses inputs to explore particular paths, and determines the appropriate output. The purpose of 
unit testing is to examine the individual 
components or pieces of methods/classes to verify functionality, ensuring the behavior is as expected.
