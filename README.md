## HackeRank SQL sollutions:

- [Average population](https://www.hackerrank.com/challenges/average-population?h_r=profile) 
        
        SELECT ROUND(AVG(POPULATION),0) FROM CITY;

- [Employee Salaries](https://www.hackerrank.com/challenges/salary-of-employees?h_r=profile) 
        
        SELECT name FROM Employee 
        WHERE SALARY > 2000 AND months < 10 ORDER BY employee_id ASC;

- [Employee Names](https://www.hackerrank.com/challenges/name-of-employees/problem) 
  
        SELECT name FROM Employee ORDER BY name ASC;
  
- [Weather Observation Station 12](https://www.hackerrank.com/challenges/weather-observation-station-12/problem?h_r=profile) 
        
        SELECT DISTINCT CITY FROM STATION 
        WHERE LEFT(CITY,1) NOT IN ('a','e','o','u','i') 
        and RIGHT(CITY,1) NOT IN ('a','e','o','u','i');
- [Higher Than 75 Marks](https://www.hackerrank.com/challenges/more-than-75-marks/problem?h_r=profile) 
        
        SELECT NAME 
        FROM STUDENTS 
        WHERE MARKS > 75 
        ORDER BY RIGHT (NAME,3), ID;


