## SQL for Data Analysis
```sql
use [SQL Tutorial]
go

select * from EmployeeDemographics;

select * from EmployeeDemographics
where FirstName in('John', 'Christopher', 'Emily', 'Amanda');

select FirstName, LastName, Age from EmployeeDemographics;

-- distinct -> returns the very first unique value in a column
select distinct(Gender)
from EmployeeDemographics;

-- group by -> returns unique values in a column similar to the
--				distinct statement
--				It summarizes all the rows by rolling them up into one column 
--				count is a derived column that's derived from the Gender column
select Gender, count(Gender) as row_count
from EmployeeDemographics
where Age > 30
group by Gender
order by row_count asc;

select distinct FirstName
from EmployeeDemographics
order by FirstName;

select Gender, Age, count(Gender) as row_count from	EmployeeDemographics
group by Gender, Age;

-- Ordering by FirstName and Age
select * from EmployeeDemographics
order by FirstName, Age asc;
--order by FirstName, Age asc;
--order by FirstName asc, Age desc;

```
