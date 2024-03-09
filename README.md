# classifier_pytorch
pytorch classifier - male/female gender . Long sleeves/short sleeves clothing

**1) Code for downloading images from Myntra..**

**Explanation -**
I used chromedriver which loads page 1 to page 10 at a time. Each page has 50 images. I downloaded 500 images for 4 categories
[Men Long sleeves, Men short sleeves, women long sleeves, women short sleeves]

**Challenge faced -**
 usually jumping to the end of a document was not loading all images on pages.Myntra uses lazy loading. I used code to scroll part by part on screen so that all images get a chance to load.

**2) classifier_model_pytorch (poor 25-35% accuracy)**

**Explanation -**
 for each category I have 500 images. I used 80% as training images (400) and 100 images as tst dataset. So for 4 categories in all 2000 = 1600 (train images) + 400 (test images).

**Challenge Faced -**
 For inference testing. I took an image from amazon (unseen image to model) Accuracy is very poor. Inference is wrong. Prediction Probabilities for all 4 categories were ~25%. Not good.

**3) classifier_model_transfer_learning (85% accuracy)**

**Explanation -** 
I used Transfer learning by using pretrained model efficientnet_b0. Base model was put in freeze. Model was fine tuned on 2000 images (1600 training + 400 test)

**Result -** For inference testing. I took an image from amazon (unseen image to model).
Accuracy , Prediction Probabilities on all 4 categories is good.
