We're excited you are applying to Unity! As a part of the recruitment process, we would like to validate your technical skills through a small assignment. Return your answer as a zip file containing all relevant files _with tests and documentation_. Include `.git`, so that we can see your commit history.

Do *not* fork this repository.

# Assignment

You have been given access to files containing data describing all of the airline flights in the U.S. from 2000-2008.

A "route" is an ordered pair of cities from source to destination (e.g., SFO to BOS).  Note that since the pair is ordered, "SFO-BOS" is not the same thing as "BOS-SFO".

Design and implement (with proper unit tests) a Hadoop program in Java to compute the following:

For each route, calculate the average number of minutes late that the flights were over the data files provided and output the 100 routes with the largest average arrival delay.

*IMPORTANT: The input files provided are small samples to allow you to test your program.  Please design your program to work correctly and efficiently on data at a much larger scale (e.g. billions of rows).  We are looking for you to demonstrate not just that you can use Hadoop, but that you know how to handle very large data sets using it.*

## Equipment

The data files to use as input are in Amazon S3 at <https://s3-us-west-2.amazonaws.com/unity-public-data/flight_data/input.zip>. Install Hadoop on your computer and run your program using Hadoop in Local (Standalone) Mode.

## Additional notes

1. The input files are CSV and have column headings.  Additionally, some lines have "NA" for some values. Do not edit the files by hand to clean up the data -- instead, your program should detect invalid values and ignore those lines gracefully.

2. Origin, Dest, and ArrDelay (arrival delay) are the columns you should use to answer the question.

3. Your program should use appropriate data structures to make reasonably efficient use of memory and CPU.

4. If you need multiple MapReduce jobs, your program should take care of sequencing them properly.

5. We recommend writing your Hadoop program in Java, but you may also use another language (Python, R, etc.) using Hadoop Streaming. However, higher level abstractions such as Hive and Pig are not allowed.

## Bonus Problem

Once you have written the Hadoop program, write a program in Spark to compute the same answer.
