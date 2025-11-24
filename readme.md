# Big Data Hadoop Exercise

## Authors

- Gal Rubinstein
- Michael Gurevich

---

## Hadoop Training questions

### Exercise 1

#### **Before flag** `-numReduceTasks 6`:
- Launched map tasks: 9
- Launched reduce tasks: 3
- Merged Map outputs: 27

#### **After flag** `-numReduceTasks 6`:
- Launched map tasks: 9
- Launched reduce tasks: 6
- Merged Map outputs: 54

#### Questions:
1. How many files are there?  
   <u>Answer</u>: Excluding the _SUCCESS file, there are 6 files.
2. Did number of mapper change?  
   <u>Answer</u>: No.
3. Did number of reducer changed?  
   <u>Answer</u>: Yes.
4. Did numbers of output files change? Why?  
   <u>Answer</u>: Yes, because we specified 6 reducer tasks, each reducer runs independently and writes its final result to its own unique file in the HDFS output directory.
5. What does the value of 'Merged Map outputs' represents and how is it calculated?  
   <u>Answer</u>: The number of possible tuples between mapper and reducer.  
   There are 9 tasks of mappers, each of the 6 reducers receives the output of the mappers, hence 6 reducers each receiving 9 mapper outputs: 6x9 = 54.

---

### Exercise 2
1. Is your change in the mapper or in the reducer?  
   <u>Answer</u>: Mapper.
2. Submitted the code in GitHub.

---

### Exercise 3
1. Is your change in the mapper or in the reducer?  
   <u>Answer</u>: Reducer.
2. Submitted the code in GitHub.
3. Print the output of the MapReduce and add to the project.  
   <u>Answer</u>:  
   - (the, 74369)  
   - (and, 42768)  
   - (of, 34588)

## License

This repository is intended for educational purposes only.
