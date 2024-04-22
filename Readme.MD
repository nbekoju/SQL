## SQL Hackerrank Basic Solution
**Revising the Select Query I**
```
SELECT * FROM CITY WHERE POPULATION > 100000 AND CountryCode = "USA"
```

**Select All**
```
SELECT * FROM CITY;
```

**Select By ID**
```
SELECT * FROM CITY WHERE ID=1661;
```

**Japanese Cities' Attributes**
```
SELECT * FROM CITY WHERE COUNTRYCODE = "JPN"
```

**Japanese Cities' Names**
```
SELECT NAME FROM CITY WHERE COUNTRYCODE = "JPN";
```

**Weather Observation Station 1**
```
SELECT CITY, STATE FROM STATION;
```

**Higher Than 75 Marks**
```
SELECT Name
FROM STUDENTS
WHERE Marks > 75
ORDER BY RIGHT(Name, 3), ID ASC;
```

**Employee Names**
```
SELECT name FROM Employee ORDER BY NAME
```

**Employee Salaries**
```
SELECT name FROM Employee WHERE salary > 2000 and months < 10 ORDER BY employee_id
```

**Revising Aggregations - The Count Function**
```
SELECT COUNT(*) FROM City WHERE Population > 100000
```

**Revising Aggregations - The Sum Function**
```
SELECT SUM(Population) AS TotalPopulation FROM CITY WHERE District = 'California';
```

**Average Population**
```
SELECT FLOOR(AVG(Population)) AS AveragePopulation FROM CITY;
```

**Japan Population**
```
SELECT SUM(Population) AS AveragePopulation FROM CITY WHERE COUNTRYCODE="JPN";
```

**Average Population of Each Continent**
```
SELECT 
    COUNTRY.Continent,
    FLOOR(AVG(CITY.Population)) AS AverageCityPopulation
FROM 
    CITY
JOIN 
    COUNTRY ON CITY.CountryCode = COUNTRY.Code
GROUP BY 
    COUNTRY.Continent;
```

**Top Earners**
```
SELECT months * salary, COUNT(*)
FROM employee
GROUP BY months * salary
ORDER BY months * salary DESC
LIMIT 1;
```