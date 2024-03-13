# chicago_crime_analysis

Q) What are the top ten communities that had the LEAST amount of crimes reported? Include the current population, density and order by the number of reported crimes.

A)
SELECT 
    COMMUNITY_AREA, COUNT(community_area)AS LEAST_CRIME_COUNT, POPULATION, DENSITY 
FROM
    chicago_crime_2018, CHICAGO_AREAS
WHERE CHICAGO_CRIME_2018.COMMUNITY_AREA = CHICAGO_AREAS.COMMUNITY_ID
GROUP BY community_area
ORDER BY LEAST_CRIME_COUNT
LIMIT 10;

