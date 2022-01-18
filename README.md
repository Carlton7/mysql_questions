# mysql_questions
answers to sql query


1.SELECT COUNT(CountryCode) FROM city WHERE CountryCode = 'USA'

2.SELECT name, population, LifeExpectancy FROM country WHERE name = 'Argentina';

3.SELECT * FROM country ORDER BY LifeExpectancy DESC LIMIT 1 

4.SELECT * 
  from country co
  join city ci on co.Capital=ci.ID
  WHERE co.name = 'Spain';

5.SELECT name, Region, language 
  from country co
  join countrylanguage cl on co.Code=cl.CountryCode
  WHERE co.Region = 'Southeast Asia';

6.SELECT * FROM city WHERE Name LIKE 'f%' LIMIT 25;

7.SELECT count(*) 
  from country co
  join city ci on co.Code=ci.CountryCode
  WHERE co.Code = 'CHN';

8.SELECT * FROM country WHERE Population !=0 ORDER BY population ASC LIMIT 1 

9.SELECT COUNT(Capital) FROM country 

10.SELECT * FROM country ORDER BY SurfaceArea DESC LIMIT 10;

11.select * FROM city WHERE CountryCode = 'JPN' ORDER BY Population DESC LIMIT 5;

12.update country SET HeadOfState = replace(HeadOfState, 'Elisabeth II', 'Elizabeth II') WHERE HeadOfState LIKE ('Eli%');
   SELECT code,Name FROM country WHERE HeadOfState='Elizabeth II'

13.SELECT name, Population/SurfaceArea FROM country WHERE Population/SurfaceArea !=0 ORDER BY Population/SurfaceArea ASC ;

14.SELECT DISTINCT(language) FROM countrylanguage;

15.SELECT name, GNP FROM country order by GNP Desc limit 10;

16.SELECT name, COUNT(name) as langNum
   FROM country co
   JOIN countrylanguage cl on cl.CountryCode=co.Code
   GROUP BY co.name ORDER BY langNum DESC LIMIT 10;

17.SELECT *
   from country co
   join countrylanguage cl on co.Code=cl.CountryCode
   WHERE cl.language = 'German' AND cl.Percentage > 50.0;

18.SELECT * FROM country where LifeExpectancy != 0 ORDER BY LifeExpectancy ASC LIMIT 1;

19.SELECT GovernmentForm, COUNT(GovernmentForm) as GovNum FROM country
   GROUP BY country.GovernmentForm ORDER BY GovNum DESC LIMIT 3;

20.SELECT COUNT(*) FROM country WHERE IndepYear !=0; 
