
# Weapon-Detection

<div align="center">
  <img height="150" src="https://drive.google.com/uc?id=1L2AJvTsN4-H7bswK1zGTtNYHExhT4wST" alt="Test Set of Gun Detection" width="500"  />
</div>

*Figure: Test Set of Gun Detection*


- Ensuring effective gun detection is vital in contemporary times to address escalating concerns about public safety and combat the increasing occurrences of crimes. 
- This project aims to enhance gun detection models by fine-tuning various deep learning architectures. Our key objectives are as follows:

## 🎯 Goals
- Achieve superior accuracy compared to existing gun detection models.
- Experiment with hyperparameter tuning to find optimal configurations.
- Focus on reducing false positive predictions while increasing precision.
- Develop a robust model that can adapt to different scenarios and perform well in various environments.

## Architectures Used
- VGG16
- YOLOv5
- YOLOv7
- YOLOv8

### ✨ Model Performance Comparison
In this section, we compare the performance of all four models on the test set

| Model   | Precision | Recall | F1 Score | mAP_0.5 | Test Time |
|---------|-----------|--------|----------|---------|-----------|
| Yolov5s | 0.89      | 0.77   | 0.83     | 0.84    | 10s       |
| Yolov7  | 0.81      | 0.73   | 0.80     | 0.80    | 13s       |
| Yolov8s | 0.91      | 0.75   | 0.83     | 0.83    | 9s        |
| VGG16   | 0.86      | 0.85   | 0.82     | 0.81    | 20s       |


## 📚 Dataset
- Download the dataset for custom training
- https://universe.roboflow.com/upc-tf3xi/guns-dataset-j8cz1

## Download Object Detection Models
- Download the object detection models manyally through this link:
- https://drive.google.com/drive/folders/1o37wWBGuH7HGw9sc2HK1VMCc3maSKQuM?usp=sharing


