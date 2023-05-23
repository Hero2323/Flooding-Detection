# Flooding Detection:
## Classification:
### Features used for Classical Models:
1. LBP Features:
For the local binary patterns, we used the ‘uniform’ method which is grayscale invariant and rotation invariant. We used a radius of 1 (i.e. we calculated the LBP for each pixel using only the 8-neighbourhood). 
2. LBP Histograms: We flatten the LBP features and calculate the histogram on it using 10 bins. 
### Classical Models:
#### 1. K-Means: (K=2, method='uniform')
 The LBP histograms were used as the feature used to train the model. 
|           | Precision (UA) | Recall (PA) | F1-Score | Accuracy |  OE  |  CE  |
|-----------|:--------------:|:-----------:|:--------:|:--------:|:----:|:----:|
| Flooded   |      0.70      |     0.86    |   0.77   |     -    | 0.14 | 0.30 |
| Non-Flooded |      0.81      |     0.64    |   0.72   |     -    | 0.36 | 0.19 |
| Macro Avg |      0.76      |     0.75    |   **0.74**   |  **0.75**   | 0.25 | 0.24 |
#### 2. SVM:
It used the LBP features from the training set as training data.

- Poly kernel, C=3

|           | Precision (UA) | Recall (PA) | F1-Score | Accuracy |  OE  |  CE  |
|-----------|:--------------:|:-----------:|:--------:|:--------:|:----:|:----:|
| Flooded   |      0.53      |     0.81    |   0.64   |     -    | 0.19 | 0.47 |
| Non-Flooded |      0.59      |     0.28    |   0.38   |     -    | 0.72 | 0.41 |
| Macro Avg |      0.56      |     0.54    |   **0.51**   |   **0.54**   | 0.46 | 0.44 |
- RBF kernel, C=3

|           | Precision (UA) | Recall (PA) | F1-Score | Accuracy |  OE  |  CE  |
|-----------|:--------------:|:-----------:|:--------:|:--------:|:----:|:----:|
| Flooded   |      0.80      |     0.59    |   0.68   |     -    | 0.41 | 0.20 |
| Non-Flooded |      0.68    |     0.86    |   0.76   |     -    | 0.14 | 0.32 |
| Macro Avg |      0.74      |     0.72    |   **0.72**   |   **0.72**   | 0.28 | 0.26 |
- RBF, C=3, gamma=0.05

|           | Precision (UA) | Recall (PA) | F1-Score | Accuracy |  OE  |  CE  |
|-----------|:--------------:|:-----------:|:--------:|:--------:|:----:|:----:|
| Flooded   |      0.74      |     0.84    |   0.79   |     -    | 0.16 | 0.26 |
| Non-Flooded |      0.82      |     0.71    |   0.76   |     -    | 0.29 | 0.18 |
| Macro Avg |      0.78      |     0.78    |   **0.77**   |   **0.775**  | 0.22 | 0.22 |
### DL Models:
#### 1. **RegNet16**:
|           | Precision (UA) | Recall (PA) | F1-Score | Accuracy |  OE  |  CE  |
|-----------|:--------------:|:-----------:|:--------:|:--------:|:----:|:----:|
| Flooded   |      1.00      |     0.97    |   0.99   |     -    | 0.03 | 0.00 |
| Non-Flooded |      0.97      |     1.00    |   0.99   |     -    | 0.00 | 0.03 |
| Macro Avg |      0.99      |     0.99    |   **0.99**  |   **0.985**  | 0.01 | 0.01 |
#### 2. ResNet18:
|           | Precision (UA) | Recall (PA) | F1-Score | Accuracy |  OE  |  CE  |
|-----------|:--------------:|:-----------:|:--------:|:--------:|:----:|:----:|
| Flooded   |      0.97      |     0.99    |   0.98   |     -    | 0.01 | 0.03 |
| Non-Flooded |      0.99      |     0.97    |   0.98   |     -    | 0.03 | 0.01 |
| Macro Avg |      0.98      |     0.98    |   **0.98**   |   **0.978**  | 0.02 | 0.02 |
#### 3. MobileNetV2:
|           | Precision (UA) | Recall (PA) | F1-Score | Accuracy |  OE  |  CE  |
|-----------|:--------------:|:-----------:|:--------:|:--------:|:----:|:----:|
| Flooded   |      0.97      |     1.00    |   0.99   |     -    | 0.00 | 0.03 |
| Non-Flooded |      1.00      |     0.97    |   0.99   |     -    | 0.03 | 0.00 |
| Macro Avg |      0.99      |     0.99    |   **0.99**   |   **0.985**  | 0.01 | 0.01 |
## Flooded Pixel Segmentation:
### Supervised:
1. U-Net.
### Unsupervised:
1. ISODATA.
2. K-Means.
### Segemenation :
<p float="left" padding="5px" margin="5px" >
  <img src="https://github.com/Hero2323/Flooding-Detection/blob/main/Inference/segmented_images_resenet18/105.jpg" width="300"  style="margin-right: 15px;" />
  <img src="https://github.com/Hero2323/Flooding-Detection/blob/main/Inference/images/105.jpg" width="300" /> 
</p>

### Collaborators :
<!-- readme: collaborators -start -->
<table>
<tr>
    <td align="center">
        <a href="https://github.com/Hero2323">
            <img src="https://avatars.githubusercontent.com/u/58619697?v=4" width="100;" alt="Abdelrahman Jamal"/>
            <br />
            <sub><b>Abdelrahman Jamal</b></sub>
        </a>
    </td>
    <td align="center">
        <a href="https://github.com/Iten-No-404">
            <img src="https://avatars.githubusercontent.com/u/56697800?v=4" width="100;" alt="Iten-No-404"/>
            <br />
            <sub><b>Iten Elhak</b></sub>
        </a>
    </td>
    <td align="center">
        <a href="https://github.com/radwaahmed2132000">
            <img src="https://avatars.githubusercontent.com/u/56734728?v=4" width="100;" alt="radwaahmed2132000"/>
            <br />
            <sub><b>Radwa Ahmed</b></sub>
        </a>
    </td>
    <td align="center">
        <a href="https://github.com/abdullahalshawafi">
            <img src="https://avatars.githubusercontent.com/u/53022307?v=4" width="100;" alt="abdullahalshawafi"/>
            <br />
            <sub><b>Abdullah Alshawafi</b></sub>
        </a>
    </td></tr>
</table>
<!-- readme: collaborators -end -->
