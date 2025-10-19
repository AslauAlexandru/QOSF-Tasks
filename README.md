# QOSF Tasks


# Task 4 QSVM

## Results

a. From the output of ``summary(features, labels, scale, pca, embeddings, reps)``, we can see the best model in terms of efficiency and accuracy is achieved with scale status of **False** and PCA status of **True** with **two** PCs, using **angle-pennylane** embedding, with an accuracy of 97 percent. This model uses two qubits, and has a depth of two. 


b. From the output of ``summary(features, labels, scale, pca, embeddings, reps)``, another top combination is with scale status of **False** and PCA status of **True** with **two** PCs, using **amplitude-qiskit** embedding, with an accuracy of 97 percent. This model uses a single qubit, and has a depth of max two.


Let's establish some statistical knowledge from this dataset. We can observe :

1. By **increasing** the number of **reps**, the **accuracy decreases**.
2. By applying **PCA**, the **accuracy slightly drops** and **keeps dropping** as we **decrease** the number of **Principal Componennts**. (However, it provides a **trade-off** between **accuracy** and **depth**, meaning we can have a shallower PQC with a high enough accuracy)
3. We can also see how we can use a **single qubit**, with a **shallow depth** using **amplitude-qiskit** as well as **amplitude-pennylane**, which makes these two encodings the **most efficient**.
4. **Scaling** slightly **improves** the result in case of angle encoding, but not so for amplitude encoding.

Overall, the main points are to observe the tradeoff between the scale of the problem and its accuracy using PCA and encoder, and to achieve an even shallower representation, to exploit the amplitude encoding protocols. What we did in this model was to develop an understanding of the key components that build up QSVM, and how they compare to classical SVM in terms of cost and accuracy for the iris dataset.



