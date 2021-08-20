# cat and dog custom object detection with TensorFlow2 
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DMBabich/cat_dog_custom_object_detection/blob/main/CV_OD_ALL.ipynb)
---
---
[RUS Task](https://github.com/DMBabich/cat_dog_custom_object_detection#rus)

[ENG Task](https://github.com/DMBabich/cat_dog_custom_object_detection#eng)

[Plot](https://github.com/DMBabich/cat_dog_custom_object_detection#eng)

[Conclusion](https://github.com/DMBabich/cat_dog_custom_object_detection#conclusion)

[Links](https://github.com/DMBabich/cat_dog_custom_object_detection#links)

---
---
### Rus
Датасет содержит изображения, на каждом из которых присутствует по одному объекту и файл разметки для каждого изображения.
<br>Разметка имеет вид: *class, bbox_xmin, bbox_ymin, bbox_xmax, bbox_ymax*

Необходимо решить задачу локализации и классификации объекта на изображении, создав и обучив 
две  нейронные  сети:  первая  должна  быть  реализована  с  применением  transfer  learning,  вторая  – 
представлять собой собственную CNN с пятью выходами (метка класса и координаты bbox'а). 
<br>В качестве метрик точности должны применяться mIoU и accuracy классификации.

Для аугментации использовалась библиотека [albumentation](https://albumentations.ai/), потому что она масштабирует bbox вместе с изображением.

---
### Eng
The dataset contains images, each of which contains one object and a markup file for each image.
<br>The markup looks like: *class, bbox_xmin, bbox_ymin, bbox_xmax, bbox_ymax*

It is necessary to solve the problem of localization and classification in the image by creating and training two neural networks: the first should be implemented using the learning transfer method, the second - its own CNN model with five outputs (class label and bbox coordinates).
<br>MIoU and classification accuracy should work as precision metrics.

The [albumentation](https://albumentations.ai/) library was used for augmentation because it scales the bbox along with the image. 

---
---

## Plot

_Custom CNN Model_

[Architecture](https://github.com/DMBabich/cat_dog_custom_object_detection/blob/main/plots/Custom_detection_CNN.png)
<br>[Accuracy](https://github.com/DMBabich/cat_dog_custom_object_detection/blob/main/plots/small_Custom_CNN_acc.png)
<br>[mIoU](https://github.com/DMBabich/cat_dog_custom_object_detection/blob/main/plots/small_Custom_CNN_mIoU.png)
<br>[Prediction](https://github.com/DMBabich/cat_dog_custom_object_detection/blob/main/plots/prediction_custom.png)


_Transfer CNN Model (VGG16)_

[Architecture](https://github.com/DMBabich/cat_dog_custom_object_detection/blob/main/plots/Transfer_detection_VGG16.png)
<br>[Accuracy](https://github.com/DMBabich/cat_dog_custom_object_detection/blob/main/plots/small_Transfer_VGG16_CNN_acc.png)
<br>[mIoU](https://github.com/DMBabich/cat_dog_custom_object_detection/blob/main/plots/small_Transfer_VGG16_CNN_mIoU.png)
<br>[Prediction](https://github.com/DMBabich/cat_dog_custom_object_detection/blob/main/plots/prediction_transfer_learning.png)

---

## Conclusion

As you can see - custom model better prediction bbox coordinates. But classificator undertrained.
<br>Also transfer model have better classificator. But bbox coordinates is very bad.

**It's a training project. You can make it better :)**
<br>_How?_
<br>Try:
- [ ] Make more augmentation data and add more test data
- [ ] Edit depth of models
- [ ] Tune a models better

---

## Links

- [X] [Custom model CNN](https://drive.google.com/file/d/1pnvjx2klYlTPiPhJXVzaLNMkboPZ8M0u/view?usp=sharing)
- [X] [Transfer model CNN](https://drive.google.com/file/d/1PgLgtM1cprIpNDoCALg-9Sq4YWZVzeOL/view?usp=sharing)
- [X] [Dataset](https://drive.google.com/file/d/1Lgq5KD9ZrW1WTeIVGgNyL32wv3YHOn-1/view?usp=sharing)
