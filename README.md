# SepsisAnalysis
# SepsisProject_Tableau
In the U.S., nearly 1.7 million people develop sepsis, and 270,000 people die from it each year. Over one-third of individuals who pass away in U.S. hospitals have sepsis. Globally, approximately 30 million people develop sepsis, resulting in 6 million deaths annually. Managing sepsis in U.S. hospitals costs $24 billion annually, which accounts for 13% of U.S. healthcare expenses. A majority of these costs are associated with patients who develop sepsis during their hospital stay. The developing world faces additional expenses for sepsis management and an increased risk of adverse outcomes. Overall, sepsis is a significant public health issue, leading to substantial morbidity, mortality, and healthcare expenses. The reliable and early identification of sepsis is often challenging due to its syndromic nature, contributing to delays in treatment.

![SIRS_flowchart](https://github.com/KrishnaVidja/SepsisProject_Tableau/assets/106781881/ab3ec548-d1e1-4820-bfdc-0e23bc0d5fa2)
### Objective
Identify a patient's risk of sepsis and make a prediction of sepsis for every hourly time window in the patient’s clinical record.

### About Data
The Sepsis project involved the analysis of a vast dataset comprising over 1.5 million data points from more than 40,000 ICU patients. This dataset included hourly records, demographic information, and the presence of a sepsis label indicating the hour of sepsis diagnosis. Additionally, the project included the bloodwork test results of 34 key biomarkers associated with sepsis.

### Demographic Analysis
Utilized Calculated Fields, Level of Details Expressions(LOD) with the "FIXED" keyword to accurately classify patients into sepsis, non-sepsis, and onset sepsis

![Screenshot 2023-10-10 131119](https://github.com/KrishnaVidja/SepsisProject_Tableau/assets/106781881/4cbce868-4447-4f68-8e70-24c0b4c27867)
![Screenshot 2023-10-10 141607](https://github.com/KrishnaVidja/SepsisProject_Tableau/assets/106781881/0b010000-ac1e-439c-bc77-0937a5ad20b7)
* Dashboard displays patient distribution: 98.02% without sepsis and 1.98% with sepsis.
* The primary goal is swift diagnosis and treatment for the non-sepsis patients (98.02%) to prevent sepsis development.
* These patients were primarily admitted due to infections or SIRS.
* Demographic analysis factors in age and gender, revealing a heightened sepsis risk in the 60-80 age group, with males at higher risk than females.
  
### Analysis of Mean Arterial Pressure and Blood Pressure in Admitted Patient
![Screenshot 2023-10-10 141737](https://github.com/KrishnaVidja/SepsisProject_Tableau/assets/106781881/0c4ee4b0-d36a-4175-89d3-ce26a8cb59e0)
*The difference in MAP and BP between sepsis and non-sepsis patients is most significant in those with elevated BP, with a 30 mmHg higher MAP in sepsis patients compared to non-sepsis patients
* Sepsis-associated increases in MAP and BP are likely due to the inflammatory response, leading to vasoconstriction and increased cardiac output.
* Elevated MAP and BP in sepsis patients can increase the risk of stroke, heart attack, and kidney failure, necessitating careful monitoring and management.
  
### Acidosis in Sepsis Patient
![Screenshot 2023-10-10 141821](https://github.com/KrishnaVidja/SepsisProject_Tableau/assets/106781881/f1bec77f-1b54-4af7-8f42-eaf541c59aab)
* This dashboard provides important insights into the relationship between sepsis and MAP and BP.
* Sepsis is associated with significant increases in MAP and BP, especially in patients with elevated BP.
* The increase in MAP and BP is most pronounced in the first 24 hours after admission.
* Patients with sepsis and elevated BP are at particularly high risk of developing complications such as stroke, heart attack, and kidney failure.

### SIRS (Systemic inflammatory response syndrome) Analysis
![SIRS_2 sunburst](https://github.com/KrishnaVidja/SepsisProject_Tableau/assets/106781881/c74d231a-6da3-4154-a89c-7436c6e10162)
* we understand that there are 22% of total patients in this data set got admitted with SIRS symptoms. It is hard to find the time of trigger since many patients may not keep track of the time when they start showing each symptom.
* Over 55% of patients exhibit high heart rates and increased metabolic stress (RR). Around 2% of patients are admitted with Acute-phase Reactions (high temp & high WBC), which can be fatal. Within the first hour of admission, many patients show more than 2 SIRS symptoms, requiring immediate medical attention.
* The percentage of new SIRS patients drops below 3% after 10 hours of admission, and it continues to decrease over time.
![Screenshot 2023-10-10 143804](https://github.com/KrishnaVidja/SepsisProject_Tableau/assets/106781881/305e538e-2d31-428b-b1c1-f977b4c4d09f)
* Utilized calculated fields, Level of Details Expressions(LOD) with the "FIXED" keyword to specifically target and identify the SIRS trigger hour for patients.
* Implemented dummy axes technique and formatted cell colors to effectively highlight abnormal test results, enabling quick identification and analysis.
* Added URL actions to implement email alerts, ensuring the prompt notification of responsible hospital staff when patients meet the pre-alert criteria, facilitating timely attention and response.

### Septic Shock Analysis
![Screenshot 2023-10-10 143430](https://github.com/KrishnaVidja/SepsisProject_Tableau/assets/106781881/6dfab5bb-dda7-48ae-8c25-9139ec28e4af)
* Septic shock is a severe, life-threatening condition with a low survival rate. It depends on your health, age, treatment, and organ failure. Without treatment, most don't survive. With it, about 30-40% can make it.
* Criteria: SBP<90 mm Hg, MAP<60 mm Hg , Resp ≥ 22 breaths/mins,Lactate>2 mmol/L.
* There were 473 cases of septic shock, and it was more common among individuals aged 71 to 80. This risk was particularly notable in both men and women aged 61 to 70.
![Screenshot 2023-10-10 143536](https://github.com/KrishnaVidja/SepsisProject_Tableau/assets/106781881/0673226a-9229-4183-b99a-0092c6e3e71c)
* This text chart illustrates the analysis of the septic shock range over hours. It identifies biomarkers that have surpassed threshold values, potentially causing septic shock in patients. For instance, when Lactate exceeds 2, it poses a risk and can trigger septic shock.

### Data Driven impact.....
This project demonstrates the significant impact of data analysis on patient care. By identifying crucial risk factors and sepsis-related patterns, we empower doctors to detect and treat this severe condition proactively, potentially saving lives and reducing hospital stays. This not only improves patient outcomes but also enhances ICU operational efficiency by up to 30%.
