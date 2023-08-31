# Datasheet Template

As far as you can, complete the model datasheet. If you have got the data from the internet, you may not have all the information you need, but make sure you include all the information you do have. 

## Motivation

- For what purpose was the dataset created? 

The dataset that I choose is the FER-2013 dataset that it was created for the purpose of advancing the field of facial expression recognition through machine learning and computer vision techniques. Specifically, its primary purpose was to facilitate research and development in the area of emotion recognition from facial expressions.

The dataset consists of 35,887 grayscale images of faces, each labeled with one of seven different emotional expressions:

Angry
Disgust
Fear
Happy
Sad
Surprise
Neutral

But for our capstone project because of the limitation of computer processing at hand I will use only 4 emotions for this model that are: Happy, Sad, Surprise and Neutral

Researchers and machine learning practitioners use this dataset to train and test facial expression recognition algorithms and models. It serves as a valuable resource for developing and evaluating techniques that can automatically detect and classify human emotions based on facial cues. Applications of such technology include human-computer interaction, sentiment analysis, and affective computing, among others. 

- Who created the dataset (e.g., which team, research group) and on behalf of which entity (e.g., company, institution, organization)? Who funded the creation of the dataset?

The FER-2013 dataset was created and designed by Goodfellow et al as a Kaggle competition (http://cs230.stanford.edu/projects_winter_2020/reports/32610274.pdf). In particular, it was created, collected and curated by a team led by Pierre-Luc Carrier and Aaron Courville (https://arxiv.org/pdf/1307.0414.pdf). The dataset was created as part of their research in the field of machine learning and computer vision.

As for funding, specific details about the funding sources for the creation of the FER-2013 dataset may not be readily available in the dataset documentation or in publicly accessible information. Dataset creation in academic settings is often supported by a combination of research grants, academic institutions, and sometimes collaborations with industry partners. Funding for such projects can come from various sources, including government research grants, private foundations, and academic institutions themselves.

If you require more detailed information about the funding sources for this dataset, it may be necessary to contact the researchers involved directly or refer to their publications and acknowledgments for potential mentions of funding support.

 
## Composition

- What do the instances that comprise the dataset represent (e.g., documents, photos, people, countries)? 

The instances in the FER-2013 dataset represent grayscale images of human faces. Each image corresponds to a single instance and captures the facial expression of an individual. These images are labeled with one of seven different emotional expressions: Angry, Disgust, Fear, Happy, Sad, Surprise, or Neutral. But for our project we will only choose 4 that are Happy, Sad, Surprise and Neutral.

The dataset comprises photographs of people's faces, and each instance (image) is associated with a specific emotional expression category. The purpose of the dataset is to provide a standardized collection of facial expression images for training and evaluating machine learning models and algorithms in the field of facial expression recognition.

- How many instances of each type are there? 

The FER-2013 dataset contains the following number of instances (images) for each emotional expression category:

Angry: 4,015 instances
Disgust: 1,248 instances
Fear: 4,467 instances
Happy: 7,025 instances
Sad: 4,858 instances
Surprise: 3,490 instances
Neutral: 6,707 instances

These numbers add up to a total of 35,800 instances in the dataset. Please note that these counts may vary slightly depending on the version or source of the dataset, but the numbers provided here are based on the commonly referenced version of FER-2013 that we are using form kaggle.

- Is there any missing data?

According to the information available in the internet, the FER-2013 dataset is known for being relatively clean and well-organized, but it's possible that there could be missing data or inconsistencies in the dataset. In the context of image datasets like FER-2013, missing data typically refers to images that were not properly collected or labeled.

While the creators of the dataset made efforts to ensure its quality, no dataset is entirely free from potential issues. In practice, researchers and developers who use the FER-2013 dataset often perform data preprocessing steps to handle any potential missing or corrupted data. This may include checking for missing images, ensuring all images are labeled correctly, and dealing with any outliers or anomalies and some data augmentation as we did in our project.


- Does the dataset contain data that might be considered confidential (e.g., data that is protected by legal privilege or by    doctor–patient confidentiality, data that includes the content of individuals’ non-public communications)?

According to the information from the internet the FER-2013 dataset does not present concerns related to privacy or confidentiality. The dataset is focused solely on facial expressions and emotions and does not include any personally identifiable information (PII), sensitive text, or private communication content. It was created for the purpose of advancing research in facial expression recognition and does not involve private or confidential data in any way.

Researchers and developers commonly use the FER-2013 dataset for machine learning and computer vision experiments related to emotion recognition, and privacy or confidentiality concerns are not associated with this dataset.


## Collection process

- How was the data acquired? 

The FER-2013 dataset was created by gathering the results of a Google image search of each emotion and synonyms of the emotions. It's important to note that the dataset was curated from diverse sources on the internet, and the exact sources of each image might not be explicitly documented.

- If the data is a sample of a larger subset, what was the sampling strategy? 

We are using the whole dataset for the emotions selected, happy, sad, surprise and neutral

- Over what time frame was the data collected?

According to the information from the internet, the FER-2013 dataset was created by collecting images from various sources on the internet, and it doesn't have a specific time frame associated with its data collection. The dataset is a static collection of facial expression images that were gathered at a point in time for the purpose of creating a benchmark dataset for facial expression recognition research. The images in the dataset represent a diverse set of individuals and facial expressions, but there is no publicly available information regarding the precise period during which these images were collected.


## Preprocessing/cleaning/labelling

- Was any preprocessing/cleaning/labeling of the data done (e.g., discretization or bucketing, tokenization, part-of-speech tagging, SIFT feature extraction, removal of instances, processing of missing values)? If so, please provide a description. If not, you may skip the remaining questions in this section. 

Yes, for the project the images has been alredy labeled and do some preprocessing as data augmentation to improve the generalization of the model. The data augmentation 

- Was the “raw” data saved in addition to the preprocessed/cleaned/labeled data (e.g., to support unanticipated future uses)? 

yes it was saved as the original dataset. It can be used for testing too.

 
## Uses

- What other tasks could the dataset be used for? 

While the FER-2013 dataset was designed for facial expression recognition, it can also be used for several related computer vision and machine learning tasks. Here are some alternative tasks for which the dataset can be repurposed like facial landmark detection, age estimation, gender classification, facial attribute recognition, emotion intensity estimation (good for pscyhology assessment), emotion transfer to transfer emotions from one face to another one, emotion generatio, multimodal emotion recognition to combine the facial emotion recognition with other modalities like audio as stress speech recognition, or text writing to performr multimodal recognition, which can provide more accurate and robust emotion recognition results and other examples like emotion-aware interfaces. 

- Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses? For example, is there anything that a dataset consumer might need to know to avoid uses that could result in unfair treatment of individuals or groups (e.g., stereotyping, quality of service issues) or other risks or harms (e.g., legal risks, financial harms)? If so, please provide a description. Is there anything a dataset consumer could do to mitigate these risks or harms? 

While the FER-2013 dataset can be a valuable resource for facial expression recognition and related tasks, dataset consumers should exercise caution, be aware of its limitations and potential biases, and take steps to mitigate ethical, legal, and fairness-related risks when using the data. Additionally, when deploying models trained on this dataset in real-world applications, thorough testing and monitoring for unintended consequences are essential to ensure fair and ethical use. Some considerations to have are some of the following: Posed Expressionsas the images in FER-2013 predominantly contain posed facial expressions. Real-world emotional expressions can be more complex and subtle, so models trained solely on posed expressions may not perform well in naturalistic settings, as mitigation for this, researchers should acknowledge the limitations of posed expressions and, if possible, combine FER-2013 with datasets containing spontaneous or real-world emotional expressions for more robust models. Label Noise: While efforts were made to obtain accurate emotion labels, the labeling process for FER-2013 involved annotators who may not have had access to the subjects' true emotional states. This can introduce label noise, where some images may be mislabeled, as mitigation for this, the dataset consumers should be aware of the potential for label noise and may consider using techniques like label smoothing, label correction, or outlier detection to mitigate its effects. Limited Diversity: The FER-2013 dataset is known for its limited diversity in terms of age, ethnicity, and gender. The majority of the images in the dataset depict young individuals with relatively neutral facial expressions. This lack of diversity can lead to biases in models trained on the dataset, which may not generalize well to more diverse populations, as mitigation for this, dataset consumers can augment the dataset with additional images from more diverse sources to create a more representative training dataset. They can also be cautious when applying models trained on FER-2013 to populations that significantly differ from the dataset's demographics. Ethical Considerations: Facial expression datasets like FER-2013 raise ethical concerns regarding privacy and consent, especially if the images were collected without informed consent. It's essential to respect individuals' privacy and ensure that the dataset is used in a way that aligns with ethical guidelines, as mitigation, dataset consumers should ensure that they have the necessary permissions to use the dataset and should handle the data in compliance with applicable privacy laws and ethical guidelines. Anonymization and blurring techniques can be applied to protect individuals' identities.


- Are there tasks for which the dataset should not be used? If so, please provide a description.

There are certain tasks and applications for which the FER-2013 dataset should be used with caution or avoided altogether due to its limitations and potential drawbacks. Here are some tasks for which the dataset may not be well-suited:

Emotion Detection in Naturalistic Settings: If the goal is to detect emotions in naturalistic settings, such as analyzing emotions in videos captured in real-world environments, FER-2013 may not provide the necessary diversity and realism. Models trained solely on posed expressions may not generalize effectively to spontaneous or subtle emotional expressions.
Emotion Detection in Diverse Populations: FER-2013 is limited in terms of demographic diversity. It may not perform well in applications where emotion detection is required across diverse age groups, ethnicities, or genders. Using it in such cases could result in biased or inaccurate predictions.
Real-time Emotion Detection in Critical Applications: In critical applications where real-time emotion detection is essential, such as healthcare (e.g., patient monitoring) or autonomous vehicles (e.g., detecting the emotions of drivers), FER-2013 may not be reliable. Real-world emotions are often more nuanced and complex than the posed expressions in the dataset, making it unsuitable for situations where safety is a concern.
Biometric Authentication: FER-2013 should not be used for biometric authentication or identification systems. The dataset primarily contains posed expressions, which are not suitable for reliable and secure biometric authentication. Using it for such purposes could lead to security vulnerabilities and false positives/negatives.
Applications with High Stakes: In applications where the consequences of incorrect predictions are significant, such as medical diagnoses or autonomous vehicles, relying solely on FER-2013 could pose risks to safety and well-being.



## Distribution

- How has the dataset already been distributed? 

The FER-2013 dataset has been distributed and made publicly available for research purposes. It was initially created and made accessible through Kaggle and has been used in various research projects, competitions, and educational contexts. Some common ways in which the dataset has been distributed and used include Kaggle, research publications, github and online repositories, educational resources, competitions and open data portals that make the FER-2013 widely accesible


- Is it subject to any copyright or other intellectual property (IP) license, and/or under applicable terms of use (ToU)?  

The FER-2013 dataset, as it was originally released on Kaggle, was made available for research purposes and typically falls under specific terms of use (ToU) set by Kaggle. However, it's important to note that the licensing and terms of use for datasets can evolve, and different versions of the dataset may have different terms. As far as August 2023, it still remains as Open database, the FER-2013 dataset was generally used for research and educational purposes under Kaggle's Terms of Use.

Kaggle's Terms of Use typically include provisions that restrict the use of the data to non-commercial, research, and educational purposes. Users are often required to attribute the source of the data appropriately and are prohibited from using the data for commercial or other non-allowed purposes. Since the terms of use and licensing for datasets can change, and new versions or distributions of the FER-2013 dataset may exist, it's essential for users to visit the official source of the dataset, such as Kaggle or the relevant repository or website, and review the specific terms and conditions associated with the version of the dataset they intend to use. Users should always adhere to the most up-to-date terms of use and any licensing agreements to ensure they are using the dataset legally and ethically.

## Maintenance

- Who maintains the dataset?

Not exactly specified as Kaggle is a platform where users can upload, share, and work on datasets and machine learning projects. Dataset creators often retain control and ownership of their datasets and are responsible for updates, maintenance, and any subsequent versions or distributions. But to obtain more detailed information about the maintenance and origin of the FER-2013 dataset, it may be necessary to refer to academic papers, research publications, or other sources associated with the dataset, if available. Up to August 2023 we could not find any information related.