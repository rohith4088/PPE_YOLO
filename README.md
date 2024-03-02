# RUNNING INSTRUCTIONS

## Clone the repository

git clone https://github.com/rohith4088/PPE_YOLO.git

## Training the model on a custom dataset

The access paths are defined in the data.yaml file.

To train the yolo custom model use:
Yolo task=detect mode=train epochs=100 data=custom.yaml model=yolov8m.pt imgsz=640 batch=8

Yolo is coded in pytorch use the cuda gpu verison of pytorch to accelarate the training precess.

For early stopping use the patiance parameter.

To predict from the webcam use the source parameter as 0.

Yolo task=detect mode=predict model=yolov8m_custom.pt show=True conf=0.5 source=0 (for webcam)