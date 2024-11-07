# IndiaAI
IndiaAI CyberGuard AI Hackathon

# **Voice Call Recording Classifier for Crime Categorization**

## **Project Overview**
This project involves building a Natural Language Processing (NLP) classifier that automatically categorizes voice call recordings based on the content's context. The system is designed to classify transcribed voice call data into predefined categories and subcategories related to criminal activities, enabling efficient sorting, processing, and analysis of incident reports. Using SpaCy’s `en_core_web_trf` model, this classifier aims to improve the response time and accuracy of handling crime-related complaints by law enforcement agencies or relevant authorities.

## **Project Objectives**
1. **Accurate Classification**: Classify transcribed voice call data into the correct `category` and `sub_category` fields, which represent different types of criminal activities.
2. **Multi-Level Categorization**: Handle two levels of classification—main categories and more granular subcategories.
3. **Robust Text Processing**: Implement comprehensive text preprocessing, including stopword removal, punctuation elimination, and lemmatization, to ensure high-quality input for model training.

## **Key Features**
- **Data Preprocessing**: Preprocess transcriptions to handle empty values in categories or subcategories and convert them to empty strings. This step also includes removing stopwords and punctuation and lemmatizing words to reduce noise in the data.
- **Custom Training with SpaCy**: The project utilizes SpaCy’s `en_core_web_trf` transformer model for training. The model is optimized to handle text classification tasks efficiently, leveraging pre-trained language models for higher accuracy.
- **Model Deployment**: The classifier is structured for easy deployment and can integrate into systems that manage and sort crime-related reports.
- **JSON Data Handling**: The project ensures smooth handling of JSON data, where each categorized call recording is formatted and stored without unnecessary escape characters, maintaining clarity and readability.

## **Technologies Used**
- **Python**: Core programming language for model development.
- **SpaCy**: Used for NLP processing and classification.
- **Transformers (`en_core_web_trf` model)**: Transformer-based model for advanced language understanding and classification.
- **Pandas**: For data manipulation and handling CSV inputs for training and testing datasets.
- **JSON**: To store and handle transcribed data and classification results effectively.

## **Data and Workflow**
1. **Data Preparation**: Import the training and testing datasets (CSV files) containing `category` and `preprocessed_crimeaditionalinfo` columns. Handle missing data by filling empty categories and subcategories with empty strings.
2. **Text Preprocessing**: Remove stopwords, punctuation, and apply lemmatization to refine the text data.
3. **Model Training**: Train the SpaCy model to classify `preprocessed_crimeaditionalinfo` based on `category` and `sub_category` fields, using transformer-based embeddings from `en_core_web_trf`.
4. **Evaluation and Testing**: Use the test dataset to evaluate the model's accuracy, precision, recall, and F1 score, ensuring reliable classification.
5. **JSON Output Handling**: Save each classification output in JSON format, ensuring a clean, escape-free representation.

## **Expected Outcomes**
The resulting model will enable the automated categorization of voice call recordings related to crime reports with high accuracy. This classification will assist in prioritizing and routing complaints to the appropriate departments or personnel, significantly enhancing operational efficiency in handling criminal investigations or incidents.

## Model Results
Accuracy of classification for each category is shown below in format <category__subcategory> : <accuracy>
```json
"Online and Social Media Related Crime__Cyber Bullying  Stalking  Sexting": 0.9379739440382652,
"Online Financial Fraud__Fraud CallVishing": 0.8267308928187918,
"Online Gambling  Betting__Online Gambling  Betting": 0.8234244532612286,
"Online and Social Media Related Crime__Online Job Fraud": 0.923630283722387,
"Online Financial Fraud__UPI Related Frauds": 0.9094381164118309,
"Online Financial Fraud__Internet Banking Related Fraud": 0.8996975588656911,
"RapeGang Rape RGRSexually Abusive Content__": 0.991045309578797,
"Any Other Cyber Crime__Other": 0.8081216800453817,
"Online and Social Media Related Crime__Profile Hacking Identity Theft": 0.9305460418784166,
"Online Financial Fraud__DebitCredit Card FraudSim Swap Fraud": 0.9332004387929442,
"Online Financial Fraud__EWallet Related Fraud": 0.8637222872135986,
"Cyber Attack/ Dependent Crimes__Data Breach/Theft": 0.9833115525279011,
"Online and Social Media Related Crime__Cheating by Impersonation": 0.8020352041799669,
"Cyber Attack/ Dependent Crimes__Denial of Service (DoS)/Distributed Denial of Service (DDOS) attacks": 0.9821898512030147,
"Online and Social Media Related Crime__FakeImpersonating Profile": 0.8757707813141331,
"Cryptocurrency Crime__Cryptocurrency Fraud": 0.9819591348392023,
"Sexually Explicit Act__": 0.864403356287435,
"Sexually Obscene material__": 0.9283415364998877,
"Cyber Attack/ Dependent Crimes__Malware Attack": 0.9824175387016845,
"Online Financial Fraud__Business Email CompromiseEmail Takeover": 0.8673347894984796,
"Hacking  Damage to computercomputer system etc__Email Hacking": 0.9610161901651674,
"Cyber Attack/ Dependent Crimes__Hacking/Defacement": 0.9831529237315453,
"Hacking  Damage to computercomputer system etc__Unauthorised AccessData Breach": 0.9297168084070068,
"Cyber Attack/ Dependent Crimes__SQL Injection": 0.9801659601421855,
"Online and Social Media Related Crime__Provocative Speech for unlawful acts": 0.8950354530970123,
"Cyber Attack/ Dependent Crimes__Ransomware Attack": 0.9817017906364721,
"Cyber Terrorism__Cyber Terrorism": 0.8554447076824362,
"Child Pornography CPChild Sexual Abuse Material CSAM__": 0.9118704833789391,
"Cyber Attack/ Dependent Crimes__Tampering with computer source documents": 0.9802799433026222,
"Online Financial Fraud__DematDepository Fraud": 0.8305887823307179,
"Online Cyber Trafficking__Online Trafficking": 0.6887266081340642,
"Online and Social Media Related Crime__Online Matrimonial Fraud": 0.8864907948745645,
"Hacking  Damage to computercomputer system etc__Website DefacementHacking": 0.9077521693690759,
"Hacking  Damage to computercomputer system etc__Damage to computer computer systems etc": 0.8727585790087794,
"Online and Social Media Related Crime__Impersonating Email": 0.9176840014098496,
"Online and Social Media Related Crime__EMail Phishing": 0.8127697448475169,
"Hacking  Damage to computercomputer system etc__Tampering with computer source documents": 0.9028614457831324,
"Ransomware__Ransomware": 0.9559458189121053,
"Online and Social Media Related Crime__Intimidating Email": 0.8643805651270968,
"Report Unlawful Content__Against Interest of sovereignty or integrity of India": null
```
