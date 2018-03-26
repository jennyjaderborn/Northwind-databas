# Northwind-databas
Inlämningsuppgift 2 databasteknik

 #1 SELECT DISTINCT country FROM Employees;

 #2 SELECT categoryid, categoryName FROM Categories ORDER BY categoryName DESC;

 #3 SELECT CompanyName, ContactName, Phone, Fax FROM Customers WHERE Country='Germany' ORDER BY CompanyName DESC;

 #4 SELECT City FROM Customers WHERE country='Sweden';

 #5 SELECT ProductName FROM `Products` WHERE ProductName LIKE '%br-d%';

 #6 SELECT FirstName, LastName FROM `Employees` WHERE BirthDate = '1966-01-27-00:00';

 #7 SELECT FirstName, LastName FROM `Employees` WHERE ReportsTo IS NULL;

 #8 SELECT ProductName, UnitsInStock, ReorderLevel FROM `Products` WHERE UnitsInStock < ReorderLevel;

 #9 SELECT CompanyName, Country, Phone, HomePage FROM `Suppliers` WHERE Country = 'Germany' OR Country = 'France'ORDER BY CompanyName DESC;

 #10 SELECT ProductID, ProductName, UnitPrice, UnitsInStock FROM `Products` WHERE UnitsInStock > 100 ORDER BY UnitPrice DESC, UnitsInStock ASC; 

 #11 SELECT BirthDate FROM `Employees` ORDER BY BirthDate ASC LIMIT 1;

 #12 SELECT AVG(Products.UnitPrice), SUM(Products.UnitPrice) FROM `Products` INNER JOIN Categories ON Products.CategoryID = Categories.CategoryID WHERE Categories.CategoryID = 2;

 #13 SELECT Discount AS 'StörstRabatt' FROM `Order_Details` ORDER BY Discount DESC LIMIT 1;

 #14 SELECT COUNT(CategoryName) FROM `Categories`;

 #15 SELECT Country, COUNT(CompanyName) AS 'antal' FROM `Customers` GROUP BY Country ORDER BY COUNT(CompanyName) DESC;

 #16 SELECT SupplierID, AVG(UnitPrice) AS 'Snittpris' FROM `Products` WHERE CategoryID IN(1,3,5,7) GROUP BY SupplierID;

 #17 SELECT CategoryID FROM `Products` GROUP BY CategoryID HAVING COUNT(ProductID) > 10;

 #18 SELECT O.CustomerID, COUNT(*) AS 'AntalOrdrar' FROM Orders AS O WHERE O.OrderDate between '1998-01-01' AND '1998-12-31' GROUP BY O.CustomerId HAVING COUNT(*) > 10 ORDER BY AntalOrdrar;


#19 SELECT OrderID, SUM(UnitPrice*Quantity) AS OrderSumma FROM Order_Details WHERE OrderID > 10500 GROUP BY OrderID HAVING OrderSumma > 10000 ORDER BY OrderSumma DESC;

#20 SELECT ProductID, SUM(Quantity) FROM `Order_Details` GROUP BY ProductID ORDER BY SUM(Quantity) DESC LIMIT 10; 

#21 SELECT o.ShipCountry, c.customerID, COUNT(*) AS 'antal' from Orders AS o INNER JOIN Customers c ON o.customerid = c.customerid WHERE o.Shipregion IS NULL GROUP BY o.ShipCountry, c.customerID HAVING COUNT(*) > 10 ORDER BY c.country DESC, c.customerid ASC;



