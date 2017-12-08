# PyCitySchools
In this project, the task is to help the school board and mayor make strategic decisions regarding future school budgets and priorities.
The project is divided in 4 sections
      <ol>
          <li> Summary of all Schools in District
          <li>Passing Rate by School 
          <li> Passing Rate by Grades in School
          <li> Passing Rate by School Size
          <li> Passing Rate by School Type
      </ol>
## Functions Used:
  
  <b><i>reading_file()</i></b> 
    <ol>
      <li>The function is used to read the file, which takes argument path of the .csv file and returns the dataframe
    </ol>
  <b><i>pass_score()</i></b>
     <ol>
        <li>The function pass_score() returns the % of passed students. It take arguments : DataFrame, Subject name :a string(maths or               reading),and    student count which is zero if returning pass count only. 
     </ol>
  <b><i>district_summary()</i></b>
     <ol>
       <li>The function , summarizes the details of the school on district level. It returns dataframe                          with                 summary         
       <li>Thefunction  <b><i>pass_score()</i></b> is called to calculate pass % for each subject
     </ol>
   
   <b><i>passSchool()</i></b>
      <ol>
        <li>The passSchool() is used to calculate summary of Pass rate, based on the school.
        <li>The function groups based on <i>School ID</i>, which is the unique value for each school. 
        <li>Based on the School ID, school_g_df dataframe is created, which contains rows of one school at a time. 
        <li>School's type,budget, pass scores are calculated and appended into a list. 
        <li>The list is then used to create a dataframe, which is then returned.
      </ol>
   
   <b><i>grade_sort()</b></i>
      <ol>
        <li>The grade_sort() is used to calculate summary of Pass rate, based on the school and for each grade. 
        <li>The function groups based on School ID, which is the unique value for each school. 
        <li>Based on the School ID, school_grades dataframe is created, which contains rows of one school at a time. 
        <li>For each school, unique grades are retreived and based on each grade, score and pass % is calculated and appended to the appropriate list. 
        <li>School's type,budget are also calculated and appended into a list. 
        <li>The list is then used to create a dataframe, which is then returned.
      </ol>
  
   <i><b>spending_student()</b></i>
      <ol>
        <li> The function is used to create dataframe based on each school id
        <li> The function calculates total score, and uses pass_score() to get pass count by setting student count=0
        <li> Function also computes average budget per school and retreives type and size of schoo;
        <li> It returns the dataframe with all values
      </ol>
        --Create bins and label them and place to dataframe
        
   <b><i>spending_group()</i></b>
      <ol>
        <li>The function spending_group() uses the dataframe from spending_student(), that takes arguments={dataframe,criteria=column used for grouping}.
        <li>Using the dataframe, the function retrieves scores and calculates average and pass %. Since the score field has sum of score for each school, sum of that value will yield sum for each bin
        <li> Returns the df calculated based on the criteria passed
      </ol>

