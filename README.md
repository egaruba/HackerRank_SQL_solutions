## HackeRank SQL sollutions:

- [Average population](https://www.hackerrank.com/challenges/average-population?h_r=profile) 
        
        SELECT ROUND(AVG(POPULATION),0) FROM CITY;

- [Employee Salaries](https://www.hackerrank.com/challenges/salary-of-employees?h_r=profile) 
        
        SELECT name FROM Employee 
        WHERE SALARY > 2000 AND months < 10 ORDER BY employee_id ASC;

- [Employee Names](https://www.hackerrank.com/challenges/name-of-employees/problem) 
  
        SELECT name FROM Employee ORDER BY name ASC;  

- [Higher Than 75 Marks](https://www.hackerrank.com/challenges/more-than-75-marks/problem?h_r=profile) 
        
        SELECT NAME 
        FROM STUDENTS 
        WHERE MARKS > 75 
        ORDER BY RIGHT (NAME,3), ID;

- [Weather Observation Station 1](https://www.hackerrank.com/challenges/weather-observation-station-1/problem?h_r=profile) 
        
        SELECT CITY, STATE 
        FROM STATION;
        
- [Weather Observation Station 2](https://www.hackerrank.com/challenges/weather-observation-station-2/problem?isFullScreen=true) 

        SELECT ROUND(SUM(LAT_N),2), ROUND(SUM(LONG_W),2)
        FROM STATION;
        
- [Weather Observation Station 3](https://www.hackerrank.com/challenges/weather-observation-station-3/problem?h_r=profile) 
        
        SELECT DISTINCT CITY 
        FROM STATION 
        WHERE ID%2=0;

- [Weather Observation Station 4](https://www.hackerrank.com/challenges/weather-observation-station-4/problem?h_r=profile) 
        
        SELECT (COUNT(CITY) - COUNT(DISTINCT CITY))
        FROM STATION;
        
- [Weather Observation Station 5](https://www.hackerrank.com/challenges/weather-observation-station-5/problem?h_r=profile) 

        SELECT CITY, LENGTH (CITY) FROM STATION
        ORDER BY LENGTH(CITY), CITY LIMIT 1;
        SELECT CITY, LENGTH (CITY) FROM STATION
        ORDER BY LENGTH(CITY) DESC, CITY LIMIT 1;

- [Weather Observation Station 6](https://www.hackerrank.com/challenges/weather-observation-station-6/problem?h_r=profile) 

        SELECT DISTINCT CITY 
        FROM STATION
        WHERE LEFT(CITY, 1) 
        IN ('a','e','o','u','i');

- [Weather Observation Station 7](https://www.hackerrank.com/challenges/weather-observation-station-7/problem?h_r=profile) 
        
        SELECT DISTINCT CITY FROM STATION 
        WHERE CITY LIKE '%a' 
        OR CITY LIKE '%e' 
        OR CITY LIKE'%i' 
        OR CITY LIKE '%o' 
        OR CITY LIKE '%u' ;
- [Weather Observation Station 8](https://www.hackerrank.com/challenges/weather-observation-station-8/problem?h_r=profile) 

        SELECT DISTINCT CITY
        FROM STATION
        WHERE REGEXP_LIKE(CITY,'^[a|e|i|o|u].*[a|e|i|o|u]$');

- [Weather Observation Station 9](https://www.hackerrank.com/challenges/weather-observation-station-9/problem?h_r=profile) 

        SELECT DISTINCT CITY 
        FROM STATION 
        WHERE LEFT(CITY,1) NOT IN ('A','E','I','O','U');
        
- [Weather Observation Station 10](https://www.hackerrank.com/challenges/weather-observation-station-10/problem?h_r=profile) 

        SELECT DISTINCT CITY 
        FROM STATION 
        WHERE RIGHT(CITY,1) NOT IN ('a','e','o','u','i');

- [Weather Observation Station 11](https://www.hackerrank.com/challenges/weather-observation-station-11/problem?h_r=profile) 

        SELECT DISTINCT CITY 
        FROM STATION WHERE LEFT(CITY,1) NOT IN ('a','e','o','u','i') 
        OR RIGHT(CITY,1) NOT IN ('a','e','o','u','i');

- [Weather Observation Station 12](https://www.hackerrank.com/challenges/weather-observation-station-12/problem?h_r=profile) 
        
        SELECT DISTINCT CITY FROM STATION 
        WHERE LEFT(CITY,1) NOT IN ('a','e','o','u','i') 
        and RIGHT(CITY,1) NOT IN ('a','e','o','u','i');
        
        
- [Select All](https://www.hackerrank.com/challenges/select-all-sql/problem?h_r=profile) 

        SELECT * FROM CITY;
        
- [Japanese Cities' Names](https://www.hackerrank.com/challenges/japanese-cities-name/problem?h_r=profile) 

        SELECT NAME 
        FROM CITY 
        WHERE COUNTRYCODE = 'JPN';
        
- [Japanese Cities' Attributes](https://www.hackerrank.com/challenges/japanese-cities-attributes/problem?h_r=profile) 

        SELECT * FROM CITY 
        WHERE COUNTRYCODE = 'JPN';

- [Select By ID](https://www.hackerrank.com/challenges/select-by-id/problem?h_r=profile) 

        SELECT * FROM CITY 
        WHERE ID = 1661;

- [Revising the Select Query II](https://www.hackerrank.com/challenges/revising-the-select-query-2/problem?h_r=profile) 

        SELECT NAME 
        FROM CITY 
        WHERE CountryCode LIKE 'USA' AND POPULATION > 120000;
        
- [Revising the Select Query I](https://www.hackerrank.com/challenges/revising-the-select-query/problem?h_r=profile) 

        SELECT * FROM CITY 
        WHERE CountryCode = 'USA' 
        AND POPULATION > 100000;



- [Weather Observation Station 13](https://www.hackerrank.com/challenges/weather-observation-station-13/problem?h_r=profile) 

        SELECT ROUND(SUM(LAT_N),4) 
        FROM STATION 
        WHERE LAT_N > 38.7880 AND LAT_N < 137.2345;

- [Weather Observation Station 14](https://www.hackerrank.com/challenges/weather-observation-station-14/problem?h_r=profile) 

        SELECT ROUND(MAX(LAT_N),4) 
        FROM STATION 
        WHERE LAT_N < 137.2345;

- [Revising Aggregations - Averages](https://www.hackerrank.com/challenges/revising-aggregations-the-average-function/problem) 
        
        SELECT AVG(POPULATION) 
        FROM CITY 
        WHERE DISTRICT = 'California';
        
- [Weather Observation Station 20](https://www.hackerrank.com/challenges/weather-observation-station-20/problem?h_r=profile) 

        SELECT ROUND(MEDIAN(LAT_N),4) FROM STATION; (ORACLE)
        
- [Revising Aggregations - The Count Function](https://www.hackerrank.com/challenges/revising-aggregations-the-count-function/problem?h_r=profile)         

        SELECT COUNT(NAME) 
        FROM CITY 
        WHERE POPULATION > 100000;
        
- [Population Density Difference](https://www.hackerrank.com/challenges/population-density-difference/problem?h_r=profile) 

        SELECT MAX(POPULATION)-MIN(POPULATION)
        FROM CITY;

- [Revising Aggregations - The Sum Function](https://www.hackerrank.com/challenges/revising-aggregations-sum/problem?h_r=profile) 

        SELECT SUM(POPULATION) 
        FROM CITY
        WHERE DISTRICT = "California";

- [Japan Population](https://www.hackerrank.com/challenges/japan-population/problem?h_r=profile) 

        SELECT SUM(POPULATION)
        FROM CITY
        WHERE COUNTRYCODE = "JPN";

- [Weather Observation Station 16](https://www.hackerrank.com/challenges/weather-observation-station-16/problem?h_r=profile) 

        SELECT ROUND(MIN(LAT_N),4)
        FROM STATION
        WHERE LAT_N > 38.7780;

- [Weather Observation Station 17](https://www.hackerrank.com/challenges/weather-observation-station-17/problem?h_r=profile) 

        SELECT ROUND(LONG_W,4) FROM STATION
        WHERE LAT_N > 38.7780
        ORDER BY LAT_N ASC LIMIT 1;

- [African Cities](https://www.hackerrank.com/challenges/african-cities/problem?h_r=profile) 

        SELECT C.NAME 
        FROM CITY C
        JOIN COUNTRY CO
        ON C.CountryCode = CO.CODE
        WHERE CONTINENT = 'Africa';

- [Average Population of Each Continent](https://www.hackerrank.com/challenges/average-population-of-each-continent/problem?h_r=profile)

        SELECT CO.CONTINENT, FLOOR(AVG(C.POPULATION))
        FROM COUNTRY CO
        JOIN CITY C
        ON C.CountryCode = CO.CODE
        GROUP BY CONTINENT;

- [The Report](https://www.hackerrank.com/challenges/the-report/problem?h_r=profile)

        SELECT 
        CASE
            WHEN G.GRADE < 8 THEN NULL    
            ELSE S.NAME
        END AS NAME, G.GRADE, S.MARKS
        FROM STUDENTS AS S
        JOIN GRADES AS G
        ON S.MARKS BETWEEN G.MIN_MARK AND G.MAX_MARK
        ORDER BY G.GRADE DESC, S.NAME ASC ;

- [Population Census](https://www.hackerrank.com/challenges/asian-population/problem?h_r=profile)

        SELECT SUM(C.POPULATION)
        FROM CITY C
        JOIN COUNTRY CO
        ON C.CountryCode = CO.Code
        WHERE CO.CONTINENT ='ASIA';

- [Top Earners](https://www.hackerrank.com/challenges/earnings-of-employees/problem?h_r=profile)

        SELECT Salary * Months AS INCOME, COUNT(*) 
        FROM EMPLOYEE 
        GROUP BY INCOME 
        ORDER BY INCOME DESC LIMIT 1;

- [Type of Triangle](hackerrank.com/challenges/what-type-of-triangle/problem?h_r=profile)

        SELECT
        CASE
                WHEN A = B and B = C THEN 'Equilateral'
                WHEN (A = B or B = C or C = A) and A + B > C THEN 'Isosceles' 
                WHEN A <> B and B <> C and A + B > C THEN 'Scalene'
                ELSE 'Not A Triangle'
        END AS NAME
        FROM TRIANGLES;

- [The Blunder](https://www.hackerrank.com/challenges/the-blunder/problem?h_r=profile)

        SELECT CEIL(AVG(Salary) - AVG(REPLACE(Salary,'0','')))
        FROM EMPLOYEES ;   

- [Weather Observation Station 15](https://www.hackerrank.com/challenges/weather-observation-station-15/problem?h_r=profile)

        SELECT ROUND(LONG_W,4) 
        FROM STATION
        WHERE LAT_N < 137.2345
        ORDER BY LAT_N DESC
        LIMIT 1;

- [Weather Observation Station 18](https://www.hackerrank.com/challenges/weather-observation-station-18/problem?h_r=profile)

        SELECT 
        ABS(ROUND(max(LAT_N),4)-ROUND(min(LAT_N),4))
        +ABS(ROUND(max(LONG_W),4)-ROUND(min(LONG_W),4)) 
        FROM STATION ;

- [The PADS](https://www.hackerrank.com/challenges/the-pads/problem?h_r=profile)

        SELECT CONCAT(Name, '(', LEFT(Occupation, 1), ')') 
        FROM OCCUPATIONS 
        ORDER BY Name;
        SELECT CONCAT('There are a total of ', COUNT(Occupation), ' ', LOWER(Occupation), 's.') 
        FROM OCCUPATIONS 
        GROUP BY Occupation 
        ORDER BY COUNT(Occupation);

- [Weather Observation Station 19](https://www.hackerrank.com/challenges/weather-observation-station-19/problem?h_r=profile)

        SELECT ROUND(SQRT(POWER((MIN(LAT_N)-MAX(LAT_N)),2)
                        + POWER((MIN(LONG_W)-MAX(LONG_W)),2)),4)
        FROM STATION; 

- []()
