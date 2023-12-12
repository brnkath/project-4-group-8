<img src="https://github.com/brnkath/project-4-group-8/blob/main/img/wordcloud_banner.png" align="center">

**Title:** Spamalot: Spam or Not?<br/>
Project 4, Group 8<br/>
**Contributors:** Laura Bishop, Brian Kath, Jake Moen and Katy Yelle<br/><br/>
**Repository:** https://github.com/brnkath/project-4-group-8<br/>
**Website:** https://brnkath.github.io/project-4-group-8/<br/>
**Slide Deck:** PDF LINK<br/>
**Tableau Dashboard:** https://public.tableau.com/app/profile/jake.moen/viz/Top_Ten_Dashboard/Dashboard22?publish=yes<br/>
**Dataset:** https://www.kaggle.com/datasets/balaka18/email-spam-classification-dataset-csv<br/>
<br/>

## INTRODUCTION:

In an era dominated by digital communication, the influx of emails has become an integral part of our daily lives. However, mixed in with legitimate messages from work and family, the rise of spam emails poses a significant challenge, requiring efficient and accurate filtering mechanisms. In this project, our focus revolves around employing supervised learning techniques for binary classification to predict whether an email is spam. Using the "Email Spam Classification Dataset" from Kaggle - which includes labeled examples of both spam and non-spam emails - we aim to train and evaluate various machine learning models to create a predictive system. The project not only delves into the intricacies of building a reliable spam classifier but also emphasizes the importance of visualizing the underlying patterns and insights derived from the data, shedding light on the factors contributing to the classification decisions.

As we navigate this project, we will explore different aspects of data visualization to communicate the performance metrics, feature importance, and potential challenges of our predictive models. By employing compelling visualizations, we seek to enhance the interpretability of our results, making the complex processes of spam classification accessible to a wider audience. Through this endeavor, we aim not only to develop an effective spam detection model but also to highlight the significance of data visualization in conveying the story hidden within the data, fostering a deeper understanding of the intricacies of email spam detection through supervised learning.

### REPOSITORY STRUCTURE:

* Main Folder
    - .gitignore
    - data_models.ipynb
    - index.html
    - README.md
    - word_cloud.ipynb
 
* Sub Folders
  - Resources
    - emails.csv
  - css
    - styles.css
  - img
     - favicon.png
     - model-1-accuracy.png
     - model-2-accuracy.png
     - model-3-accuracy.png
     - model-4-accuracy.png
     - model-5-accuracy.png
     - model-5-random-forest-importance.png
     - tableau-dashboard.png
     - Top-Ten-Features-Bar.png
     - Top-Ten-Features-Bubble.png
     - Top-Ten-Usage-Bar.png
     - Top-Ten-Usage-Bar.png
     - Top-Ten-Dashboard-Bar.png
     - wordcloud_banner.png
     - wordcloud_medium.png
     - wordcloud-1.png
     - wordcloud-2.png
     - wordcloud-3.png

### OVERVIEW:

Using supervised learning in order to predict whether an email is spam or not, using a binary classification model.

#### General Breakdown of Tasks:

<ins>Data Model Implementation</ins>
- Clean, normalized & standardized data before modeling - Laura
- Python initialize, train, evaluates a model - Brian & Katy
- Dataset imported into Spark – Laura

<ins>Data Model Optimization</ins>
- Changes documented - Brian & Katy
- Change results documented - Brian & Katy
- Overall performance at end - Katy

<ins>Git Hub Documentation</ins>
- gitignore - Brian
- No unnecessary files/folders - Jake & Laura
- Draft README - Laura
- Draft Next Steps - Laura

<ins>Visualizations & Presentation</ins>
- Website - Brian
- Tableau - Jake
- Presentation slides - Katy
- Next Steps - Laura & Katy


### ANALYSIS:

