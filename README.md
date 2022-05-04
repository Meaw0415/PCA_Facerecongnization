# PCA_Face_recongnization

Referenced from https://www.geeksforgeeks.org/ml-face-recognition-using-eigenfaces-pca-algorithm/

Trainng with PCA face recongnization.

1. For each image(w*h) convert in  into w*h*1 vecotr.

2. For all images convert them into (w*h,n) matrix. That is what we want to input.

3. Start PCA algorthim:  
    
    1. Decentralized. Calculate the average of all these face vectors and subtract it from each vector. 

    2. Find convarience matrix by Conv = np.dot(A.T,T)   
    ![img](https://www.geeksforgeeks.org/wp-content/ql-cache/quicklatex.com-2abfb5b3ae1d2973a0f3c5be78a57633_l3.svg)
    3. 
    4. asdasd  