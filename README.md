# GmE 221 – Laboratory Exercise 6

## Overview

This laboratory exercise will focus on applying GeoAI concepts.

## Expected Output

I expect to create a script that will predict the classification of parcels.

---

## Environment Setup

---

## How to Run

---

## Outputs

| Model |    Features    | Accuracy |
| :---- | :------------: | -------: |
| RF    |    Default     |    96.13 |
| RF    | 2 New Features |    96.34 |
| KNN   |    Default     |    94.77 |
| KNN   | 2 New Features |    94.76 |

I generated 4 predictions with the parameters and accuracies above. Based on my observation RF with 2 additional features produced the best accuracy. On the other hand KNN models, both the default and the one with 2 new features have bad accuracy compared to RF.

---

## Reflection

### Data Loading Reflection

1. Why are parcels the prediction unit?

   Parcel was used as the prediction unit since parcel has different classification and we will use the other geojson data to predict the classification of parcel.

2. What spatial processes might roads influence?

   Road can influence the parcel proximity to road network.

3. Why might tourism affect parcel classification?

   Tourism can affect the value of parcel and type of structures desirable to be build on the parcel. For example hotels are more desirable to be build on parcels near tourism spots.

4. Is machine learning occurring at this stage?

   No.

### Feature Engineering Reflection

5. Why can geometry not be used directly in ML?

   It is hart to use geometry directly in ML because it is just coordinates with no context.

6. Why are distances meaningful features?

   It provides context on what is in the proximity of the parcels.Everything is related to everything else, but near things are more related than distant things.

7. Which feature do you think is most influential?

   I think land use is the most infuential since it dictates what structures can be built on the parcel.

### Model Reflection

8. What does accuracy mean spatially?

   Since the script is predicting on the parcel ASS_CLASSI it is not predicting a spatial feature therefore accuracy is not directly related to spatial feature. Spatial features has indirect relation to accuracy since the input columns used in the ML model are generated from spatial relationship between the parcel and the feature.

9. Can a model have high accuracy but poor spatial interpretation?

   Yes.

10. What features may improve the model?

    Data on zoning can improve the accuracy of the model.

### Spatial Misclassification

    Based on the printed result an Agricultural(A) ASS_CLASSI was tagged as Residential(R)

### Final Reflection Questions

11. How is GeoAI different from traditional GIS analysis?

    Traditional GIS is easier to follow on the other hand GeoAI is more of a black box where we dont really understand how the model created relationships between the features to predict the output.

12. What spatial features most influenced the model?

    Based on my testing removing dist_to_school as feature decreased the accuracy the most therefore it has the most influence to the accuracy.

13. What are the limitations of this model?

    Since the prediction result is dependent on the features provided, the accuracy of the prediction is influenced the proper feature selection by the user.

14. How can this support spatial decision-making?

    GeoAI is useful in finding patterns that are not easily noticible by humans. GeoAI can help decision makers see spatial patterns.

15. What ethical or planning concerns may arise from predictive parcel classification?

    One thing to consider when using GeoAI for predicting parcels is who is accountable for the results. In traditional GIS, the GIS specialist processing the data is accountable to the result however in GeoAI no one is accountable. That is why it is advisable that results from GeoAI is still reviewed by human experts before being used as inputs by decision makers.

---
