# Proj004-P02-ML-Models-HR-Analytics-20230505
Predicting Employee Retention (employee stayed or left) profile
<img style="float:left" src="https://i.imgur.com/DWQOJgU.png" width="1500">
<hr>
5 May 2023

<div>
<img style="float: left" src="https://i.postimg.cc/qvZpHzhk/002-Img-Objectives-Draft-2-20220819.png(https://postimg.cc/cvYpQ1Bj)" width="75">
<h2 id="Obj1">Objectives</h2>
<hr>

<h3 style="text-align:justify">The HR department at Salifort Motors wants to take some initiatives to improve employee satisfaction levels at the company. The goals in this project are to analyze the data collected by the HR department and to build <b>a model that predicts whether or not an employee will leave the company</b> or <b> an employee will stay in the company</b>. 

by predicting employees likely to quit, it might be possible to identify factors that contribute to their leaving. Because it is time-consuming and expensive to find, interview, and hire new employees, increasing employee retention will be beneficial to the company.</h3> 
<p style = "font-family: Arial; font-size: 18px">Note: This project's dataset was created for pedagogical purposes and may not be indicative of Salifort Motors.</p>
</div> 

<div class="alert alert-block alert-warning">
<img style="float: left" src="https://i.postimg.cc/kXz8cFqC/005-Img-Yellow-Notes-Draft-1-20220819.png" width="60">
<b style = "font-family: Arial; font-size: 16px">Remember:</b><p style = "font-family:Verdana; font-size:14px"> We must be <b>objective</b> in analyzing the data in order to acquire valuable insights and understand it by collecting, fact checking or challenging the data and other sources. Go to where the data - Genchi Genbutsu attitudes. Data must be <b>Clear, Objective, Valuable, Focus, Agile, Scientific and Timeframe (COV-FAST)</b></p>
    <p style = "font-family:Verdana; font-size:14px">There are other methodologies may be considered like, logistic regression, random forest or neural networking. We can use the same preprocessing dataset and try each options methodologies in seperate notebooks</p>
</div>
    <h3>Methodologies Overview</h3>
<h3>Data Analysis PACE Steps:</h3>
   <ol style="font-family:Verdana; font-size:16px">
    <li><img style="float:left" src="https://i.imgur.com/gIne5bH.png" width="50"> Define (Plan & Analyze - EDA) - PART 1</li> 
    <blockquote>
    <ol>Understand your data in the problem context
        <br>EDA - check model, assumption & select model
    </ol>
    </blockquote>
        <li><img style="float:left" src="https://i.imgur.com/rb8V6X5.png" width="50">Measure (Analyze - EDA)</li>
    <blockquote>
    <ol> EDA - check model, assumption & select model
     </ol>
    </blockquote>
    <li><img style="float:left" src="https://i.imgur.com/J4M3HKM.png" width="50">Analyze (Construct) </li>
    <blockquote>
    <ol>Contruct and evaluate model
     </ol>
    </blockquote>
    <li><img style="float:left" src="https://i.imgur.com/wpcEXQC.png" width="50">Improve (Execute) - interpret model and share the story</li>
    <br>
    <li>Control</li>
  
  <table style="color:black;
           display:fill;
           border-colapse: colapse;
           width: 100%;
           border: 1px solid black;
           border-collapse: collapse;
           border-style: solid;
           border-radius:5px;
           background-color:#5642C5;
           font-size:110%;
           font-family:Verdana;
           letter-spacing:0.5px">
  <h3 style = "text-align:center">Table 1.1. SIPOC Analysis</h3>
  <tr>
    <th>Supplier (S)
    <th colspan="2">Input (I)</th>    
    <th colspan="4">Process (P)</th>
    <th colspan="2">Output (O)</th>
    <th colspan="2">Customer (C)</th>  
  </tr>
    <td>Employee
    <br>Dept Head</td>
    <td colspan="2">Employee
        <ul>
            <li>Believe in your employee - Leadership
            <li>Employee Empowerement - Personal growth
            <li>Work ballance - Flexibility
            <li>Company adequate professional information about company news
            <li>Keep their morale high - Work satisfaction and recognition
            <li>Establish a "healthy environment" - Work relationship
            <li>Financial reward - salary,reward for loyalty and career prospect for high skill (peoplo who upgraded) or by tenure
        </ul></td> 
    <td style="background:LightSkyBlue;text-align:center">Define key group of employees</td>
    <td style="background:LightSkyBlue;text-align:center">Design retention plan</td>
    <td style="background:LightSkyBlue;text-align:center">Assign employees to right plans</td>
    <td style="background:LightSkyBlue">
       Measure KPI, Report and Evaluate </td>
        </td>
    <td colspan="2" style="margin: auto; display:fill; word-wrap: break-word">
        <ul>
            <li>Turnover rate
            <li>Loyalty Reward  
            <li>HR Engagement and Retention Report/Survey
            <li>Employee performance report
            <li>Promotion
        </ul>
    </td>
    <td colspan="2" style="margin: auto; display:fill; word-wrap: break-word">
        <ul>
            <li>Dept Head
            <li>HR
        </ul>
    </td>
 </table>
