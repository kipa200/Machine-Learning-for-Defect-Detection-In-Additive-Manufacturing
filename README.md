# Machine-Learning-for-Defect-Detection-In-Additive-Manufacturing

# Abstract
The formation of defects in laser powder bed fusion product is closely related melt pool dynamics. The occurrence of melt pool anomalies such as plume ejection or spattering could result in defects formation. In this project, two machine learning frameworks are proposed for melt pool anomalies detection and classification. 


One class learning with deep convolutional autoencoder was proposed as the first framework for anomalies detection. In this framework, the autoencoder was trained to specialise in reconstructing normal melt pool images. Failing to reconstruct anomalous melt pool images, the autoencoder commits a high reconstruction error. Following that, an appropriate RE threshold was determined through the use of a receiver operating characteristic (ROC) graph. The performance of the autoencoder was also compared with the data pre-sieving model and a newly instantiated autoencoder trained on further cleaned training dataset. This framework does show some promising melt pool anomaly detection performance.
The second framework proposed was an automated features extraction framework. Instead of manual features extraction, this framework utilises the data compressing capability of a disentangled variational autoencoder to extract latent components related to the tail length, size and roundness of melt pool. K-Means Clustering algorithm was then used to compute the distance of data points from their respective cluster’s centroid in the latent space. This distance -based metric was used as an anomaly metric. Furthermore, three supervised classifiers were trained based on these melt pool encodings. Subsequently, this framework enabled the detection of plume, large melt pools and melt pools with unstable tail.


With the classified melt pool anomalies, a case study was conducted to investigate on the formation of build defects. Based on the spike in anomaly metrics, various melt pool anomalies have been detected. It was hypothesised that the build defects were, to a certain extent, caused by these anomalies. Furthermore, the correlation analysis shows slight positive association between the size of melt pools and the average surface depth. 


Finally, future work will focus on training and validating the models with a more diverse melt pool images dataset. With known limitation, the resulting models will then be generic enough to cope for melt pool images produced under different printing parameters.
