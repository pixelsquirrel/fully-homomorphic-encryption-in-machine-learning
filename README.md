Fully Homomorphic Encryption (FHE) enables computations on encrypted data without the need to decrypt it. This ensures strong data privacy when leveraging cloud computing services. In particular, FHE allows machine learning models to be trained and evaluated on confidential data without exposing it to third-party servers.

### Overview

This project demonstrates the use of FHE for training a logistic regression model to predict utility debt. The workflow is divided into two main steps:
1. Client-side encryption: The dataset is encrypted before being sent to the server.
2. Server-side training and evaluation: The model is trained and evaluated directly on the encrypted data.

### Results

| Parameter      | Value |
| --- | --- |
| Original dataset file size (CSV)  | 38 274 KB  |
| Size of one encrypted vector (hex)  | 428 KB  |
| Time to encrypt one array (2200 × 23) | 45 seconds  |
| Model accuracy on encrypted data  | 86.13 %  |
| Model accuracy on unencrypted data  | 86.13 %  |
| Average training time on encrypted data  | 202 seconds  |

The logistic regression model achieves the same accuracy on encrypted data as on unencrypted data, demonstrating that FHE can provide strong data protection without degrading predictive performance.

### Considerations

While FHE ensures maximum data privacy, it introduces additional computational overhead, including increased data size and longer training times. Users should balance security requirements with performance constraints when applying FHE in practical scenarios.