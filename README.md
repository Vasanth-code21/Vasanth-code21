
1)SELECT Country, Temperature
FROM country_pollution
WHERE Temperature = (SELECT MAX(Temperature) FROM country_pollution);

2) SELECT Country, CO2_Emissions
FROM country_pollution
WHERE CO2_Emissions = (SELECT MIN(CO2_Emissions) FROM country_pollution);

3) SELECT Country, Temperature, CO2_Emissions, Date
FROM country_pollution
WHERE Temperature > 20;

4) SELECT Country, CO2_Emissions
FROM country_pollution
WHERE Date = 2020;

5) SELECT COUNT(Temperature) AS Total_Temperature_Records
FROM country_pollution;

6) SELECT Country
FROM country_pollution
WHERE Date = 2020 AND Temperature IS NULL;

7) SELECT Date AS Year, AVG(Temperature) AS Average_Temperature
FROM country_pollution
GROUP BY Date
ORDER BY Date;

8) SELECT SUM(CO2_Emissions) AS Total_CO2_Emissions
FROM country_pollution;

9) SELECT Country, Temperature, CO2_Emissions, Date FROM country_pollution
ORDER BY Temperature DESC;
