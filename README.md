# No_show_appointments
This dataset collects information from 100k medical appointments in Brazil and is focused on the question of whether or not patients show up for their appointment.
 A number of characteristics about the patient are included in each row.

We need to find out what factors are important for us to know in order to predict if a patient will show up for their scheduled appointment?


Questions
What age range do most patients fall in? What is the relationship with show ups?
Does the patient sickness have an impact on their show up(Hypertension, Diabetes, Alcoholism, Handicap)
What neighbourhood has the highest number of patients? what is the impact on the rate of show up?
What proportion of male and female patients showed up for their appointments?

Data Cleaning
Here's a list of what i did

I renamed the columns all to lower characters to enable easy manipulation.
i deleted the PATIENT ID column as it wasnt formatted properly and it wasnt important to the analysis.
I converted the datatype of the APPOINTMENT AND SCHEDULED DAY columns to Datetime format to aid the analysis.

Exploratory Data Analysis
Question 1: What age range does most patient fall in
Here, i got the value counts of all ages in the dataframe. Then i plotted a graph to show the range of age distribution.

What is the relationship between age and show up
This is divided into 3 steps:
I divided the data into two, differentiating information of patients that showed up from those that didnt.
I got the age count(value_counts) from the two data which i divided
I plotted a graph to demonstrate the result

What is the relationship between age and sickness
I had to groupby the patients illnesses and then got the mean ages of patients with such illness. This will help to determine the age group which majorly possess each kind of illness and then plot a bar chart to demonstrate such for each illness.

Question 3: Is there a relationship between different sickness and the rate of show up
Here i grouped by the no_show column, and then i got the mean of all sickness.
This is to demonstrate whether the kind of sickess motivates patients to show up for their appointments. I also plotted a bar chart to visualise the results.

Question 4: What is the proportion of males and females that showed up for their appointment
Here i did 4 things:
I got the value counts of gender in the dataset
I got the value counts of gender in the divided dataset(Those that showed up and those that didnt)
I got the proportion by dividing no.1 from no.2.
I plotted the graph to demonstrate the proportion of both genders that showed up and those that didnt.

Conclusion
Majority of patients are toddlers(ages 0-2) and the elderly (ages 50 and above). This could be as a result of their illness. Its is known that older people tend to have more underlying illnesses. From the data(view chart above), We can see that:
-patients with underlying sickness tend to show up more.
-The Location of the hospital(Neighorhood) also have an impact on whether patients show up as more patients from JARDI Carbim tend to show up for their appointment.
-We can also deduce that more males tend to show up for their appointments although there are more female patients in the hospital.

Therefore, factors to know in order to predict if a patient will show up for their appointment include, gender, age, illness and the hospital location


Limitations
From the dataset given, The dependent variable was not numerical, this made it difficult to check for relationship/ correlation between the other variables.
The data was not sufficient to prove my findings. We cannot draw conclusions based on a one month data. The time period covered in the data is to short to draw accurate conclusions.
