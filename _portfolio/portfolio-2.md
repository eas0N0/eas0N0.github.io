---
title: "Image-Text Based Dermatological Diagnosis Helper: Vector and Relational Database"
excerpt: "Forecasting multiple time series concurrently based on their interrelations and individual information<br/><img src='/images/model_archi.png'>"
collection: portfolio
---
Please visit the full version of the [report](https://github.com/eas0N0/Image-Text-Based-Dermatological-Diagnosis-Helper/blob/main/report_g31(1).pdf) here.

# Introduction

Skin diseases have always been persistent challenges to human physical health. 
In the current healthcare environment, the imbalance between the number of 
doctors and patients has driven many individuals turn to self-detection online. 
However, internet-based information tends to be disorganized and unreliable. 
With the development of deep learning, its combination with dermatological 
diagnosis has demonstrated great effectiveness. In response to this evolving 
scenario, therefore, we introduce **Image-Text Based Dermatological Diagnosis 
Helper** - an innovative system designed to offer guidance for individuals who 
are seeking dermatological diagnosis and treatment. The system combines two 
types of databases: the relational database is for storing data including patients’ 
basic information, symptom descriptions, information about associated diseases, 
recommended medical treatments, and drug information. The vector database is 
designed for storing pictures of different skin diseases’ symptoms. Additionally, 
it facilitates a direct channel for individuals to purchase necessary medicines 
from nearby drug stores. To enhance user experience, we have developed a user-friendly interface (UI) that streamlines data queries and processing. The 
implementation of this database system is poised to significantly benefit patients 
by providing them with tools for self-diagnosis and self-treatment. By bridging 
the gap between online information and accurate medical guidance, this system 
has the potential to enhance the overall healthcare experience in a more 
accessible and efficient manner.

# System Architecture
In essence, our database system is a comprehensive integration of diagnostic and drug 
purchasing functionalities. It comprises two primary components: a diagnosis system and a 
drug ordering system. The diagnosis system is fundamentally a vector database, and in 
contrast, the drug ordering system operates as a relational database. This dual-component 
structure allows for a cohesive and efficient platform that seamlessly combines diagnostic 
capabilities with the convenience of purchasing prescribed medications.  

As previously highlighted, our database was meticulously crafted to tackle the challenges 
associated with human reliance on visual inspection for diagnosing skin diseases and the 
inefficiencies of online searches. To utilize the system, users simply upload a photo of the 
affected skin area. Subsequently, the vector database of the drug ordering system encodes the 
image, facilitating the retrieval of the most closely matched image along with its corresponding 
diagnosis and treatment plan (inclusive of the recommended medication) stored in the database. 
Users can promptly proceed to order the prescribed medication through diagnosis system, 
thereby achieving a streamlined process for both diagnosis and drug treatment.

![image](https://github.com/eas0N0/Vector-and-Relational-Database/assets/129197157/0bcfddce-b6a2-4fb5-9cf1-26d3dd3d0e25)

## Diagnosis System

Traditional databases are structured using tables that contain structural information. AI tools, 
such as text embedding or image encoding, produce high-dimensional vectors, offering greater 
power and flexibility compared to fixed symbolic representations. However, conventional 
databases designed for SQL queries are not well-suited to handle these new representations. 
The massive influx of multimedia items results in billions of vectors. Identifying similar entries
is inefficient with standard query languages. So, we designed a vector database.
Firstly, we employ the embedding model to generate vector embeddings for the images and 
texts earmarked for indexing. Secondly, these vector embeddings are incorporated into the 
vector database, with a reference back to the original content from which the embedding 
originated. Finally, when receiving a query from the application, we utilize the same 
embedding model to create embeddings for the query itself. These query embeddings are then 
employed to search the database for vector embeddings that closely align with the query. This 
method enables efficient retrieval of relevant content based on the similarity of vector 
embeddings.

![image](https://github.com/eas0N0/Vector-and-Relational-Database/assets/129197157/21749fc6-5626-47d1-a971-56e35cfac977)

## Drug Ordering System
This system is designed to help users buy medication conveniently after obtaining a diagnosis.
The user can order for drug after obtaining diagnosis, which containing symptom and treatment. 
Our system integrates information of patients, diseases, drug orders, drug stores and inventory 
of drugs, which is a relational database.

![image](https://github.com/eas0N0/Vector-and-Relational-Database/assets/129197157/1112734d-bea1-46ff-b5e9-81a9520079f8)

# Conclusion
In summary, our Image-Text Based Dermatological Diagnosis Helper, seamlessly integrates 
online diagnostics with medication ordering. On the one hand, we employ CLIP to convert 
images and texts into vectors. Subsequently, FAISS is utilized to compress, index, and retrieve 
the data, facilitating efficient diagnosis. On the other hand, we have implemented a relational 
database, allowing users to conveniently order medications following the diagnosis results. 
Through rigorous testing, our system has demonstrated a harmonious blend of accuracy and 
efficiency.

```HTML
<video width="320" height="240" controls>
    <source src="https://github.com/eas0N0/Image-Text-Based-Dermatological-Diagnosis-Helper/blob/0fdb14a6570eda7bd30f871650f9fef12d161b22/video_demo.mp4" type="video/mp4">
</video>
```


