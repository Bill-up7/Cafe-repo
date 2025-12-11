\# Testing Plan — \<Project Name\>

\#\# 1\. Overview  
This plan describes how this project will be tested.    
It connects requirements, test cases, expected results, and automated testing opportunities into one organized system.

\---

 2\. **Requirements / User Stories**  
List the main user stories your tests must cover.

As a mom I want to be able to play this game on the go, so that I can keep up with my kids busy schedules and still enjoy something for myself.

**Acceptance Criteria 1:**  
The user can play the game internet free  
Game shows ad free

**Acceptance Criteria 2:**  
The user can play the game on mobile device  
Games allows for cell phone and tablet dimensions

**User story 2:**  
As a student I want to pause the game, so that I can continue playing after classes.

**Acceptance Criteria 1:**  
The user should be able to pause the game  
Game shows pause button

**Acceptance Criteria 2:**  
The user can continue playing.  
Games shows Continue where you left off or restart day

**User story 3:**  
As a father I want to be able to unwind while playing so that I can give 100% for my kids.

**Acceptance Criteria 1:**  
The user wants to relax  
Game shows sound options  
**Acceptance Criteria 2:**  
The user wants to unwind  
The game shows a brightness option

**Reflection**:  
Which user story was easiest to write?  
The user story that was easiest to write was user story 1\.

Which one was the hardest?  
The user story that was the hardest to write was user story 3\.

How will these stories help you design your game screens later?  
They will put us into perspective of the users' needs i.e. “on the go” would mean mobile play instead of desktop.

\---

3\. Boundary and Edge Testing

Boundary / Edge 1:  Inventory Limits  

Boundary Input 	               Purpose                                       expected outcome 

| 0 items | This tests the Lowest possible value this can have. The lowest amount of stuff a person can hold is nothing. | Allowed |
| :---- | :---- | :---- |
| 2.0 Items  | This tests the Highest possible value this can hold, One item in each hand so 2 Items total.  | Allowed |
| \-1.0 Items  | This tests to make sure this CANNOT be a taken value since someone cannot hold \-1 items in their hands.  | Prevented |
| 2.5 Items  | This tests to make sure the limit for the two hands is only 2\. In the game we don't want the player holding too many things to make the game easier. | Prevented |

        d) Automation Candidate: Yes, This is repeatable and simple.

    Boundary / Edge 2:  Random Guest orders

  Boundary Input 		    purpose                                      expected outcome

| 0.0 oz  | This is the lowest amount of liquid a cup should accept. | Allowed |
| :---- | :---- | :---- |
| 24.0 oz | This is the highest possible amount of liquid a cup should accept. | Allowed |
| \-0.1 oz | This tests if an amount lower than the lowest accept amount will be accepted, this value should not be accepted. | Prevented |
| 24.1 oz | This tests just above the max value this should hold, this value shouldn't be accepted.  | Prevented |

        d) Automation Candidate: Yes, This is repeatable and simple.

Boundary / Edge 3:  Random Guest orders  
 Boundary Input 		    purpose                                      expected outcome

| I Item | This is the minimum amount of items a guest should be able to order.  | Allowed |
| :---- | :---- | :---- |
| 5 Items | This is the Maximum amount of items a guest should be able to order.  | Allowed |
| \-1 Items | This value is less than the minimum value and should not be an accepted value. | Prevented |
| 6 Items  | This value should not be accepted because iTs above the max amount of items a guest should be able to order.  | Prevented |

   d) Automation Candidate: Yes, This is repeatable and simple.

\---

4\. Automated Test List  
Which tests were candidates for Automation?    
All three tests were candidates for automation.   
For each candidate, which kind of automated testing is recommended:  

repetitive, rule-based, or high-volume?:  
All of these tests should be Rule-Based tests since they follow a defined path of logic and rules, they all can only accept certain values.  
