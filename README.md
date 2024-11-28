# Emotion Detection for Good Mental Health with---

## Project Description
Please describe your Startup Campus final project here. You may should your <b>model architecture</b> in JPEG or GIF.

## Contributor
| Full Name | Affiliation | Email | LinkedIn | Role |
| --- | --- | --- | --- | --- |
| Hasbi Anshari Simbolon| Politeknik Ganesha Medan | hasbianshrismbln1411@gmail.com | [link](www.linkedin.com/in/hasbiansharisimbolon) | Team Lead |
| Aldona Septiana | Universitas Amikom Purwokerto | aldonaseptiana19@gmail.com | [link]() | Team Member |
| Satriawan Adinugroho | Universitas Mercu Buana Yogyakarta | satriawan2210@gmail.com | [link]() | Team Member |
| M. Saifuddin Eka N | Universitas Sebelas Maret| masoodinc1@gmail.com | [link]() | Team Member |
| Amin Ridho A | Politeknik Negeri Sriwijaya | aminridhoa@gmail.com | [link]() | Team Member |
| Feni Fitriani | Sekolah Tinggi Teknologi Terpadu Nurul Fikri | fenifitriani59@gmail.com | [link]() | Team Member |
| Aries Fitriawan | Startup Campus, AI Track | aries.f1991@gmail.com | [link](https://www.linkedin.com/in/ariesfitriawan/) | Supervisor |

## Setup
### Prerequisite Packages (Dependencies)
- pandas
- numpy
- re
- BeautifulSoup
- metrics
- openai
- torch
- BerTokenizer
- AutoTokenizer
- transformers


### Environment
| | |
| --- | --- |
| CPU | Google Colaboratory |
| GPU | Python 3 Google Compute Engine backend |
| ROM | - |
| RAM | 15 GB |
| OS | - |

note : Google Colaboratory

## Dataset
Describe your dataset information here. Provide a screenshot for some of your dataset samples (for example, if you're using CIFAR10 dataset, then show an image for each class).
- Sumber Dataset: Dataset GoEmotions dari Kaggle(https://www.kaggle.com/datasets/debarshichanda/goemotions)

  Deskripsi : GoEmotions adalah kumpulan data berisi 58.009 komentar yang dikurasi dengan hati-hati dari Reddit, dilabeli secara manual ke dalam 27 kategori emosi. Dataset ini dikembangkan untuk analisis emosi dalam teks pendek dengan panjang maksimal 30 kata.
- Kategori yang Dipilih dalam final projek ini:
- Dari 27 label emosi asli, kami menggunakan subset dari 6 kategori berikut:
  - Caring (Peduli)
  - Love (Cinta)
  - Gratitude (Rasa Syukur)
  - Sadness (Kesedihan)
  - Fear (Ketakutan)
  - Anger (Kemarahan)
- Contoh Format Dataset
![image](https://github.com/user-attachments/assets/659cd184-3da3-4b98-babf-5bd0d7c3e01a)

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

| model | epoch | learning_rate | batch_size | optimizer | val_loss | val_precision | val_recall | val_f1 | note | 
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| roberta | 20 |  2e-5 | 64 | AdamW | 0.221 | 84% | 85% | 85% | ... |
| bert | 5 | 2e-5 | 8 | AdamW | 0.170 | 84% | 82% | 83% | ... |
| Svm (OnevsRest) | - | - | - | - | - | 81% | 75% | 78% | Kernel: linear, C: 10, gamma: 0.1 |

#### 2. Ablation Study
Any improvements or modifications of your base model, should be summarized in this table. Feel free to adjust the columns in the table below.

| model | embedding_type | encoder | attention_layer | dropout | val_acc |
| --- | --- | --- | --- | --- | --- |
| roberta | RoBERTa embeddings | RoBERTa | yes | - | 85% |
| bert | pre-trained bert | transformer encoder |yes | 0.5 | 95% |
| Svm (OnevsRest) | TF-IDF | SVM (One-vs-Rest) | - | - | 72% |


#### 3. Training/Validation Curve
Insert an image regarding your training and evaluation performances (especially their losses). The aim is to assess whether your model is fit, overfit, or underfit.
- Model Bert
  ![WhatsApp Image 2024-11-26 at 19 11 16_5c1dc2a0](https://github.com/user-attachments/assets/486b3391-70db-4fc8-a95e-5e28a0bf81a7)

- Model Roberta
  
 ![WhatsApp Image 2024-11-26 at 19 21 02_f49e05b3](https://github.com/user-attachments/assets/d016ce4b-c0ad-4d7c-b5c9-7465827cebf5)

### Testing
Show some implementations (demos) of this model. Show **at least 10 images** of how your model performs on the testing data.

- Model Bert

![WhatsApp Image 2024-11-26 at 19 45 14_ccf73a68](https://github.com/user-attachments/assets/f995b5ea-4a86-47a7-bb6a-4e6380b295ee)


### Deployment (Optional)
Describe and show how you deploy this project (e.g., using Streamlit or Flask), if any.

## Supporting Documents
### Presentation Deck
- Link: https://...

### Business Model Canvas
Provide a screenshot of your Business Model Canvas (BMC). Give some explanations, if necessary.

### Short Video
Provide a link to your short video, that should includes the project background and how it works.
- Link: https://...

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
This project entitled <b>"YOUR PROJECT TITLE HERE"</b> is supported and funded by Startup Campus Indonesia and Indonesian Ministry of Education and Culture through the "**Kampus Merdeka: Magang dan Studi Independen Bersertifikasi (MSIB)**" program.
