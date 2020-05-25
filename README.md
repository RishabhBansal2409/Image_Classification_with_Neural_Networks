# Image_Classification_with_Neural_Network

I have built a **Logistic Regression cum Neural Network model which recognizes if a cat is present in an image or not**.
This model can serve as a basis for more sophisticated model which will **check if a person is wearing a mask or not on a real time basis given the current COVID-19 crisis**.

### Datasource :-

Both Training and Testing Data are given in an **h5 file format** (file saved in the Hierarchical Data Format (HDF)).    
These files contain **multidimensional arrays of images** which is nothing but **collection of pixels** where a pixel is represented by 3 values each describing the **intensity of Red , Blue and Green (R,G,B) channels**.

### Data Pre-Processing :-

Common steps undertaken for pre-processing the dataset are as follows:
- Figuring out the **dimensions and shapes** of the problem (m_train, m_test, width, height,...)
- Reshaping the datasets such that **each example is now a vector of size (width \* height \* 3, 1)**.
- **Standardizing the data**.

### Alogrithm Architecture :-

![](/images/Algorithm_Architecture)


Essence of the architecture is that **features (R,G,B intensity for each pixel) belonging to an image are multiplied with the weights (determined by the network by reducing the cost function) which when with added with a scalar known as bias (determined in the same fashion as that of weights) acts as an input to the sigmoid/tanh or function of that sorts.THe output of these functions is probability which can be used to classify the cat vs non cat image based on the threshold (usually 0.5) set by the modeler**.   

Key steps involved are as follows:   

   - Initialize the parameters , weights (w) and bias (b) of the model with zeros.  
   - Compute the **Activation function (A) and the Final Cost (J) using Forward Propagation**.  
   - Compute the **gradients w.r.t the weights and the bias using Backward Propagation**.  
   - Learn the **parameters for the model by minimizing the cost** using the gradient descent update rule.  
   - Use the learned parameters to **make predictions (on the test set)**.    
   - Analyse the results and conclude.
