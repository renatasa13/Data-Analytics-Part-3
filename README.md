# Data-Analytics-Part-3

# 1. Dataset
- This data set contains booking information for a city hotel and a resort hotel and includes information such as when the booking was made, length of stay, the number of adults, children, and/or babies, and the number of available parking spaces, among other things. All personally identifying information has from the data.

# 1.1 Data Understanding
- This data set contains booking information for a city hotel and a resort hotel and includes information.
- Source Data: https://www.kaggle.com/jessemostipak/hotel-booking-demand
- The dataset has 32 column and 119390 rows.
- Data Dictionary:
- hotel : Hotel categories (Resort Hotel and City Hotel)
- is_canceled : Value indicating if the booking was canceled (1) or not (0)
- lead_time : Number of days that elapsed between the entering date of the booking into the PMS and the arrival date
- arrival_date_year : Year of the arrival date
- arrival_date_month : Month of arrival date
- arrival_date_week_number : Week number of year for arrival date 
- arrival_date_day_of_month : Day of arrival date
- stays_in_weekend_nights : Number of weekend nights (Saturday or Sunday) the guest stayed or booked to stay at the hotel
- stays_in_week_nights : Number of week nights (Monday to Friday) the guest stayed or booked to stay at the hotel
- adults : Number of adults
- children : Number of children
- babies : Number of babies
- meal : Type of meal booked. Categories are presented in standard hospitality meal packages (Undefined/SC - no meal package, BB - Bed & Breakfast, HB - Half board, and FB - Full Board)
- country : Country of origin
- market_segment : Market segment designation (TA - Travel Agents and TO - Tour Operators)
distribution_channel : Booking distribution channel (TA - Travel Agents and TO - Tour Operators)
- is_repeated_guest : Value indicating if the bookings name was from a repeated gest (1) or not (0)
- previous_cancellations : Number of previous bookings that were cancelled by the customer prior to the current booking
- previous_bookings_not_cancelled : Number of previous bookings not cancelled by the customer prior to the current booking
- reserved_room_type : Code of room type reserved. 
- assigned_room_type : Code for the type of room assigned the the booking.
- deposit_type : Indication on if the customer made a deposit to guarantee the booking (No Deposit, Non Refund, and Refundable)
- booking_changes : Number of changes/amendments made to booking from the moment the booking was entered on the PMS until the moment of check in or cancellation
- agent : ID of the travel agency that made the booking
- company : ID of the company/entity that made the booking or responsible for praying the booking
- days_in_waiting_list : Number of days the booking was in the waiting list before is was confirmed to the customer
- customer _type : Type of booking (contract, group, transient, and transient-party)
- adr : Average daily rate as defined by dividing the sum of all lodging transactions by the total number of staying nights
- required_car_parking_spaces : Number of car parking spaces required by the customer
- total_of_special_requests : Number of special requests made by the customer
- reservation _status : Reservation las status (canceled, check out, and no show)
- reservation _status_date : Date at which the last status was set.

# 1.2 Data Preparation 
- Code used:
- Python version: 3.11.4 
- Packages: Pandas, Numpy, Matplotlib, and Seaborn.

# 1.3 Data Profiling
- Load the Data
- Check the Data
- After checking the data, there are columns that have missing values, there are  children, country, agent and company columns. Therefore, there is a need for a data cleaning process

# 1.4 Data Cleansing
- Duplicate data can have a significant impact on the data cleansing process. Duplicate data cted.an skew prediction results, contaminate the training data with the test data, or vice versa.
- Therefore, it is important to check and remove duplicates before performing any data analysis or modeling.
- The data set is not clean. We have 4 features with missing values.
- The data in the Age column is in numerical form with non-normal data distribution or skewness. Therefore, missing values can be handled by replacing them with medians.
- The data in the Country column is in categorical (string) form. Therefore, missing values can be handled by replacing them with the mode. 
- The data in the Agent column is in categorical form (ID of the travel agency that made the booking). Therefore, missing values can be handled by replacing them with the mode.
- The data in the Company column have missing value and because the percentage of null values is greater than 50, the column must be removed or deleted.