**Model 1 - Logistic Regression | Long Words Only (>6 letters)**<br/>
In our dataset, we initially contended with a substantial 3000 columns. In the search for efficiency, we opted to streamline the feature set by exclusively retaining columns with more than 6 letters. This curation significantly pruned the columns to 1198. Remarkably, the model built upon this refined dataset delivered an impressive accuracy score of 92%.<br/>

<img src="https://github.com/brnkath/project-4-group-8/blob/main/img/model-1-accuracy.png" width="40%"><br/>


**Model 2 - Logistic Regression | Common Words Only**<br/>
Despite achieving our accuracy threshold with the initial model, we became intrigued by the idea of reducing the number of columns based on word frequency rather than letter count. This approach resulted in a model with only 307 columns, achieving an impressive 95% accuracy score. Consequently, we recommend this model over the first one, not only due to its superior accuracy but also because it utilizes fewer columns, thereby imposing a lighter computational demand.<br/>


<img src="https://github.com/brnkath/project-4-group-8/blob/main/img/model-2-accuracy.png" width="40%"><br/>

**Model 3 - Logistic Regression | All Columns**<br/>
Finally, we were interested in how to utilize all of the columns of the dataset on the accuracy of our logistic regression models. This comprehensive approach resulted in a notable accuracy score of 97%.<br/>

<img src="https://github.com/brnkath/project-4-group-8/blob/main/img/model-3-accuracy.png" width="40%"><br/>

**Model 4 - Support Vector Machine (SVM)**<br/>
Despite all logistic regression models meeting our threshold, we were interested in how other classification models would perform with the data. Since utilizing all of the columns resulted in the most accurate logistic regression model, we wanted to run this model with all of the columns as well. This model had a 95% accuracy score.<br/>

<img src="https://github.com/brnkath/project-4-group-8/blob/main/img/model-4-accuracy.png" width="40%"><br/>

**Model 5 - Random Forest** <br/>
Given the less favorable performance of the SVM model compared to the Logistic Regression model, we continued to explore the various models to identify the most effective one. To that, we turned to the Features Importance element of the Random Forest model to provide additional insight into our dataset. Notably, this particular model exhibited the highest accuracy score at 98%, outperforming all three model types considered—Logistic Regression, SVM, and Random Forest—when using the complete set of columns.<br/>

<img src="https://github.com/brnkath/project-4-group-8/blob/main/img/model-5-accuracy.png" width="40%"><br/>

## DATA VISUALIZATIONS: 

<img src="https://github.com/brnkath/project-4-group-8/blob/main/img/summary-model-results.png" width="75%"><br/>
Summary of Models and Results, compiled in Jupyter Notebook.<br/>

<img src="https://github.com/brnkath/project-4-group-8/blob/main/img/Top-Ten-Features-Bar.png" width="50%"><br/>
Bar graph of the top represented features as identified by Random Forest: Feature Importances.<br/>

<img src="https://github.com/brnkath/project-4-group-8/blob/main/img/Top-Ten-Features-Bubble.png" width="50%"></br>
Bar graph of the top represented features as identified by Random Forest: Feature Importances.<br/>

## CONCLUSION:

The significance of robust spam filters in today's digital landscape cannot be overstated. They are not simply for convenience but for your digital footprint's protection. With the exponential growth of electronic modes of communication, we faced an ever-increasing deluge of emails, making a filtering system indispensable.

Developing an effective spam identification model hinged on a detailed examination of linguistic patterns. Our models consistently achieved a remarkable accuracy rate exceeding 90%, building from these linguistic patterns. This success could be largely attributed to the nature of our dataset, which served as a key factor in training the models to differentiate between spam and legitimate content. Notably, we focused on linguistic elements, excluding non-textual components like date and time information. This intentional omission allowed us to streamline our approach and gain a distinct advantage over broader email analysis methods. This linguistic emphasis significantly contributed to the outstanding performance of our spam detection models.

