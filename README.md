# Satellite-Image-Prediction

## Keywords : 
  Supervised Learning ,Classification Task, TransferLearning, Deep Learning, CNN, VGG16, MobileNet

## WORKFLOW
1. Dataset : About , Load, Visualize, Data generators(Augment)
2. Model : About, Load, Do tweaks( Freeze, Remove top, Add Top) , Compile
3. Performance : Train, Evaluate

## Libraries Used : 
  1. OpenCV
  2. OS 
  3. Time
  4. MatplotLib 
  5. Numpy
  6. Pandas
  7. TensorFlow
  8. Keras
  9. SkLearn 

## Satellite Image Classification Dataset :
  1. Total Samples = 5631
  2. Classes = Cloudy, Desert, Green Area, Water
  3. Count of data points in each class :
  
  ![image](https://user-images.githubusercontent.com/52949047/181217384-d0790f51-dce2-40cf-87c5-dc3748f9af1b.png)
 
 4. Samples : 
  
  ![image](https://user-images.githubusercontent.com/52949047/181217594-e562bad9-79aa-46fb-9eb4-05de000c2fd7.png)
  
## Models Used : 
  1. VGG16 : 
    
  ![image](https://user-images.githubusercontent.com/52949047/181711116-ff0559e6-4584-4482-b1e2-606b75fcb414.png)
  
  a. Uses three stacked 3*3 layer with same padding instead of one 7*7 layer, and one 2*2 layer       with valid padding.
  b. Converges Faster
  c. Reduces the number of parameters : 14M in VGG16 ( 16 trainable layers), 61M parameters in        AlexNet(8 trainable layers) 
     In 3 layers VGG16 : 3 * 3 * 3 * input channels * output channels = 27C^2
     In 1 layer of AlexNet : 7 * 7 * input channels * output channels = 49C^2
  
  2. MobileNet :
  
  ![image](https://user-images.githubusercontent.com/52949047/181712530-6c73cf8c-a427-42bc-8216-09dc80f62105.png)


  a. DepthWise Separable Convolution 
    Uses depthwise Convolution , stacked with pointwise convolution
  
  b. Reduces Number of parameters
  
  
    
  
## Testing accuracy : 
 1. VGG16 : 98.31%
 
 ![image](https://user-images.githubusercontent.com/52949047/181220454-01488a66-8fe2-4605-806c-9a518f793d45.png)

 2. MobileNetV2 :98.04% 
 
 ![image](https://user-images.githubusercontent.com/52949047/181220501-f17ccd80-b1b7-4003-9b25-ef456dcbbe01.png)

 ## Confusion Matrix for Test Set:
 1. VGG16
 
  ![image](https://user-images.githubusercontent.com/52949047/181219884-95fc1981-cad8-41d0-a10e-17c810415cb5.png)
  
 2. MobileNetV2
 
 ![image](https://user-images.githubusercontent.com/52949047/181220654-3016a08f-efdf-4c49-a096-6a4c9c1c3135.png)


 ## Classification Report for Test Set : 
 1. VGG16
 
 ![image](https://user-images.githubusercontent.com/52949047/181220029-d2973d42-6c2f-4610-9027-5c49fdb64b18.png)

 2. MobileNetV2
 
  ![image](https://user-images.githubusercontent.com/52949047/181220695-75929d79-21ec-455b-9342-6d03369d2043.png)

  ## Predictions on Random Samples
  1. VGG16
  
  ![image](https://user-images.githubusercontent.com/52949047/181220265-445c4c9b-2e94-4073-a972-3aaffb6afe30.png)
  
  2. MobileNetV2
  
  ![image](https://user-images.githubusercontent.com/52949047/181220568-a393c6c4-ad4d-4eb6-9bd2-6246f6be261b.png)

  
