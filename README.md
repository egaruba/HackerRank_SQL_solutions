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

