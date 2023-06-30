# Model-Recruitment-Database-System
Database Develop and Design Assignment
 
> Business Rules of Entities

One candidate can only be invited in one and only one interview and one interview can only be attended by one only one candidate. (one-to-one)
One interview needs to answer one and only one test and one test can be answered by one or many interview sections. (one to many)
One employee will send one or many offer letters and one offer letter will be sent by one and only one employee. (one to many)
One employee can come from one and only one department and one department can have one or many employees. (one to many)
One employee can prepare zero or many tests and one test can be prepared by one and only one employee. (zero to many)
One employee can set one or many recruitment job details and one recruitment job details can be set by one and only one employee. (one to many)
One candidate can submit one and only one resume and one resume will be submitted by one and only candidates. (one-to-one)
One resume will be selected for one and only one resume selection and one resume selection selected from zero or many resumes. (zero to many)
One resume selection will be selected by one and only one employee and one employee can select one or many resume selections. (one to many)
One candidate can be selected in one and only one resume selection and one resume selection will select one and only one candidate. (one-to-one)
One candidate can be included in one and only one recruitment job detail and one recruitment job details can include one and only one candidate. (one-to-one)
One agent can promote one or many advertisement details and one advertisement detail will be promoted by one and only one agent. (one to many)
One recruitment job detail can have one or many advertisement details and one advertisement details have one and only one recruitment job detail.  (one to many)  
One employees_id will have zero or one manager_id and one manager_id will have one and only one employees_id. (one to many)


> Attributes of entities with keys

Resume(Resume_ID,Candidates_ID*,Resume_date,Resume_job,Resume_educational,Job_Experience,Resume_selection_ID*, )
Candidates (Candidates_ID, Job_Detail_ID*, Candidates_name, Candidates_gender, Candidates_Job, Candidates_Expected_Salary )
Resume Selection(Resume_selection_ID,Employee_ID*,Candidates_ID*,Resume_ID*,Selection_Description,Selection_Date,Candidates_TestResult,Candidates_InterviewResult) 
Interview( Interview_ID, Candidates_ID*,  Test_ID*, Interviewer_Name, Interview_Date, Candidates_attendance,  Interviewer_Position)
Test ( Test_ID, Employee_ID*, Test_Created_Date, Test_Using_Date)
Offer Letter ( Offer_Letter_ID, Employee_ID*,New_emp_Name, Work_Start_Date, Work_Location, Work_Rules )
Employees ( Employee_ID, Dept_ID*,Job_Position, Employee_name, Employee_salary, Employee_gender, Total_work_year, Manager_ID )
Department ( Dept_ID, Dept_name,  Dept_duty)
Recruitment Job Detail ( Job_Detail_ID, Employee_ID*, Job_Department, Job_Position, Job_Description, Request_Date,  Job_Required_Exp, Job_Required_Edu)
Advertisement Detail (Job_Detail_ID*,Agent_ID*, Date_Start,Advertisement_name,Recruitment_Platform)
Agent ( Agent_ID, Agent_Name, Agent_Position, No_Agent_Team, Advertisement_Exp)