<div class="alert alert-block alert-warning">
<img style="float: left" src="https://i.postimg.cc/kXz8cFqC/005-Img-Yellow-Notes-Draft-1-20220819.png" width="60">
<b style = "font-family: Arial; font-size: 16px">Note:</b><p style = "font-family:Verdana; font-size:14px">Discussion should be conducted with the process' owner</p>
</div>

## Stakeholder Analysis
<hr>
<span style ="font-family:Verdana; font-size:16px; text-align:justify">In this project we will only be mapping the stakeholders that were mentioned in articles or sources with high impacts and major role to the Salifort Motors project.</span>

<h3 style = "text-align:center">Table 1.2. Stakeholder Analysis</h3>
<table style="color:black;
           display:fill;
           border-colapse: colapse;
           width: 100%;
           border: 1px solid black;
           border-collapse: collapse;
           border-style: solid;
           border-radius:5px;
           background-color:#5642C5;
           font-size:110%;
           font-family:Verdana;
           letter-spacing:0.5px">
  
  <tr>
    <th>Stakeholders</th>
    <th>Role</th>
    <th colspan="2">Involvement</th>    
    <th>Power or Influence (H/M/L)</th>
    <th>Interest (H/M/L)</th>
    <th colspan="2">Engagement</th>  
  </tr>
  <tr>
    <td>HR Director</td>
    <td style = "text-align:left">      
      Project sponsor 
    </td>
    <td colspan="2" style ="text-align:left">
    Makes high-level decisions; serves as team resource
    </td>
    <td style ="text-align:center">
      H 
    </td> 
    <td style ="text-align:center">
      L
    </td>
    <td colspan="2" style ="text-align:left">
      Communicate regularly, but not daily. Ask questions and give updates. 
    </td>
  </tr>
  <tr>
    <td>Dept Head</td>
    <td style = "text-align:left">      
      Project owner 
    </td>
    <td colspan="2" style ="text-align:left">
     <ul>
         <li>advisory role and providing valid information
         <li>Implementation of preventive, diagnosis and treatment measures
         <li>Allow re-export of surplus imported data or any required items to support project
         <li>Formulation of the business requirements
        <li>Formulation and implementation of equitable distribution of execution
        </ul> 
    </td>
    <td style ="text-align:center">
      M 
    </td> 
    <td style ="text-align:center">
      H 
    </td>
    <td colspan="2" style ="text-align:left">
      <ul>
        <li>Informing, mentoring and coaching
        <li>Monitoring the proper implementation of interventions
        <li>Coordination in informing
        <li>Official information reference in the Human Resource Management and
control
        <li>Training and consulting with other related organizations and institutions
        </ul> 
    </td>
  </tr>
  <tr>
    <td>HR Engagement and Retention</td>
    <td style = "text-align:left">      
      Project leader 
    </td>
    <td colspan="2" style ="text-align:left">
     <ul>
      <li>Project-rules making and planning
     <li>Facilitate and synergy in inter-sectorial cooperation
     <li>Identifying problems and providing solutions in the form of executive
       approvals
     </ul> 
    </td>
    <td style ="text-align:center">
      M 
    </td> 
    <td style ="text-align:center">
      H 
    </td>
    <td colspan="2" style ="text-align:left">
       <ul>
      <li>Synergy and strengthening of various capabilities across the team and organization,
       directing and Mobilizing all capacities within the team.
      <li>Lead project from the start to clossing.
      </ul> 
    </td>
  </tr>
  
 </table>
 
 <h3 style = "text-align:center">Figure 1. Employee Stayed or Left Profile</h3>

<div style = "display:fill;
           border-colapse: colapse;
           width: 50%;
           margin: auto"> 
 <img style= "margin:auto" src="https://i.imgur.com/FnJ3frJ.png" width = "600">
 </div>

