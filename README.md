# angularExcelUpload
excel upload in angular with node js and mysql
First clon the code and run --- npm install
then you need to make db with same name that is available in server.js
after that you need to make a stored procedure in mysql with same name that is in project

Sql code----

CREATE DEFINER=`root`@`localhost` PROCEDURE `employeeAdd`(
IN _EmployeeID int,
IN _FirstName varchar(45),
IN _LastName varchar(45),
IN _Gender varchar(45),
IN _Designation varchar(45),
IN _Salary int,
IN _City varchar(45),
IN _Country varchar(45)
)
BEGIN
		INSERT INTO employeetable(FirstName,LastName,Gender,Designation,Salary,City,Country)
        values(_FirstName,_LastName,_Gender,_Designation,_Salary,_City,_Country);
        
        SET _EmployeeID = last_insert_id();
		SELECT _EmployeeID AS 'EmployeeID';
END

then one more importing thing enable corse in your system
then run the command --  node server.js
and open the html file and perform opration
