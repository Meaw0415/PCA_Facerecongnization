# PCA_Face_recngnization

Referenced from https://www.geeksforgeeks.org/ml-face-recognition-using-eigenfaces-pca-algorithm/

Trainng with PCA face recongnization.

1. For each image(w*h) convert in  into w*h*1 vecotr.

2. For all images convert them into (w*h,n) matrix. That is what we want to input.

3. Start PCA algorthim:  
    
    1. Decentralized. Calculate the average of all these face vectors and subtract it from each vector. 

    2. Find convarience matrix by Conv = np.dot(A.T,T)   
    ![img](https://www.geeksforgeeks.org/wp-content/ql-cache/quicklatex.com-2abfb5b3ae1d2973a0f3c5be78a57633_l3.svg)
    3. Select K largest eigenvalues' eigenvectors as our eigenface.
    4. Use this eigenface to map the original matrix to low-rank face matrix   
        
        face = np.dot(pca_face_k,facematrix0)

4. Now we calculate the weight of each eigenfaces.
    ![img](https://www.geeksforgeeks.org/wp-content/ql-cache/quicklatex.com-f9fc0d956d2838c9766c8f7868ddbd97_l3.svg)  

    And its corresponding coefficient.
    ![img](https://www.geeksforgeeks.org/wp-content/ql-cache/quicklatex.com-d364fff8c5d711f478b6669c176473dc_l3.svg)  

5. Now we can use this weight to do face recognization.

6. We use the projection(eigen_face) above to get a coefficient vector

7. Calculate the Euclidean distance(Norm) between the img we input and each img in dataset.

8. Find the smallerst one(argmin).
