# Big Data – Hadoop Ex1
## Lior Berlin 206363236, Nika Klimenchuk 22997628
### Exercise 1 – Job Configuration and Outputs

#### First run (default number of reducers)

- Launched map tasks: 9  
- Launched reduce tasks: 3  
- Merged Map outputs: 27  
- Partition files: 3  

#### Second run (-numReduceTasks 6)

- Launched map tasks: 9  
- Launched reduce tasks: 6  
- Merged Map outputs:** 54  
- Partition files: 6  


#### Answers

**Q1: How many files are there now?**  
**A1:** 6 partition files (7 in total including the _SUCCESS file).


**Q2: Did the number of mappers change?**  
**A2:** No, it’s still 9.


**Q3: Did the number of reducers change?**  
**A3:** Yes, it changed from 3 to 6.


**Q4: Did the number of output files change? Why?**  
**A4:** Yes, it changed from 3 to 6.  
Each reducer writes its own partition output file.


**Q5: What does the value of “Merged Map outputs” represent and how is it calculated?**  
**A5:** It’s the number of map output files that the reducers had to merge.  
Each mapper creates spill files, and the reducers merge all of them together during the shuffle and sort phase.

---

### Exercise 2 – Case Insensitive and Punctuation Handling

**Q: Is the code change in the mapper or the reducer?**  
**A:** In the mapper.

---

### Exercise 3 – Sample Word Counts

of 34588

and 42768

the 74369

**Screenshot:**

<p align="center">
  <img src="https://raw.githubusercontent.com/Nika-Klimen/Ex1_Big_Data_Lior_206363236_Nika_322997628/refs/heads/main/Screenshot%202025-11-27%20145645.png" width="600">
</p>