<h3 style = "text-align:center">Table 1.3. Project Charter</h3>
<table style="color:black;
           display:fill;
           border-colapse: colapse;
           width: 100%;
           border: 1px solid black;
           border-collapse: collapse;
           border-style: solid;
           border-radius:5px;
           background-color:#5642C5;
           font-size:110%;
           font-family:Verdana;
           letter-spacing:0.5px">
  
  <tr>
    <th colspan ="4" style="text-align:center">Project HR Employee Retention</th>
  </tr>
    <tr>
    <th colspan ="4" style="text-align:center">5th May 2023</th>
  </tr>
  <tr>
      <th colspan ="4" style="text-align:center">Document Status: <del>Draft</del> | In Review | <del>Approved</del></th>
  </tr>
  <tr>
      <th colspan ="4" style="text-align:center">Executive Summary</th>
  </tr>
  <tr>
      <td colspan ="4" style="text-align:center">develop a model that predicts employee churn (stayed or left) profile.</td>
  </tr>
  <tr style ="background:LightSkyBlue;text-align:center">
      <td colspan ="2">Business Case</td>
      <td colspan ="2">Problem/Opportunity Statement</td>
  </tr>
 <tr style="text-align:left">
      <td colspan ="2">Through excellent employee retention (also known as retention program or retention management), outstanding performance can not only be maintained, but also promoted and maximized for the company. Based on the <b>there are 17% employees that left the company, approximately 1,991 employees</b> along the years (the year of the resignation or terminatiion not mentioned). Employees who identify with the company feel more responsible. Fluctuation is reduced, absenteeism due to illness is reduced and the quality of work results is higher. All this and many other effects of high employee loyalty increase success and minimize avoidable costs. Another challenge will be the remote work culture and chat-gpt that change the working environment can affect performance. 
          <br><br>
HR estimates for a 200-employee-sized business,with 17% turnover rate that’s 34 departures every year. In compensation terms, the real cost of employee turnover can be upward of 30% and cost up to five times the position’s annual compensation, depending on the type of role, location, etc.
<br><br>
By calculating reasonable estimates for expenses like employee annual salary and daily cost of covering vacancy, that 200-employee business would spend <b>estimated more than $500,000 in avoidable costs</b>. 
</td>
      <td colspan ="2"><em>In this project</em> we establish a model to find ways to<b> predict profile that likely to churn. </b>
<br><br>The goal of selective employee retention is to identify and retain people who are relevant to success. So-called "top performers" typically have the following roles:
<ol>
<li>Performers (high and top performers)
<ul> <b>Based on the data high salary around 8% and were not disproportionately comprised of higher-graded employees.</b> 
    <li>Potential carriers (promising talents)
    <li>Holders of positions of high strategic importance
    <li>Experts with expertise or skills that are rarely available on the market
</ul>
<li>Mid-performers", can also be developed into "top performers" with good personnel and management work. <b>Based on the data medium salary around 44% and were not disproportionately comprised of medium-graded employees.</b>
<li>"Low-performers" are resistant to measures for employee retention and boycotting, often even measures to improve employee satisfaction or retention. That is why the (main) focus of all measures for employee retention is on top and mid-performers. <b>Based on the data high salary around 48% and were not disproportionately comprised of lower-graded employees.</b>
          </ol>
     </td>
  </tr>

 <tr style ="background:LightSkyBlue;text-align:center">
      <td colspan ="2">Goal Statement</td>
      <td colspan ="2">Deliverables (Key Results)</td>
 </tr>
 <tr style="text-align:left">
      <td colspan ="2">Primary metric:
     <ul>
         <li>Employee retention Rate - build a model that predict employee who stayed or left. 
     </ul>
     Secondary Metric:
     <ul>
         <li>Average monthly hours
         <li>Evaluation
     </ul>
     </td>
      <td colspan ="2">Primary Key Results:
     <ul>
         <li>Increase retention rate - reduce 50% of people leaving the company (the data provide the employee who stayed and left).
     </ul>
     Secondary Key Results:
     <ul>
         <li>Number of project
         <li>Top and Medium evaluation distribution
     </ul>
     </td>
  </tr>
 
 <tr style ="background:LightSkyBlue;text-align:center">
      <td colspan ="2">Benefits, Cost, and Budget</td>
      <td colspan ="2">Scope and Exclusion</td>
 </tr>
 <tr style="text-align:left">
      <td colspan ="2">Benefits:
     <ul>
         <li>Reducing 50% of employees (for 200 employees) leaving the company estimated more than $250,000 in avoidable costs.
         <li>Increase tenure
         <li>Increse satisfaction
         <li>Increase top performer
     </ul>
     Costs:
     <ul>
         <li>Recruitment cost
         <li>Training cost   
     </ul>
     Budget Needed:
           <span>TBD</span>
     </td>
      <td colspan ="2">In-Scope:
     <ul>
         <li>All department
         <li>Top and medium evaluation
         <li>Full time
     </ul>
     Out-of-Scope:
     <ul>
         <li>Part Time or contract
         <li>Lean measure such as ,Fastest recruitment etc.
     </ul>
     </td>
  </tr>   
 
 <tr style ="background:LightSkyBlue;text-align:center">
      <td colspan ="2">Project Team</td>
      <td colspan ="2">Measuring Success</td>
 </tr>
 <tr style="text-align:left">
      <td colspan ="2"> 
     <ul>
         <li>Sponsor: Laura, Director of HR
         <li>Owner: Washington, Operations Manager
         <li>Leader:Joko, Senior   
             HR Engagement and Retentioan
         <li>Member: Denzel, Data Analysis Manager, jennifer, Senior Data Analyst, Wahyu Senior Data Analyst   
     </ul>
     </td>
  
  <td colspan ="2">Deliverables after solutions implementation:
     <ul>
         <li>Increase retention rate and turnover rate
         <li>Increase employee engagement and retention survey
         <li>Increase employee performance    
     </ul>
  </td>
  </tr>
  </table>
  
  <hr>
