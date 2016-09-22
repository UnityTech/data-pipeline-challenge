We're excited you are applying to Unity! As a part of the recruitment process, we would like to validate your technical skills through a small assignment. Return your answer as a zip file containing all relevant files _with tests and documentation_. Include `.git`, so that we can see your commit history.

Do *not* fork this repository.

# Assignment

You have been given access to files containing data describing all of the airline flights in the U.S. from 1987-2008.

A "route" is an ordered pair of cities from source to destination (e.g., SFO to BOS).  Note that since the pair is ordered, "SFO-BOS" is not the same thing as "BOS-SFO".

Design and implement (with proper unit tests) a Hadoop program in Java to answer the following question:

For each route, calculate the average number of minutes late that the flights were over the data files provided and output the 100 routes with the largest average arrival delay.

## Equipment

You have been given access to an Amazon EMR cluster and an S3 bucket containing data to be analyzed. Your Hadoop job should run on the cluster, reading the data files from the S3 bucket and writing the output file there.

## Additional notes

1. The input files are CSV and have column headings.  Additionally, some lines have "NA" for some values. Do not edit the files by hand to clean up the data -- instead, your program should detect invalid values and ignore those lines gracefully.

2. Origin, Dest, and ArrDelay (arrival delay) are the columns you should use to answer the question.

3. Consider integer overflow when handling large amounts of input.

4. Your program should use appropriate data structures to make reasonably efficient use of memory and CPU.

5. If you need multiple MapReduce jobs, your program should take care of sequencing them properly.

## Bonus

Once you have written the Hadoop program, write a program in Spark to compute the same answer.
