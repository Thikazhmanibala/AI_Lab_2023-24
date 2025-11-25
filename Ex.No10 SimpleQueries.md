# Ex.No: 10  Logic Programming –  Simple queries from facts and rules
### DATE: 7/09/25                                                                           
### REGISTER NUMBER : 212222060277
### AIM: 
To write a prolog program to find the answer of query. 
###  Algorithm:
 Step 1: Start the program <br> 
 Step 2: Convert the sentence into First order Logic  <br> 
 Step 3:  Convert the sentence into Horn clause form  <br> 
 Step 4: Add rules and predicates in a program   <br> 
 Step 5:  Pass the query to program. <br> 
 Step 6: Prolog interpreter shows the output and return answer. <br> 
 Step 8:  Stop the program.
### Program:
### Task 1:
Construct the FOL representation for the following sentences <br> 
1.	John likes all kinds of food.  <br> 
2.	Apples are food.  <br> 
3.	Chicken is a food.  <br> 
4.	Sue eats everything Bill eats. <br> 
5.	 Bill eats peanuts  <br> 
   Convert into clause form and Prove that John like Apple by using Prolog. <br> 
### Program:
% --- Knowledge Base ---
% Rule: John likes all kinds of food likes(john, X) :- food(X).
% Facts: foods food(apple). food(chicken).
% Rule: Sue eats everything Bill eats eats(sue, X) :- eats(bill, X).
% Fact: Bill eats peanuts eats(bill, peanuts).

### Output:
<img width="1329" height="745" alt="Screenshot 2025-11-25 183126" src="https://github.com/user-attachments/assets/1582da78-ccb4-494c-8297-395f24b970aa" />


### Task 2:
Consider the following facts and represent them in predicate form: <br>              
1.	Steve likes easy courses. <br> 
2.	Science courses are hard. <br> 
3. All the courses in Have fun department are easy <br> 
4. BK301 is Have fun department course.<br> 
Convert the facts in predicate form to clauses and then prove by resolution: “Steve likes BK301 course”<br> 

### Program:
% courses.pl
% Steve likes all easy courses likes(steve, X) :- easy(X).
% Science courses are hard (included for completeness) hard(X) :- science(X).
% All courses in "Have fun" dept are easy easy(X) :- have_fun_course(X).
% BK301 is a "Have fun" department course have_fun_course(bk301).

### Output:

<img width="1324" height="737" alt="Screenshot 2025-11-25 183233" src="https://github.com/user-attachments/assets/ea54607f-07ed-477d-856a-5456ce99fc27" />


### Task 3:
Consider the statement <br> 
“This is a crime for an American to sell weapons to hostile nations. The Nano , enemy of America has some missiles and its missiles were sold it by Colonal West who is an American” <br> 
Convert to Clause form and prove west is criminal by using Prolog.<br> 
### Program:
% Rule: It's a crime for an American to sell weapons to hostile nations criminal(X) :- american(X), weapon(Y), sells(X, Y, Z),
hostile(Z).
% Facts american(west).
enemy(nono, america). hostile(nono).
missile(m1). owns(nono, m1).
% All missiles are weapons weapon(X) :- missile(X).
% Sales fact sells(west, m1, nono).


### Output:

<img width="1315" height="737" alt="Screenshot 2025-11-25 183317" src="https://github.com/user-attachments/assets/c8510801-bf60-4d23-a0d6-b79a1a526dcb" />


### Result:
Thus the prolog programs were executed successfully and the answer of query was found.
