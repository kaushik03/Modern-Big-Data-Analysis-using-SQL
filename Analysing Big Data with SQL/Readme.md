# Analyzing Big Data with SQL 

## Graded Assignment : 
1. F​or this assignment, you will query and analyze flights data to inform a business decision.
2. Imagine that you have been hired as a `data analyst` for a company that plans to disrupt the airline industry by building an underground high-speed passenger rail tunnel. 
3. The company needs your help to decide which two major United States airports this tunnel should connect. 
4. T​he distance between the airports must be within a specified range, and the airports must have a large volume of air travelers flying between them in both directions. 
5. The company believes that these air travelers can be persuaded to switch to high-speed rail because of frustratingly long flight delays.

## The Task
 - Your job is to recommend which pair of **United States airports** should be connected with a high-speed passenger rail tunnel. 
 
- The company you work for has given you the following strict requirements:
- These two airports must:
    - Be between 300 and 400 miles apart
    - Average at least 5,000 (five thousand) flights per year between them, in each direction
    - Among the pairs of airports that meet these requirements, you must identify the one pair that has the largest total number of seats on the planes that flew between them.

    - The company is also interested to know the average arrival delay for flights between these two airports, because they believe that routes with a history of delayed arrivals will make it easier to persuade air travelers to switch to high-speed rail.

1. For the pair of airports you recommend, you must provide the following details:
    1. The three-letter codes identifying both airports
    2. The average flight distance in miles for flights between the airports, in each direction
    3. The average number of flights per year between the airports, in each direction
    4. The average annual passenger capacity (average yearly total number of seats on the planes) for flights between the airports, in each direction
    5. The average arrival delay for flights between the airports, in each direction

**Write the SQL Query** 
You must write a `SELECT statement` to identify the pair of airports that fulfills all the requirements listed above. This SELECT statement must also return all the required details listed above.


The following hints might help you:
From the given Database `Fly` in VM.
The flights table has a column named distance which gives the distance in miles of each flight. Use the values in this column as the distances between airports.
The planes table contains ten years of flights data, so to get per-year (annual) average totals, divide the full-table totals by ten.
The planes table has a column named seats which gives the number of seats on each plane.
The first two rows in the result of your query should show your recommended tunnel route. These top two rows should both show the same pair of airports, but with the origin and dest switched.