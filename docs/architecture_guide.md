# **Architecture Guide**

The system is built using the following key components:

- The **FastAPI** backend connects the **hardware** and **frontend** to each other and to the **MongoDB** database.
  
- The infrastructure and database are set up using a **Terraform** script that provisions a **MongoDB** cluster. Then, a Python script is used to create the database with two collections:  
  - One holds carts **1 to 10** and logs of items purchased.  
  - The other holds **item**, **nutrition**, and **price** information.
  
- The **frontend** is built using **Swift**, and it acts as a smart cart "tablet" that communicates with the server.
  
- The **hardware** consists of a **TensorFlow** model trained for object detection, and **OpenCV** is used to handle the webcam for object detection. The webcam detects items and sends requests to update the **MongoDB** log via the backend server.
  
### **Key Technologies Used:**  
- **FastAPI**  
- **MongoDB**  
- **Terraform**  
- **Swift**  
- **TensorFlow**  
- **OpenCV**
