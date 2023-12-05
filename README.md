# *"Rubber Guardian"* Tire Quality Detection and Classification

## Project Description
"Rubber Guardian" is a project created for Final Project in MSIB Startup Campus Track Artificial Intelligence. This product is an innovative solution designed to revolutionize the tire industry by ensuring uncompromised quality through advanced detection and classification technology. This cutting-edge system employs state-of-the-art artificial intelligence and machine learning algorithms to meticulously inspect and categorize tires during the manufacturing process. The primary objective is to enhance quality control, minimize defects, and ultimately improve overall safety and performance

## Contributor
| Full Name | Affiliation | Email | LinkedIn | Role |
| --- | --- | --- | --- | --- |
|Octa Miraz       |Universitas PGRI Yogyakarta         |                           |[Link](https://www.linkedin.com/in/octa-miraz-b58102145/)| Team Leader      |
|Alya Fauziah     |Institut Teknologi Telkom Purwokerto|alyafauziyah6175@gmail.com |[Link](www.linkedin.com/in/alyafauziyah/)|Team Member      |
|Andi Zulfikar    |Universitas Islam Bandung           |                           |                                     |Team Member     |
|Hanina Nafisa A. |Universitas Sebelas Maret           |haninafisazka@gmail.com    |[Link](www.linkedin.com/in/haninanafisaazka/)|Team Member     |
|Risnaldy N.I     |UPN "Veteran" Jawa Timur            |risnaldy19@gmail.com       |[Link](www.linkedin.com/in/risnaldynovendra/)|Team Member     |
|Ryanza Aufa Y.   |UPN "Veteran" Jakarta               | ryanzaufay18@gmail.com    |[Link](www.linkedin.com/in/ryanza-aufa-yansa-669b0a221/)|Team Member    |

## Setup
### Prerequisite Packages (Dependencies)
- pandas==2.1.0
- openai==0.28.0
- google-cloud-aiplatform==1.34.0
- google-cloud-bigquery==3.12.0
- ...
- ...

### Environment
| | |
| --- | --- |
| CPU | Example: Apple M3 Pro 12-core CPU |
| GPU | Example: Nvidia A100 (x1) |
| ROM | Example: 1 TB SSD |
| RAM | Example: 36 GB |
| OS | Example: macOS Sonoma v14.1.1 |

## Dataset
The dataset that we used is sourced from Kaggle, consisting of two classes: defective and good. There are 1028 images of defective tires and 828 images of good tires in the dataset.

However, the dataset we acquired has varied sizes. Therefore, we conducted preprocessing by resizing the images to 512x512. Additionally, we divided our dataset into training and testing sets. For the training set, we utilized 822 images of defective tires and 622 images of good tires. Meanwhile, for the testing set, we needed 206 images of defective tires and 166 images of good tires. Consequently, the total number of images we used amounts to 1856.

Moreover, we implemented data augmentation techniques to enhance the quality of our dataset. We applied vertical and horizontal flips, 90-degree rotation, and Gaussian blur during the augmentation process.

- Link Kaggle : [Dataset Rubber Guardian](https://bit.ly/Dataset-Rubber-Guardian)


## Results
### Model Performance
Describe all results found in your final project experiments, including hyperparameters tuning and architecture modification performances. Put it into table format. Please show pictures (of model accuracy, loss, etc.) for more clarity.

#### 1. Metrics
Inform your model validation performances, as follows:
- For classification tasks, use **Precision and Recall**.
- For object detection tasks, use **Precision and Recall**. Additionaly, you may also use **Intersection over Union (IoU)**.
- For image retrieval tasks, use **Precision and Recall**.
- For optical character recognition (OCR) tasks, use **Word Error Rate (WER) and Character Error Rate (CER)**.
- For adversarial-based generative tasks, use **Peak Signal-to-Noise Ratio (PNSR)**. Additionally, for specific GAN tasks,
  - For single-image super resolution (SISR) tasks, use **Structural Similarity Index Measure (SSIM)**.
  - For conditional image-to-image translation tasks (e.g., Pix2Pix), use **Inception Score**.

Feel free to adjust the columns in the table below.

| model | epoch | learning_rate | batch_size | optimizer | val_loss | val_precision class 0 | val_recall class 0 | val_precision class 1 | val_recall class 1 |

| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ResNet50 | 150 |  0.001 | 32 | SGD | 0.036 | 97.85% | 98% | 93% | 92% | 98%
| vit_l_32 | 2500 | 0.00001 | 128 | SGD | 0.041 | 90.19% | 87.55% | ... |
| ... | ... | ... | ... | ... | ... | ... | ... | ... | 

#### 2. Ablation Study
Any improvements or modifications of your base model, should be summarized in this table. Feel free to adjust the columns in the table below.

| model | fully connected layer | top1_acc | top5_acc |

| --- | --- | --- | --- | --- | --- | --- |
| ResNet50 | Linear(2048, 1024) x1, Linear(1024, 512) x1, Linear(512, 256) x1, Linear(256, 2) x1, ReLU() x3, Dropout(0.5) x2 | 55.37% | 90.86% |
| vit_b_16 | Conv(3x3, 32) x3 | 72.11% | 76.84% |
| ... | ... | ... | ... | ... | ... | ... |

#### 3. Training/Validation Curve
Insert an image regarding your training and evaluation performances (especially their losses). The aim is to assess whether your model is fit, overfit, or underfit.
 
### Testing
Show some implementations (demos) of this model. Show **at least 10 images** of how your model performs on the testing data.

### Deployment (Optional)
Describe and show how you deploy this project (e.g., using Streamlit or Flask), if any.

## Supporting Documents
### Presentation Deck
- Link: Rubber Guardians's [Presentation Deck](https://drive.google.com/file/d/165V4WECq-jD6kIgnRtFFQz5yRRgFxheT/view?usp=sharing) 

### Business Model Canvas
Provide a screenshot of your Business Model Canvas (BMC). Give some explanations, if necessary.

### Short Video
Background project for [Rubber Guardian](https://drive.google.com/file/d/1hBedE9WZkkGswuJ2WN2ZxyYSEdUPnUk8/view?usp=sharing)

## References
Provide all links that support this final project, i.e., papers, GitHub repositories, websites, etc.
- Link: https://...
- Link: https://...
- Link: https://...

## Additional Comments
Provide your team's additional comments or final remarks for this project. For example,
1. ...
2. ...
3. ...

## How to Cite
If you find this project useful, we'd grateful if you cite this repository:
```
@article{
...
}
```

## License
For academic and non-commercial use only.

## Acknowledgement
This project entitled <b>"Rubber Guardian" Tire Quality Detection and Classification</b> is supported and funded by Startup Campus Indonesia and Indonesian Ministry of Education and Culture through the "**Kampus Merdeka: Magang dan Studi Independen Bersertifikasi (MSIB)**" program.
