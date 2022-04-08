# Pneumonia Diagnosis Using Machine Learning

***
### The Background
Pneumonia is a common infection that causes inflammation and possible fluid accumulation in the air sacs of the lungs. In China, pneumonia is one of the leading causes of death for [children under 5 years old](https://journals.lww.com/md-journal/Fulltext/2018/11160/The_drug_use_to_treat_community_acquired_pneumonia.42.aspx#:~:text=More%20than%202%20million%200,the%20age%20of%205%20years.) The infection is commonly caused by bactria and viruses, but can also be caused by fungal sources. 

Pediatric pneumonia is initially diagnosed based on the [time of the year and the results of a physical exam](https://www.nationwidechildrens.org/conditions/pneumonia), paying attention the child's breathing and listening to the lungs. Physical symptoms associated with pneumonia generally include fever, rapid breathing, and increased heart rate. A further step in diagnosis would be to use chest X-rays; pneumonia is not always seen on x-rays, either because [the disease is in its initial stages or it involves a part of the lung not easily seen by X-ray.](https://www.wikidoc.org/index.php/Pneumonia_chest_x_ray). Inconclusive initial testing can result in additional blood tests to confirm or rule out the presence of infection.

### Business Problem
As we can see, even with modern medicine pneumonia can be misdiagnosed. Not all pneumonia infections are treated in the same way; viral infections cannot be fought with the same antibiotics that would treat a bacterial infection. A fast and accurate diagnosis allows doctors to treat the infection with the appropirate care. One application of machine learning in medicine is digital diagnosis. We have been tasked with developing an identification model to determine if a chest X-ray indicates the presence of pneumonia. False negative results are to be minimized compared to false positives.

### The Data
The data is sourced from [Kaggle](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia). It is already split into three folders for training, validation and testing, totaling 5,856 images. All the chest radiographs were screened for quality and diagnostic labeling performed by physicians. The images were collected during routine clinicial care of pediatric patients between one and five years old from Guangzhou Women and Children's Medical Center in Guangzhou, China.

### The Process
Images were initially scaled to square and resized to 256x256. An MLP model was used as a baseline, scoring a 74% total accuracy but basically behaving as a majority class predictor. We then iterated through versions of convoluted neural networks, comparing classification reports and confusion matrices to evaluate performance before ultimately selecting a model.

### Conclusions
Our best performing CNN model scored an overall accuracy of 82%, with a 94% recall on pneumonia cases. Future work would involve exploring pretrained model accuracy, expansion to ternery classification (no infection vs bacterial vs viral), and creating a web dashboard and using our model in production.

