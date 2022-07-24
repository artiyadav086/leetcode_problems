# leetcode_SQL_problems
solutions

175. Combine Two Tables
-----------------------
select firstname, lastname, city, state
from Person as p                          </br>
left join Address as a 
on a.personid = p.personid;
</br></br>

181. Employees Earning More Than Their Managers
-----------------------------------------------
select e1.Name as Employee from employee as e1, employee as e2          
where e1.managerId=e2.id and e1.salary> e2.salary;
</br></br>

182. Duplicate Emails
-----------------------
select Email from Person
group by Email
having count(Email)> 1;
</br></br>

183. Customers Who Never Order
-------------------------------
select Name as Customers from Customers
where id not in (select customerId from Orders);
</be></br>
196. Delete Duplicate Emails
--------------------------------
delete P2
from Person P1, Person P2
where P1.Email= P2.Email
and P1.Id< P2.Id;
