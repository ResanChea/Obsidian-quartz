---
{"dg-publish":true,"permalink":"/mid-term-feedback/"}
---

# Mid Term Feedback

(F) Day of the week: Tuesday
Class: IS303
Created Time: January 26, 2021 2:21 PM
Database: Class Notes Database
Date: January 26, 2021 2:21 PM
Days Till Date: Passed
Last Edited Time: June 9, 2021 10:42 AM

Research Problem: what the research is aiming to do, the question it's asking.

The study is to examine if the salary is varied according to the 

How do you get the 100 participants?

I go to Human Resource Department to get a list of staff of 1,000 as a sample frame/population.

- Systematic Random: from 1,000 pick 100 with 10 in between each person.
- Simple Random:
    
    ```jsx
    let list = [...];
    let newList = [];
    for(let i = 0; i < 100; i++) {
    	newList.push(list[random(0, 100)]);
    }
    ```
    
- Proportionate Sampling:
    
    ```jsx
    let list = [Person1, Person2, ...];
    let mList = [];
    let newMList = [];
    let newFList = [];
    let fList = [];
    let malePik = 40;
    let femalePik= 60;
    for(let i = 0; i < list.length; i++) {
    	if(list[i].gender === 'Male') {
    		mList.push(list[i]);
    	}
    	else if(list[i].gender === 'Female') {
    		fList.push(list[i]);
    	}
    }
    for(let i = 0; i < malePik; i++) {
    	newMList.push(mList[i]);
    }
    for(let i = 0; i < femalePik; i++) {
    	newFList.push(fList[i]);
    
    ```
    

Ratio with Ratio: Chi-square test

Ratio with oridinal: compare mean 

Likert Scale: 

1. Not Sure
2. Not Very Worried
3. Worried
4. Very Worried

(Read the paper)

for Weight-mean report