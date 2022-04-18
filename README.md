Pewlet_Hackard_Analysis

Overview

With the data that was already created to provide information about retiring employees, I was tasked to create two more queries. The first was to determine the number of retiring employees per title.  The second was to identify employees who are eligible to participate in a mentorship program.

Results

I needed to create a Retirement Title table to hold all the titles of those born within the retiring age range.

![Screen Shot 2022-04-17 at 7 51 07 PM (2)](https://user-images.githubusercontent.com/93801125/163866466-e49489c0-b5ec-4ab7-8e6f-40369365f6f5.png)

 I also needed to make sure there weren’t any duplicates of people who changed positions and therefor job titles within the company. Two statements/functions I used were:

* DISTINCT ON - statement used to create a table that contains the most recent title of each employee

![Screen Shot 2022-04-17 at 7 51 35 PM (2)](https://user-images.githubusercontent.com/93801125/163866494-226b5b80-ba74-4f4c-b75c-4c9db337c06f.png)

* COUNT() - function used to crate a table that has the number of retirement-age employees by that most recent job title.

Because some people in that demographic may have left or already retired, I also had to make sure I only included current employees.

![Screen Shot 2022-04-17 at 12 37 14 PM (2)](https://user-images.githubusercontent.com/93801125/163866640-43abb2bb-f0c6-4f70-a7ac-ea441a302d48.png)

I also needed to isolate the information that would give me people who were nearing retirement, and are eligible to participate in the mentorship program. 

* Isolating people born in 1965 gave a 10 year time frame to get find people who would like to participate and get the program up and running before their retirement.
* Querying their current title within the company would find qualified mentors for this program, allowing for a swift compilation and return to get the program started. 

Both of these applied to the query allowed me to create a comprehensive list  to present to Pewlet-Hackard as per their request.

![Screen Shot 2022-04-17 at 7 59 27 PM (2)](https://user-images.githubusercontent.com/93801125/163866696-1b5b625d-7a61-49f7-87ac-e89d24584931.png)


Summary

In order to get a better understanding, I created few more query tables to find the impact of both those retiring and those who will mentor, to see if more adjustments need to be done.  I took the oldest year for retirees (1952) and created a query using the tables unique_titles, employees and dept_emp. This allowed me to get the latest instance of their title, as well as their birth_date and to_date so I could limit those that are currently working that were born in 1952.

![Screen Shot 2022-04-18 at 2 08 59 PM (2)](https://user-images.githubusercontent.com/93801125/163866766-b9de23b6-c61c-431a-ac4d-d822139bb4b6.png)

I then created a count table to get the number of retirees in each department.

![Screen Shot 2022-04-18 at 2 12 46 PM (2)](https://user-images.githubusercontent.com/93801125/163866853-2f0a666b-10ab-4b8f-9b84-23441cb70fd4.png)

After which, I created another count table on the mentorship_eligibility table in order to get an idea, whether there will be enough upcoming staff to help fill the shoes of those beginning to retire, and be able to mentor those in the younger generations.

![Screen Shot 2022-04-18 at 1 43 45 PM (2)](https://user-images.githubusercontent.com/93801125/163866879-1358bafa-733b-41c1-be6c-ca4fc210b0eb.png)

I found that with the number of people retiring, who were born in 1952, were mostly in the thousands per department, and that doesn’t include the 4 other years that were in previous queries requested for up and coming retirement age staff.  If they were to implement the Mentorship program, they would be woefully understaffed to fill the shoes of those who retire.  The numbers are below 500 people per department for mentor eligibility.
They will need to include more years for the Mentorship program if it’s to be a success.  
