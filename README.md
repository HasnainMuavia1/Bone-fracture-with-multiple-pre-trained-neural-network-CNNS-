**Report**

**Dataset Description**

Class "Chest" has 300 pictures, while the rest of the classes contain 54, 105, 71, 271, 61, 34, and 23 images, respectively. Therefore, there is an imbalance in the dataset. We applied image augmentation techniques such as flipping and rotating (90°, 180°, 270°). With these augmentation techniques, each class now has 300 pictures.

**Classes:**

- Chest Fracture = 0
- foot Fracture= 1
- hand Fracture = 2
- hip Fracture = 3
- leg Fracture = 4
- shoulder Fracture = 5
- spinal cord Fracture = 6
- ulna and radius upper arm bone fracture = 7

All models other than VGG 16 used following layers:

1. Flatten
1. Dense with 128 units

**Hyperparameters:**

- RMSprop(learning\_rate=1e-5)
- Epochs 10

**Best Model:**

DenseNet201








|<p></p><p>**Model**</p>|<p></p><p>**Accuracy**</p>|<p></p><p>**Loss**</p>||||||||
| :-: | :-: | :-: | :- | :- | :- | :- | :- | :- | :- |
||<p></p><p>**train**</p>|<p></p><p>**Validation**</p>|<p></p><p>**Test**</p>|<p></p><p>**train**</p>|<p></p><p>**Validation**</p>|<p></p><p>**Test**</p>||||
|<p>VGG-16</p><p></p>|97\.02%|94\.34%|95\.2%|0\.23|0\.25|0\.19%||||
|<p>VGG – 19</p><p></p>|98%|96%|95%|0\.17|0\.21|0\.1772%||||
|ResNet50V2|98\.9%|97%|92%|0\.13|0\.20|0\.27||||
|DenseNet201|98\.7%|94%|96%|0\.12|0\.18|0\.17||||


**Augmentation:**

`      `**Simple                   Augmented                                  Simple                                  Augmented**

![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.001.jpeg)      ![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.002.jpeg)           ![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.003.jpeg)       ![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.004.jpeg)

![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.005.jpeg)     ![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.006.jpeg)     ![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.007.jpeg)     ![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.008.jpeg)

**VGG-16**

**Fine Tuning**

We applied the VGG-16 model and fine-tuned the last block 5, achieving an accuracy of 99% on the training set. However, the validation accuracy was only 70%, indicating overfitting. There was a significant difference in loss, approximately 25% to 29%.

To mitigate overfitting, we added a dense layer with 128 neurons, applied a dropout of 0.2, and included batch normalization. This adjustment led to an improved performance with a training accuracy of 98% and validation accuracy of 95%. The loss values ranged between 0.25 to 0.30.

**layers:**

1. Flatten
1. Dense with 128 units
1. Dropout 0.2
1. Batch Normalization

![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.009.png)![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.010.png)

**Test Accuracy Confusion Matrix and Classification report:**

![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.011.png)![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.012.png)












**VGG – 19:**

**Removed dropout and batch normalization layer.**

![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.013.png)![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.014.png)

**Test Accuracy Confusion Matrix and Classification report:**

![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.015.png)![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.016.png)











**ResNet50V2:**

![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.017.png)![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.018.png)

**Test Accuracy Confusion Matrix and Classification report:**

![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.019.png)![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.020.png)












**DenseNet121:**

![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.021.png)![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.022.png)

**Test Accuracy Confusion Matrix and Classification report:**

![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.023.png)![](Aspose.Words.31ec207a-5099-4fad-bc7a-7f6326349910.024.png)

**Credit:**

**Hasnain Muavia**
## Authors

- [@HasnainMuavia](https://github.com/HasnainMuavia1)

