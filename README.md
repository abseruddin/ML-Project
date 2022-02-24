# ML-Project

Given images of microscopic views of blood components, we need to detect basic blood cell types RBC, WBC,Platelet & their counts from that image

# BCCD_YOLO-V5_Comparison.ipynb
With the help of Icevision framework, we trained 4 models:
	1. Faster-RCNN
	2. YOLO-V5
	3. RetinaNet
	4. EfficientDet
on BCCD Dataset upto 10 epochs. Except Faster-RCNN, we used Transfer Learning. We generated stats based on loss, running time & Mean Average Precision (mAP). It turned out, YOLO-V5 was 'by far' the best model both in terms of Faster Running Time (14 sec) & Mean Average Precision (0.61) [after 10 epochs]. Please see the report for details. 
# BCCD_Without_Augmented_YOLO-V5.ipynb
Here, we trained YOLO-V5 model on original BCCD Dataset from scratch. First, we preprocessed the .xml files to generate .csv & then .txt files in 'appropriate format' for YOLO-V5 model. Then, we trained for 100 epochs generating an overall Mean Average Precision of 0.625. Please see the report for details.
# BCCD_Augmented_YOLO-V5.ipynb
Here, we trained YOLO-V5 model on an augmented (3 times) version of BCCD Dataset (downloaded from Robolow). We trained for 100 epochs generating an overall Mean Average Precision of 0.642. Please see the report for details.