<table style="color:black;
           display:fill;
           border-colapse: colapse;
           width: 100%;
           border: 1px solid black;
           border-collapse: collapse;
           border-style: solid;
           border-radius:5px;
           background-color:#5642C5;
           font-size:110%;
           font-family:Verdana;
           letter-spacing:0.5px">
            
  <h3 style = "text-align:center">Table 2. Machine Learning Model Feature Importance </h3>
  <tr>
    <th>Decision Tree (2)</th>
    <th>Random Forest (2)</th>    
    <th>XG Boost (2)</th>
  </tr>
  <tr style = "text-align:center">
      <td><img style= "margin:auto" src="https://i.imgur.com/geNGequ.png" width = "600"></td>
      <td><img style= "margin:auto" src="https://i.imgur.com/X3FKKnN.png" width = "600"></td>
      <td><img style= "margin:auto" src="https://i.imgur.com/QParrbM.png" width = "600"></td>
  </tr>
  </table>
  
  <img style="float:left" src="https://i.imgur.com/wpcEXQC.png" width="50"><div style = "font-family: Arial; font-size: 16px">
    Execute</div>

## Conclussion
<hr>

<div class="alert alert-block alert-success" style="font-family:verdana; font-size:14px">

Logistic Regression
<br><br>
The logistic regression model achieved precision of 81%, recall of 84%, f1-score of 81% (all weighted averages), and accuracy of 84%, on the test set.
<br><br>
Tree-based Machine Learning
<br><br>
After conducting feature engineering, the decision tree model achieved AUC of 96%, precision of97%, recall of 92%, f1-score of 94%, and accuracy of 98%, on the test set. The random forest and xgboost modelslightly underperformed the decision tree model
<br>    
The models and the feature importances extracted from the models confirm that employees at the company are overworked. 
<br><br>
To retain employees, the following recommendations could be presented to the stakeholders:
<br><br>
<ol>
<li> Limit the number of projects that employees can work on.
<li> Promote employees who have great evaluation results and have been for atleast four years, or conduct further investigation about why four-year tenured employees are so dissatisfied. 
<li> Give reward to employees for working longer hours who have brought significant improvements, working collaboratively executing in a project(s) or consider that employee can exchange their overtime with more paid leave of holiday or vacation. 
<li> Ensure that employee has understood the overtime policy, check and if the employee has been given information accordingly.
<li> Consider proprtionate score on employee's evaluation towards employee who have great impact and team enabler as not due to the amount of works as aligned to point 2.
<li> Important to have team or department as well in company-wide discussion regarding the work culture. Open consultation from HR to address together with department head or related parties for company's improvement specially for the top talent and medium employee.
<li> Set a features that can elaborate satisfaction level similar to filter medium and top talent employees (good performance).
<br><br>
Next Steps
<br><br>
It may be justified to still have some concern about data leakage. It could be prudent to consider how predictions change when `last_evaluation` and employee satisfaction is removed from the data. It's possible that evaluations aren't performed very frequently, in which case it would be useful to be able to predict employee retention without this feature. <b>It's also possible that the evaluation score determines whether an employee leaves or stays, in which case it could be useful to pivot and try to predict performance score. The same could be said for satisfaction score.</b>. After setting the features, it may be more productive to focus on the medium to the top talent employee which possibility has the most satisfied score.
<br><br>
We can also see the cluster from this model which k = 15.
</div>
  
<h3 style = "text-align:center">Figure 2. Fishbone Diagram Employee Churn (Stayed or Left) Profile</h3>

<div style = "display:fill;
           border-colapse: colapse;
           width: 50%;
           margin: auto"> 
    
<img style= "margin:auto" src="https://i.imgur.com/my21RZl.png" width = "6000">

</div>
