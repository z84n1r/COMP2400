java cCOMP2400/6240 - Relational Databases
Assignment 1 (SQL)
Due date: 5:00pm, Friday, August 30, 2024
Instructions
 This assignment must be done individually.
Do not share your solutions, or partial solutions, with anyone. Do no post
any idea/partial solution/result related to the assignment on the course
discussion forum, or anywhere else where it can be read by other students.
You may of course ask clarification questions, but make sure you phrase your questions
so that they do not give away what you think the answer or solution is. If you have
technical problems with accessing the moviedb database then you should ask for help.
If you are not sure if a question is ok to post to the forum then ask your tutor during
a lab or come to a drop-in session instead.
You must not use generative tools (ChatGPT or similar) to create your answers to the
assignment. Your answers should be your answers. You can (and indeed should) use
documentation, tutorials and other resources you can find on the web to learn SQL, and
use what you learn to answer the assignment questions. Reference all resources that
you have used in completing this assignment (by writing comments in your submitted
SQL file).
You must submit your solutions through Wattle before the assignment
deadline. There will be an Assignment activity on the course Wattle page where you
should upload your solution file. You can submit more than once, but we can only see,
and will only mark, the last file that you submit.
Late submissions will not be accepted. Submissions made outside the Assignment
activity on Wattle (for example, files sent by email) will not be accepted under any
circumstance. You will be marked on what you have submitted at the time of the
deadline.
 This assignment will count for 18% of the final course mark. There are 9 questions
and each contributes to 2% of the final course mark.
A copy of the moviedb database is available in the PostgreSQL DBMS in the CSIT
lab environment (including via partch). You can connect to the moviedb database by
entering the following in a Terminal:
psql moviedb
 You must submit one file: myqueries.sql containing your solutions to all the ques-
tions. The file must be submitted through Wattle before the due date. Please down-
load the template file from the folder “Assignment 1 (SQL)” on Wattle.
You must enter your queries into the template file, and your submitted file
myqueries.sql must be executable in the given database moviedb.
moviedb=> \i myqueries.sql
You can also test your queries against the moviedb database one by one following
previous lab instructions.
Please write each of your answers below the comment indicating the cor-
responding question (-- Q1 through -- Q9), and leave these comments un-
changed.
 The correctness of queries should not depend on the database state, i.e., the content of
the tables in the database. The current content in moviedb is provided to help you to
get familiar with the database schema. To be fully correct, your SQL queries should
produce the correct answer when tested against other databases that have the same
schema, but different content. Partial marks may be given if a query only has minor
issues.
1
 Please write your SQL queries in a clear, well-formatted style, and use SQL comments
(lines starting with --) to explain your thinking behind the crafting of a complex query.
We will inspect queries that are not fully correct to determine if the flaw is minor (i.e.,
the question is mostly correct, or on the right track) or significant. If your queries
are well documented and easy to 代 写COMP2400 、 SQL
代做程序编程语言read and understand, this increases the chances that
we will be able to find them partially correct. A well-documented and well-reasoned
comments for each question you provide will also increase the chances of partial marks.
Plagiarism, collusion, and the use of disallowed tools will attract academic
penalties in accordance with the ANU guidelines. Every student in this
course is expected to be able to explain and defend any submitted assess-
ment item. The course conveners can conduct or initiate an additional
interview about any submitted assessment item for any student. If there
is a significant discrepancy between the two forms of assessment, this will
be seen as a case of potential academic misconduct.
The Movie Database
The schema of the relational database moviedb is shown in Figure 1.
There are five different categories of awards: movie awards, crew awards, director awards,
writer awards and actor awards. A movie can only win an award after being nominated for
the award.
2
Figure 1: The moviedb schema.
3
Questions
Your task is to write SQL queries that answer the following questions. For each question,
your answer must be a single SQL query (that may contain subqueries). Remember that
your answers should not depend on the example database state. (For example, the answer to
Question 2 below is not “2”; it is an SQL query that evaluates to 2 on the example database,
but may evaluate to different number if the database state is different.)
You must write all your answers into the template file myqueries.sql.
1. How many movies were categorised in the ‘R’ restriction in the USA? List that number.
2. How many writers were born after 1960 (inclusive)? List that number.
3. How many restriction categories each country has? List the countries and the corre-
sponding numbers of restriction categories. Order your result in the ascending order
of the number of restriction categories.
4. How many directors have never directed any action movies (i.e., the major genre of
the movie is action)? List that number.
5. What is the percentage of Australian action movies (i.e., action movies produced in
Australia) among all Australian movies in this database? List the percentage as a
decimal (round to two decimal places).
6. Which movie(s) won the largest number of crew awards in a single year? List their
title(s) and production year(s).
7. How many movies have won at least one award (any award in the databases)? List
that number.
8. Which writers always wrote a movie with other writer(s), i.e., every movie written by
such a writer has at least two writers? List their ids, first and last names. Order your
results in the descending order of their last names.
9. List all the pairs of movies which have won any award in the same year. List the pairs
of their title and production year. Note that the result should not contain duplicated
pairs of title and production year, e.g., (title1, production year1), (title2, produc-
tion year2) and (title2, production year2), (title1, production year1) are considered as
duplicated pairs and your query should only produce one of them in the result. Hint:
in PostgreSQL, the function CONCAT(A1,A2,...,An) can be used to combine selected
attributes.
All done? Well done! Before you submit:
 Check that your myqueries.sql file is syntatically correct SQL, by running it in psql:
moviedb=> \i myqueries.sql
Check that your solution (query) for each question is written below the comment line
indicating the corresponding question (“-- Qi”) in your myqueries.sql file.

         
加QQ：99515681  WX：codinghelp
