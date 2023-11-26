# Capstone-project-Amenity-detection-using-DETR-and-Detectron-2-retinanet-

General overview of the project:
  The project's various steps were geared towards achieving the ultimate objective of conducting amenity detection and inventory tracking for Airbnb properties, both indoors and outdoors. This goal was pursued by developing a dedicated web application, which relied on a Deep Neural Network model to carry out object detection tasks. The project was developed following the CRISP-DM methodology. Pert and Gantt charts were used to schedule tasks and ensure deadline adherence. Additionally, Clickup software served as the project management tool for task assignment and progress tracking.
   Thirty-two amenities, such as beds, coffeemakers, lounge chairs, and more, were selected for inclusion. The data for this project was sourced using the simple_image_download library, Roboflow, and the Open Images dataset in its raw form, requiring additional preprocessing. Two hundred images were gathered for each of the 32 categories, resulting in 7,000 images. The data underwent initial preprocessing, which involved identifying and removing duplicates using image hashing techniques and eliminating irrelevant data.
  The image features were annotated using the Labelme tool, producing bounding box coordinates stored in JSON format. Data augmentation techniques, including rotation, noise addition, cropping, and adjustments to hue and brightness, were applied to tackle class imbalance using the Roboflow tool. Subsequently, the images were resized to dimensions of 604 x 640 using the same tool.
  After thoroughly researching and reviewing various literature sources, our team selected five distinct deep-learning models for object detection on the custom dataset. The chosen models for this project were YOLO V7, Detectron 2 (which includes Mask R-CNN, a two-stage model, and RetinaNet, a one-stage model), EfficientDet, and Detection Transformer (DeTr). 
  The selected models were individually trained using the obtained custom dataset. The preprocessed data was stored in the Roboflow tool, and it was divided into a training set (70%), a validation set (20%), and a test set (10%). These datasets were accessed by calling the Roboflow API within the Colab environment. These powerful models demanded significant time and GPU of Nvidia A100 resources for training on the custom dataset. After evaluating the models, it was determined that the YOLO V7 model outperformed all the others, achieving an mAP score of 0.86.
  An interactive web application was created
 using the Streamlit library. Customers had the option to log in or sign up for their accounts. After logging in, hosts and guests could upload pictures of rooms containing amenities. The application integrated the YOLO V7 model to detect objects and identify the amenities. Subsequently, the identified amenities were displayed, and the inventory was stored in a Google Cloud SQL database designed by the team. 
When Airbnb guests logged into the web application, they were allowed to upload images from their Airbnb stay. The application then compared the identified amenities from these images with the inventory list provided by the host for that address to identify any missing items. The benefit of our web application is its stand-alone nature, making it adaptable for use in any domain that requires an object detection or inventory tracking system.

#SYSYEM ARCHITECTURE OF THE WEB APPLICATION:
<img width="664" alt="image" src="https://github.com/SANGAMITHRAMURUGESAN/Capstone-project-Amenity-detection-using-DETR-and-Detectron-2-retinanet-/assets/78456699/32cf3a9b-559e-40b4-a1f5-d7c53e8bda7a">



#INFRENCE ON THE TEST DATA: 


<img width="459" alt="image" src="https://github.com/SANGAMITHRAMURUGESAN/Capstone-project-Amenity-detection-using-DETR-and-Detectron-2-retinanet-/assets/78456699/ef68449e-c2f3-43b7-9b09-2c1cc90fe771">