# 1.5 Exploratory Data Analysis and Data Storytelling
-  ![WhatsApp Image 2023-10-28 at 10 26 14_3e41e044](https://github.com/Nirmalafauzhia/Data-Analytics-Part-3/assets/146448514/ab4e5bc5-9d78-4f35-992a-4caff34cfd72)
- From this chart, it can be seen that there was more than double bookings were made in 2016, compared to the previous year, but decrease in the number of visitors coming from 2016 to 2017 for each hotel. There was a decrease of around 42.5% in Resort Hotels compared to the previous year, while in City Hotels there was a decrease of around 42.9% from the previous year. This decline figure almost reached half of the previous year's visits. Therefore, hotels need to make efforts to increase the number of visitors in the following year, for example by providing attractive discounts and promotions.
  
- ![WhatsApp Image 2023-10-28 at 10 25 10_dde16195](https://github.com/Nirmalafauzhia/Data-Analytics-Part-3/assets/146448514/e24c1cfd-a2c1-4270-9755-e9bd7adf6ff6)
-  From this chart, there was a trend of decreasing number of customers at the beginning and end of the year. However, there was a spike in the number of customers between June and August of 33% at City Hotels and more than 77% at Resort Hotels, but fell in the following months. Therefore, efforts are needed to increase the number of visits, such as promotions by offering certain attractive facilities at the beginning and end of the year, as well as providing more rooms between June and August with good facilities and services to maintain customer loyalty so that there is no decline. which was quite extreme in the following month.

- ![WhatsApp Image 2023-10-28 at 10 18 54_3db1665d](https://github.com/Nirmalafauzhia/Data-Analytics-Part-3/assets/146448514/9df5e745-841d-44f4-bae8-c316cb6b50da)
- Based on data, it can be seen that there are 2 types of hotels, namely city hotels and resort hotels and from all visitors it can be seen that more people choose to stay at city hotels at 61% of all visitors and for resort hotels themselves there are 39% of all visitors who choose to stay at there.
  
- ![WhatsApp Image 2023-10-28 at 13 12 04_c9026920](https://github.com/renatasa13/Data-Analytics-Part-3/assets/93513745/c75c3fc1-2469-483d-8c53-1b0e7df19f06)
- Based on data, 77% of visitors ordered BB (Bed & Breakfast) meals, while 10% of visitors ordered SC (Self-Catering) or HB (Half board (breakfast and one other meal – usually dinner)), the rest ordered full board, and there were visitors who did not order food.
  
- ![image](https://github.com/renatasa13/Data-Analytics-Part-3/assets/93513745/47e81b13-2383-402d-848f-842b68fe5244)
- Based on this data, it shows the number of hotel orders every month. Based on this, August is the month with the most visitors (12.8%) and January is the month with the fewest visitors (5.3%), January is only half as many as August. So hotels must pay attention to what must be done so that visitors can increase.

# 2. Responsible analytics practices
- The meaning of "Responsible analytics practices" are a set of principles and guidelines that organizations should follow to ensure that they are using data in a way that is ethical, fair, and transparent. These practices are important to protect the privacy and rights of individuals, and to build trust with customers and stakeholders.

# 2.1 Data privacy laws and best practices
- The meaning of" Data privacy laws and best practices" are Data privacy laws, also known as data protection laws or regulations, are legal frameworks that govern the collection, use, processing, storage, and sharing of personal data. These laws are designed to protect individuals' privacy by ensuring that organizations and entities handle their personal information responsibly and securely. Data privacy best practices are a set of guidelines and strategies that organizations and individuals can follow to protect personal information and comply with data privacy laws. These practices aim to ensure that data is handled with care, respecting the privacy rights and expectations of individuals. Here some keys point of Data privacy laws and best practices:

1. Data Protection Regulation (GDPR)
- Definition: General Data Protection Regulation (GDPR) is a regulation in the European Union that sets out strict rules for the collection and use of personal data. The GDPR applies to all organizations that process personal data of individuals located in the European Union, regardless of where the organization is located.
- Example: A company that collects data from customers in the European Union must comply with the GDPR. This means that the company must obtain consent from customers before collecting their data, and it must provide customers with access to their data and the ability to correct any inaccuracies.
- Image example: ![WhatsApp Image 2023-10-27 at 19 42 14_fb188c33](https://github.com/Nirmalafauzhia/Data-Analytics-Part-3/assets/146448514/26c08dcb-d77a-4e7d-96e1-6668398ad954)


2. Family Educational Rights and Privacy Act (FERPA)
- Definition: Family Educational Rights and Privacy Act (FERPA) is a US law that protects the privacy of student education records. FERPA gives parents and students certain rights over their educational records, including the right to access, correct, and delete their records.
- Example: A school district that collects data from students must comply with FERPA. This means that the school district must obtain consent from parents before collecting data from their students, and it must provide parents with access to their students' data and the ability to correct any inaccuracies.
- Image example: ![WhatsApp Image 2023-10-27 at 19 42 14_3ec1d3bc](https://github.com/Nirmalafauzhia/Data-Analytics-Part-3/assets/146448514/43a9a7e2-5a8b-4b76-873d-33c64e73905d)

3. Health Insurance Portability and Accountability Act (HIPAA)
- Definition: Health Insurance Portability and Accountability Act (HIPAA) is a US law that protects the privacy of health information. HIPAA applies to healthcare providers, healthcare insurance companies, and other organizations that handle health information.
- Example: A doctor's office that collects data from patients must comply with HIPAA. This means that the doctor's office must obtain consent from patients before collecting their data, and it must protect the data from unauthorized access or use.
- Image example:
- ![WhatsApp Image 2023-10-27 at 19 42 14_6455942a](https://github.com/Nirmalafauzhia/Data-Analytics-Part-3/assets/146448514/55329a2b-0074-4236-abcd-28dbcd86ded6)

4.Institutional Review Board (IRB)
- Definition: Institutional Review Board (IRB) is a committee that reviews research proposals to ensure that they protect the rights and welfare of human subjects. IRBs are required to review research proposals that involve human subjects, including research that uses personal data.
- Example: A university that is conducting research on student behavior must obtain approval from an IRB before collecting data from students. This ensures that the research is conducted in a way that protects the privacy and rights of the students.
- Image example:
- ![WhatsApp Image 2023-10-27 at 19 42 14_5c9a6fe7](https://github.com/Nirmalafauzhia/Data-Analytics-Part-3/assets/146448514/bf2e206a-6577-4c06-a011-27bdbe070e71)

5.Payment Card Industry Data Security Standard (PCI DSS)
- Definition: Payment Card Industry Data Security Standard (PCI DSS)is a set of security standards for organizations that process credit and debit card payments. The PCI DSS requires organizations to implement certain security measures to protect credit and debit card data from unauthorized access, use, or disclosure.]
- Example: A merchant that accepts credit and debit cards must comply with the PCI DSS. This means that the merchant must implement security measures to protect the credit and debit card data that it collects from customers.
- Image example: ![WhatsApp Image 2023-10-27 at 19 42 15_c59328df](https://github.com/Nirmalafauzhia/Data-Analytics-Part-3/assets/146448514/f639bdd3-c5ee-4c18-a1fa-3e3fa8076f51)

# 2.2 Describe Best Practices for Responsible Data Handling: 
- The meaning of "Describe best practices for responsible data handling" is to explain the best practices in responsible data handling. These best practices encompass the most effective and ethical ways of collecting, storing, securing, interpreting, and using data. The purpose of these practices is to protect individual privacy, ensure data security, prevent data misuse, and ensure that data is used in a legal and beneficial manner. This involves compliance with applicable data privacy laws and ethical guidelines in data usage. Here some keys point of Describe Best Practices for Responsible Data Handling:

1. Methods of Handling PII (Personally Identifiable Information):
- Definition: PII refers to information that can be used to identify individuals, such as names, addresses, ID numbers, or phone numbers. Best practices involve strict protection of PII, including data encryption when stored and transmitted. 
- Example: E-commerce Shopee should encrypt customer information, such as social security numbers, when it's stored in their databases. Access to this data should be restricted to authorized personnel only. 
- Image example:
- ![WhatsApp Image 2023-10-27 at 19 42 15_4fe32765](https://github.com/Nirmalafauzhia/Data-Analytics-Part-3/assets/146448514/aa0f2e93-3fa7-4186-8acc-deb02c3eaafc)

2. Securing Data:
- Definition: Data security involves using encryption, firewalls, limited access, and active monitoring to protect data from unauthorized access.
- Example: MyEduSolve should use encryption to protect sensitive financial data during transmission, ensuring that even if intercepted, the data remains confidential and secure.
- Image example:
- ![WhatsApp Image 2023-10-27 at 19 42 15_55849cc4](https://github.com/Nirmalafauzhia/Data-Analytics-Part-3/assets/146448514/5a32fd56-46d6-4ac9-ac33-cb370ca7e2bb)
  
3. Protecting Anonymity Within Small Data Sets:
- Definition: When working with small datasets that may have the potential to identify individuals, it's essential to carefully design the data to maintain anonymity.
- Example: Researchers working with a small survey dataset might aggregate responses for demographic information, making it harder to identify any single participant.
- Image example: 
- ![WhatsApp Image 2023-10-27 at 19 42 16_b1e9f3b1](https://github.com/Nirmalafauzhia/Data-Analytics-Part-3/assets/146448514/d15f7d9f-e8fa-4856-966b-5f4500543462)
- ![WhatsApp Image 2023-10-27 at 19 42 16_90ec1844](https://github.com/Nirmalafauzhia/Data-Analytics-Part-3/assets/146448514/ab0b6c23-1403-4ee3-a37c-4d52605d6c0a)
  
4. Importance of Anonymizing Data:
- Definition: Anonymization is the process of removing information that could identify individuals from data. This is important for safeguarding privacy and complying with regulations such as GDPR.
- Example: A Data Analytics before sharing healthcare records for research purposes, all personally identifiable information, like names and addresses, should be removed to protect patients' privacy.
- Image example:
- ![WhatsApp Image 2023-10-27 at 19 42 16_8a39cca1](https://github.com/Nirmalafauzhia/Data-Analytics-Part-3/assets/146448514/0550809a-7038-49e6-8a33-48eed31a884e)
- ![WhatsApp Image 2023-10-27 at 19 42 17_34a5edd0](https://github.com/Nirmalafauzhia/Data-Analytics-Part-3/assets/146448514/6845c546-c02e-4569-b173-373b3ef5b1e6)

5. Trade-Offs When Balancing Interpretability and Accuracy:
- Definition: There are situations where you must choose between maintaining data interpretability and achieving higher accuracy. For example, very complex machine learning models may offer high accuracy but are harder to interpret.
- Example: A Data Analytics or Data Scientist In credit scoring, a simple model that uses just a few variables may be more interpretable, even if it's less accurate, while a complex neural network might have higher accuracy but is less transparent.
- Image example: ![WhatsApp Image 2023-10-27 at 19 42 15_88f2496c](https://github.com/Nirmalafauzhia/Data-Analytics-Part-3/assets/146448514/744b4ba2-41a5-4b7c-817b-e2a2929a6e26)
  
6. Shortcomings of Making Population-Level Generalizations with Limited Sample Data:
- Definition: When making generalizations about an entire population based on a limited sample, there are risks of error. The sample may not fully represent the variation within the population.
- Example: the share of U.S. adults who said they had received at least one COVID-19 vaccine dose by June 2021 was roughly two-thirds based on data from both the Centers for Disease Control and Prevention (66%) and Center polling (67%). While not perfect, this level of accuracy is usually sufficient for getting a meaningful read of the public’s mood on key issues.
- Image example: ![WhatsApp Image 2023-10-27 at 19 42 17_a351c114](https://github.com/Nirmalafauzhia/Data-Analytics-Part-3/assets/146448514/ea0b84ce-9820-4928-b196-7ecfaf711a94)

# 2.3 Given a scenario, describe types of bias that affect collection and interpretation of data
- It is important to recognize and address these biases in data collection and interpretation to ensure the integrity and validity of the findings. This can involve careful study design, transparent methodology, and rigorous data analysis techniques to mitigate bias as much as possible.

1. Confirmation bias 
- (is the tendency to search for, interpret, favor, and recall information in a way that confirms or supports one's existing beliefs or hypotheses)
- Definition: Confirmation bias is a type of cognitive bias that occurs when we only seek out. information that confirms our existing beliefs, while ignoring or downplaying information that contradicts them.
- Example: A person who believes that climate change is not real may only seek out information from sources that support their belief, while ignoring or downplaying information from sources that contradict it.
- Image example: ![WhatsApp Image 2023-10-27 at 19 42 17_e1e00e23](https://github.com/Nirmalafauzhia/Data-Analytics-Part-3/assets/146448514/6cd37511-7c3a-4080-a01c-dbd6a1a1e240)

2. Human cognitive bias
- (is a mental shortcut that can lead to errors in judgment. Cognitive biases are based on our experiences, emotions, and assumptions.)
- Definition: Human cognitive bias is a mental shortcut that can lead to errors in judgment. Cognitive biases are based on our experiences, emotions, and assumptions.
- Examples: Availability bias: The tendency to give more weight to information that is more readily available. Anchoring bias: The tendency to rely too heavily on the first piece of information we receive when making a decision. Representativeness bias: The tendency to judge the likelihood of an event based on how similar it is to other events we are familiar with.
- Image example: ![WhatsApp Image 2023-10-27 at 19 42 18_ba161576](https://github.com/Nirmalafauzhia/Data-Analytics-Part-3/assets/146448514/86b51a39-ed55-4b33-8dfc-dabdb2e09b19)

3. Motivational bias 
- (is a type of bias that occurs when our motivations influence our collection or interpretation of data.)
- Definition: A tendency to collect or interpret data in a way that supports one's desired outcome.
- Example: A pharmaceutical company may design a clinical trial in a way that is biased in favor of its new drug. For example, the company may recruit participants who are more likely to respond favorably to the drug, or use a dosage that is higher than what is typically used in real-world practice.
- Image example: ![WhatsApp Image 2023-10-27 at 19 42 18_7353b753](https://github.com/Nirmalafauzhia/Data-Analytics-Part-3/assets/146448514/e134fe2e-87f6-4434-99b6-17e8aa0f2adf)

4. Sampling bias 
- (occurs when the sample of data collected is not representative of the population that it is intended to represent.)
- Definition: Sampling bias occurs when the sample of data collected is not representative of the population that it is intended to represent.
- Examples:The child is only scooping out the red jelly beans. This means that the sample of jelly beans that the child collects will not be representative of the entire bowl of jelly beans, but will be biased towards red jelly beans. Sampling bias is a serious problem in research because it can lead to inaccurate results. It is important to be aware of sampling bias and to take steps to avoid it when designing and conducting research studies.
- Image example: ![WhatsApp Image 2023-10-27 at 19 42 19_3de8a22a](https://github.com/Nirmalafauzhia/Data-Analytics-Part-3/assets/146448514/d867e049-8771-4d8c-a907-300ee5ba1396)

5. Selecting visualizations/data representations to avoid bias
- Definition: When selecting visualizations and data representations, it is important to be aware of the potential for bias. Some visualizations and data representations can be more misleading than others. Here are some tips for selecting visualizations and data representations to avoid bias: Use visualizations that are accurate and easy to understand. Avoid using visualizations that are misleading or manipulative. Be transparent about how the data was collected and analyzed. Use multiple visualizations to represent the same data, and compare the results.
- Example: Using a bar chart to compare two groups of people is a good way to avoid bias, because bar charts are easy to understand and do not distort the data. However, using a pie chart to compare the same two groups could be misleading, because pie charts can make small differences appear larger.
- Image example: ![WhatsApp Image 2023-10-27 at 19 42 19_adaced78](https://github.com/Nirmalafauzhia/Data-Analytics-Part-3/assets/146448514/883eb8e9-e091-465f-9446-37a96f0827f3)
