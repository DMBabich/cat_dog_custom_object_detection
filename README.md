# cat and dog custom object detection with TensorFlow2
---
---
RUS Task

ENG Task

Plot

Conclusion

Links

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

### Plot

_Custom CNN Model_

[Architecture](https://github.com/DMBabich/cat_dog_custom_object_detection/blob/main/plots/Custom_detection_CNN.png)
<br>[Accuracy](https://github.com/DMBabich/cat_dog_custom_object_detection/blob/main/plots/small_Custom_CNN_acc.png)
<br>[mIoU](https://github.com/DMBabich/cat_dog_custom_object_detection/blob/main/plots/small_Custom_CNN_mIoU.png)


_Transfer CNN Model (VGG16)_

[Architecture](https://github.com/DMBabich/cat_dog_custom_object_detection/blob/main/plots/Transfer_detection_VGG16.png)
<br>[Accuracy](https://github.com/DMBabich/cat_dog_custom_object_detection/blob/main/plots/small_Transfer_VGG16_CNN_acc.png)
<br>[mIoU](https://github.com/DMBabich/cat_dog_custom_object_detection/blob/main/plots/small_Transfer_VGG16_CNN_mIoU.png)

