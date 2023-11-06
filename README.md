# New York Taxi Trip Analysis

## Dataset 
The datasets consist of a log of taxi trips including starting point, drop-off point, corresponding timestamps, and information related to the payment.
Data is ordered by the datetime of the end of the trip. Events with the same dropoff_datetime are in random order.
Quality of the data is not perfect.
• Some coordinates seem to be incorrect (far from NYC).
• Some events might miss information such as drop off and pickup coordinates or fare
information.
• Moreover, some information, such as, e.g., the fare price might have been entered
incorrectly by the taxi drivers thus introducing additional skew.

Original data from ACM DEBS 2015 Grand Challenge
http://www.debs2015.org/call-grand-challenge.html

## Project
The project was designed to be implemented using Pandas/scikit learn and Spark.

- **Question 0 [2 points out of 20]**
The notebook provided includes a basic computation, implemented in Spark and Pandas for computing the number of trips per taxi driver.
Run the program with the three datasets in Colab. Present the results and draw some conclusions.

- **Question 1 [3 points out of 20]**
The first question intends to help the city to identify which new express bus routes should be introduced. To this end, you should find the most frequent routes whose distance is above a given threshold (defined by you).
For establishing these routes, we suggest that you use a grid of 500m of side.

- **Question 2 [4 points out of 20] (cont.)**
The taxi trips can be classified in two categories, depending on whether the client has given a tip or not (or alternatively in three categories - no tip, low percentage tip, high percentage tip). In the third question you should propose a method to predict the class of a given trip (for this prediction, you cannot use the value of the tip) and evaluate the quality of your proposal.
The expect output will be the value that quantifies the quality of your solution.

- **Question 3 [4 points out of 20]**
The third question intends to help taxi drivers to decide to which area of the city they should go next. To this end, we could have a web site/mobile app where the drivers could check the best area at a given moment. To support such application efficiently, it would be necessary to have a pre- computed index with the value for each area and period of time (e.g. combining the weekday and a period of one hour).
You should create the program to create such index. The output tuples should be something like:
  longitude latitude day_of_week hour value
Define your own metric for the value of an area. Parameters that may be included in such metric include: the number of pickups in the area, the amount collected in the trip, the average time a taxi is idle in the area, etc. The metric may be multi-valued (i.e., include different numbers).
Besides presenting the code, explain the rationale of your solution. NOTE: there is no right metric here – propose one that makes sense.

- **Question 4 [4 points out of 20]**
The fourth question intends to define the location of taxi ranks (the places where taxis stop waiting for collecting clients) in a way that tries to minimize the distance a client needs to travel to reach the taxi rank.
Consider that you want to establish between 100 and 150 taxi ranks - present the code that defines the number and locations of the ranks.
Besides presenting the code, explain the rationale of your solution.
Suggestions:
Data is for NYC taxis, so data outside NYC might not be relevant for defining taxi ranks – use a square that includes only the city.
Plot your results in a graph (e.g., as a heatmap, with the color being the quality of the taxi rank); use the visual feedback to enhance your solution.

- **Question 5 [3 points out of 20]**
Propose a problem to be solved and solve it using the techniques you have learnt in this course.
The valuation of your solution will take into consideration the following aspects: complexity; quality of the solution; difference from the previous questions.
