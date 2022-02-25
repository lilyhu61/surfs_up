# surfs_up
## Overview of the statistical analysis
The purpose of our analysis is to see temperature statistics for June and December to determine if running a surf shop is sustainable year around. The way we get the temperature data is by running two seperate queries, one being for June and the other being December. Once we run our queries we store the temperatures in a list then convert them to a dataframe. Once our dataframe is created we are able to get our summary statistics by using the .describe() method. 
## Results
What we found as following:
-  In June we had a total count of 1700, mean of 74.9, min of 64.0 and max of 85.0


![Screen Shot 2022-02-25 at 12 51 08 PM](https://user-images.githubusercontent.com/95242493/155785661-ad848c0d-3a48-4791-8d3b-244a9b15261a.png)

- In December we had a total count of 1517, mean of 71.0, min of 56.0 and max of 83.0


 ![Screen Shot 2022-02-25 at 12 52 19 PM](https://user-images.githubusercontent.com/95242493/155785817-b236976a-0df8-46fd-b782-bd77158dda0d.png)
 
 
 
 
- Standard deviation is 3.25 in June and 3.75 in December, making a 0.5 difference between two seasons

## Summary
Since there are other attributes to the weather such as all the precipitation for the month of June and December. It shows we can run additional queries to let us know whether or not people can come and visit the shop. Queries will look like as following:
- results = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date)==6).all()
- results = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date)==12).all()
