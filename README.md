# Forestfires

## Business Scope: Predicting Burned Area of Forest Fires in Northeast Portugal

The goal of this project is to predict the burned area of forest fires in the northeast region of Portugal using meteorological and other relevant data. This task has implications in various areas, and its outcomes can contribute to a multitude of sectors and initiatives. Below are some aspects of the business scope:

1.  **Environmental Monitoring and Early Warning Systems:** Developing accurate predictive models for burned area estimation can facilitate the creation of effective early warning systems. These systems provide timely alerts to authorities and communities, enabling them to prepare for potential fires and mitigate environmental impact and public safety concerns.

2. **Risk Assessment and Management:** Predictive models can assist in assessing fire risk in the northeast region of Portugal based on meteorological and related data. This information aids in allocating firefighting resources, equipment, and supplies to high-risk areas, enhancing the efficiency and effectiveness of fire management efforts.

3. **Resource Allocation:** Government agencies responsible for firefighting, emergency response, and environmental conservation can benefit from predictive models. These models optimize resource allocation by identifying areas with higher fire probabilities, ultimately enhancing fire management strategies.

4. **Policy Formulation and Land Management:** Insights from predictive models inform policymakers in creating effective land management strategies. Data-driven knowledge about meteorological conditions, land use, and fire occurrence can lead to policies promoting safer land management practices and reducing fire risks.

5. **Research and Collaboration:** Building predictive models necessitates collaboration among experts in meteorology, environmental science, data science, and public safety. This initiative fosters interdisciplinary research, leading to innovative solutions and advancements in fire management strategies.

6. **Insurance and Economic Impact Assessment:** Accurate burned area predictions aid insurance companies in assessing fire-related claims. Furthermore, understanding the economic impact of forest fires on local communities, agriculture, tourism, and infrastructure enables informed decision-making and preparedness.

7. **Public Awareness and Education:** Predictive model outcomes raise public awareness about forest fire risks. Educating residents about fire prevention, safety measures, and emergency response promotes responsible behavior and minimizes fire-related damages.

8. **Data Collection and Infrastructure:** Developing accurate models necessitates robust data collection, storage, and analysis infrastructure. This may involve creating data-gathering mechanisms, quality control processes, and secure storage solutions.

9. **Continuous Improvement and Adaptation:** Predictive models must be continuously refined as new data becomes available and environmental conditions evolve. This establishes a long-term business scope for maintaining and enhancing model accuracy.

In summary, predicting burned areas of forest fires in the northeast region of Portugal has broad applications across environmental monitoring, risk assessment, resource allocation, policy formulation, research collaboration, public awareness, and more. The accurate prediction of burned areas contributes to improved preparedness, resource allocation, and management of forest fire-related risks.

## Forest Fire Burned Area Prediction Study

This section highlights key insights from a research paper titled "[Cortez and Morais, 2007]" that delves into the prediction of burned areas in forest fires through data mining techniques. The study explores various aspects of predictive modeling to improve accuracy and provide valuable insights:

1. **Output Transformation:** The study begins by transforming the output variable "area," representing burned forest area, using the natural logarithm function ln(x+1). This transformation enhances model stability and performance when dealing with skewed or non-normal data distributions.

2. **Data Mining Methods:** Researchers employ a range of data mining methods to predict the transformed burned area. These methods likely involve different regression algorithms designed to capture relationships between input features and the transformed area.

3. **Post-Processing:** After model training, predictions are post-processed using the inverse of the ln(x+1) transformation. This step restores predictions to their original scale, enabling direct comparison with actual burned area values.

4. **Input Setups:** The study explores four distinct input configurations for the predictive models. These setups encompass various combinations of input features, which could encompass meteorological conditions and other pertinent data.

5. **Cross-Validation:** Experiments employ a 10-fold cross-validation approach. This technique divides the dataset into 10 subsets or folds. Models are iteratively trained on nine folds and tested on the remaining fold, providing insight into model generalization.

6. **Regression Metrics:** Researchers measure two vital regression metrics: MAD (Mean Absolute Deviation) and RMSE (Root Mean Squared Error). These metrics quantify model accuracy by evaluating how well predictions align with actual burned area values.

7. **Gaussian Support Vector Machine (SVM):** Among the models examined, a Gaussian support vector machine (SVM) utilizing only four direct weather conditions (temperature, relative humidity, wind, and rain) achieves the best MAD value of 12.71 with a 95% confidence interval. SVM, a versatile machine learning algorithm, excels in regression and classification tasks.

8. **Naive Mean Predictor:** Interestingly, the most optimal RMSE is attained by a simple naive mean predictor. This observation suggests that while the SVM model excels in MAD, the naive mean predictor displays more consistent prediction errors in terms of RMSE.

9. **Regression Error Curve (REC):** Analysis of the regression error curve (REC) reveals that the SVM model predicts a greater number of instances within a lower admitted error range. This highlights the SVM model's proficiency in accurately predicting smaller fires, which constitute the majority of cases.

In summary, this study provides valuable insights into predicting burned areas in forest fires. By employing a range of data mining methods, a Gaussian SVM leveraging specific weather conditions emerges as the top performer in terms of MAD. The SVM's strength lies in its accurate prediction of smaller fires, contributing to a comprehensive understanding of forest fire dynamics.


## Dataset Attributes Description

The dataset used in the study "[Cortez and Morais, 2007]" for predicting burned forest area comprises several attributes that contribute to the predictive modeling process. Here's a breakdown of each attribute:

1. **X - x-axis spatial coordinate:** Represents the x-axis location within the Montesinho park map. Values range from 1 to 9.

2. **Y - y-axis spatial coordinate:** Represents the y-axis location within the Montesinho park map. Values range from 2 to 9.

3. **month - month of the year:** Represents the month in text format, ranging from 'jan' to 'dec'.

4. **day - day of the week:** Represents the day of the week in text format, ranging from 'mon' to 'sun'.

5. **FFMC - Fine Fuel Moisture Code index:** A value from the FWI (Fire Weather Index) system, indicating the moisture content of fine fuels. Values range from 18.7 to 96.20.

6. **DMC - Duff Moisture Code index:** A value from the FWI system, indicating the moisture content of decomposed organic material. Values range from 1.1 to 291.3.

7. **DC - Drought Code index:** A value from the FWI system, indicating the moisture content of deep organic layers. Values range from 7.9 to 860.6.

8. **ISI - Initial Spread Index:** A value from the FWI system, indicating the potential rate of fire spread. Values range from 0.0 to 56.10.

9. **temp - temperature:** Represents the temperature in Celsius degrees. Values range from 2.2 to 33.30.

10. **RH - relative humidity:** Represents the relative humidity in percentage (%). Values range from 15.0 to 100.

11. **wind - wind speed:** Represents the wind speed in kilometres per hour (km/h). Values range from 0.40 to 9.40.

12. **rain - outside rain:** Represents the amount of outside rain in millimetres per square meter (mm/m2). Values range from 0.0 to 6.4.

13. **area - burned area of the forest:** Represents the burned area of the forest in hectares (ha). Values range from 0.00 to 1090.84. This attribute is mentioned to be highly skewed toward smaller values, so a logarithmic transformation might be applied when modeling.

These attributes encompass spatial coordinates, temporal characteristics, meteorological indices, and the target variable (burned area). The "area" variable's logarithmic transformation is recommended due to its skewed distribution. This dataset serves as the foundation for predicting burned forest areas using advanced data mining techniques.