Among the models tested, the Random Forest algorithm emerged as the most effective with a 97% accuracy. Several factors contributed to the overall superiority of Random Forest. One notable strength lay in its inherent resilience against overfitting. This characteristic was derived from the ensemble nature of Random Forest, where multiple decision trees were trained on different subsets of the data. This diversity in training data mitigated the risk of overfitting, enhancing the model's generalizability to new, unseen data. Moreover, Random Forest exhibited robustness in handling outliers and nonlinear data. This versatility was particularly advantageous when dealing with datasets that might deviate from linear structures.

Another commendable aspect of Random Forest was its efficiency when applied to large databases. Its parallelized training process and the ability to distribute computation made it well-suited for handling substantial volumes of data. This efficiency not only contributed to faster model training but also enhanced the scalability of the algorithm, making it a pragmatic choice for datasets with extensive dimensions. With over 3000 rows and more than 5000 columns in our dataset, Random Forest stood out as an exceptionally suitable choice for this particular question: Spam or Not Spam Communication.

The accuracy of our models directly influenced the trustworthiness of computed feature importances. Given the consistently high accuracy of our models, the derived importances became dependable indicators of feature significance. These computed importances offered an approximate measure of the importance of different features within the dataset, aiding in the understanding of underlying patterns.

Given the exceptional accuracy of our models, the derived feature importances provided valuable insight for selecting the most appropriate model to move forward with. They served as nuanced tools for identifying key contributors to predictive power, enhancing interpretability. The precision of our models not only boosted practical utility but also amplified the reliability of feature importances, valuable for discerning intrinsic data patterns.

The deployment of advanced machine learning techniques for classification underscored the pivotal role of accurate spam detection. This not only shielded users from malicious content and thwarted phishing attempts but also served as a crucial mechanism for mitigating the challenges posed by information overload. As we navigated the digital landscape, the significance of precision in spam detection became increasingly evident, contributing to a safer and more streamlined user experience.

### NEXT STEPS:

* To elevate the project, a crucial step involves creating a program for generating data like our current dataset but with recent information. This maintains relevance for the spam detection model. Utilizing the latest data allows adaptation to evolving electronic communication trends, enhancing spam identification accuracy. The program should consider language changes, emerging linguistic patterns, and communication style variations. Incorporating real-time features and recent spam characteristics strengthens the model's robustness, making it adept at tackling contemporary digital challenges.

* A vital next step is optimizing the Random Forest model for enhanced performance. Focusing on important features identified during development, fine-tuning parameters improves efficiency with diverse datasets. Optimization extends to scalability and speed, crucial for real-world databases. Exploring alternative feature selection approaches reveals hidden patterns, refining predictive capabilities. This iterative process involves continuous testing and validation to ensure enhancements contribute positively to the model's accuracy and overall performance.


### SPAM TIPS:

* To take a proactive stance, an IT Department should implement a robust email filtering program that leverages advanced machine learning algorithms to intelligently detect and block unwanted messages. Regularly updating and maintaining those filters is essential to staying ahead of evolving spam tactics. 

* Educating employees about safe email practices, such as avoiding clicking on suspicious links, inspecting the sender's domain elements for questionable URLs, and downloading attachments from unknown sources contributes to a more resilient defense against spam and phishing threats.

* Implementing multi-factor authentication (MFA) will strengthen email security by enforcing an additional layer of protection against unauthorized access, reducing the risk of compromised accounts through phishing attacks. By requiring users to provide multiple forms of verification, such as a password and a temporary code sent to their mobile device, MFA significantly enhances the overall security posture and mitigates the impact of potential email-related security breaches.

## THANK YOU!

To Hunter, Sam, and Randy – thank you so much for these last 24 weeks, giving us this opportunity to grow and develop a whole new skillset built for success! 

### RESOURCES:

* [https://www.kaggle.com/](https://www.kaggle.com/)
* [https://slidesgo.com/](https://slidesgo.com/)
* [https://python-charts.com/ranking/wordcloud-matplotlib/](https://python-charts.com/ranking/wordcloud-matplotlib/)
* [https://www.geeksforgeeks.org/ways-to-import-csv-files-in-google-colab/](https://www.geeksforgeeks.org/ways-to-import-csv-files-in-google-colab/)

