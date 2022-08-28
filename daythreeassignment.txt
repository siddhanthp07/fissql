use daytwoassignment

--1
select * from Emp where Job = 'Manager'

--2
select Ename,Sal from Emp where Sal > 1000

--3
select Ename,Sal from Emp where Ename != 'James'

--4
select * from Emp where Ename like 'S%'

--5
select Ename from Emp where Ename like '%a%'

--6
select Ename from Emp where Ename like '__l%'

--7
select Sal/30 from Emp where Ename = 'Jones'

--8
select sum(Sal) from Emp 

--9
select avg(Sal) from Emp

--10
select Ename,Job,Sal,Deptno from Emp where Job!='Salesman' and Deptno!=30

--11
select Name from Dept where Deptno = any (select distinct(Deptno) from Emp)

--12
select Ename as 'Name',Sal as 'Salary' from Emp where Sal > 1500 and (Deptno=10 or Deptno=30)

--13
select Ename,Job,Sal from Emp where (Job = 'Manager' or Job = 'Analyst') and (Sal!=1000 or Sal!=3000 or Sal!=5000)

--14
select Ename,Sal,Comm from Emp where Comm > Sal + Sal*0.1

--15
select Ename from Emp where Ename like '%ll%' and (Deptno=30 or Mgrid=7782)

--16
select Ename,DATEDIFF(year,Hiredate,SYSDATETIME()) as 'Years of Experience',count(Ename) from Emp where DATEDIFF(year,Hiredate,SYSDATETIME()) between 10 and 20 group by Ename,Hiredate

--17

select Emp.Ename,Dept.Name from Emp join Dept on Emp.Deptno= Dept.Deptno order by Emp.Ename , Dept.Name desc

--18
select Ename,FLOOR(DATEDIFF(year,Hiredate,SYSDATETIME())) as 'Years of Experience' from emp where Ename='Miller'



