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

- [Weather Observation Station 12](https://www.hackerrank.com/challenges/weather-observation-station-12/problem?h_r=profile) 
        
        SELECT DISTINCT CITY FROM STATION 
        WHERE LEFT(CITY,1) NOT IN ('a','e','o','u','i') 
        and RIGHT(CITY,1) NOT IN ('a','e','o','u','i');
        
        
- []() 
