# **Setup Guide**

## **1. Running the Swift Frontend**  
To use the NutriCart app, you'll need an iOS device:  
1. Clone the frontend repository to your Mac.  
2. Open the project in Xcode.  
3. Build and run the app on an iPhone or iOS simulator.  

## **2. Running the Hardware Repo**  
The hardware component requires:  
- A device that can run Python  
- A webcam for object detection  

### **Steps:**  
1. Clone the hardware repository.  
2. Position the webcam inside a **cardboard box** to create an optimal detection environment—ensure it doesn’t capture the floor or anything above it.  
3. Run the object detection script in the hardware repo.  

By default, the **hardware repo auto-connects to Cart 2**, but this can be changed in the settings.  

## **3. Setting Up the Infrastructure (Terraform & Database)**  
1. Navigate to the Terraform repository.  
2. Set up the necessary environment variables for Terraform.  
3. Run:  
   ```sh
   terraform init
   terraform apply
   ```
4. Once the infrastructure is deployed, run the `populate_database.py` script to seed the database.  

## **4. Running the Backend**  
- You can **self-host** the backend or use the hosted version:  
  **[https://hackru-spring-2025-backend.onrender.com](https://hackru-spring-2025-backend.onrender.com)** (if available).  
- If self-hosting, ensure that REST API requests in the frontend are updated accordingly.  

## **5. Using the System**  
1. Connect to Cart 2 in the Swift app (or change it if needed - it can be between 1 - 10).  
2. Input body stats manually or allow automatic calorie/macronutrient goal entry.  
3. Scan grocery items with the webcam, and they will be added to the app.  
4. When checkout is pressed, the cart is cleared, and the items are checked out.  
