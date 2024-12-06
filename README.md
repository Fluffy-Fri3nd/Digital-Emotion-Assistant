# EmoCare: Digital Emotion Assistant for Mental Health

## Project Description
The **Emotion Detection** project focuses on developing a web-based application that analyzes and predicts emotions from text input. Using a machine learning model, this application identifies six different emotional states from the text: **Caring**, **Love**, **Gratitude**, **Sadness**, **Fear**, and **Anger**.
This application features an interactive and visually appealing interface, using a dynamic bar chart to visualize the emotion predictions and offering suggestions based on the detected emotions. The background dynamically adjusts according to the user's mouse position, creating an immersive experience.

### Benefits
- **Enhanced Emotional Awareness**: Helps users understand the emotions conveyed in their written text, promoting self-reflection and emotional intelligence.
- **Visual Insights**: The emotion predictions are displayed in a bar chart with probabilities, giving users a clear overview of their emotional state.
- **Personalized Suggestions**: Provides actionable suggestions based on predicted emotions, guiding users toward positive actions or reflections.
- **Interactive UI**: The user interface is designed with dynamic background changes and an intuitive layout, making the app fun and easy to use.
- **Real-time Emotion Analysis**: Predictions are made in real time, giving users immediate feedback on the emotional content of their input.

### Features
- **Emotion Prediction**: Predicts six types of emotions from text input, including Caring, Love, Gratitude, Sadness, Fear, and Anger.
- **Bar Chart Visualization**: Uses a **Bar chart** (powered by **Chart.js**) to visually represent the probability of each detected emotion.
- **Fast and Responsive**: The app processes text and returns emotion predictions within seconds, ensuring quick feedback.
- **Suggestion Generation**: After emotion predictions, users can receive tailored suggestions based on their detected emotions (e.g., "Feeling grateful? Try expressing your gratitude in writing!").
- **Dynamic Background**: The background of the app changes in real time based on the user's mouse position, creating a responsive and visually engaging experience.
- **Text Input Area**: Users can input text (up to 300 characters), and the system will predict the emotions behind it.
- **Example Input**: A feature to populate the text area with an example input for ease of use.

## Contributor
| Full Name | Affiliation | Email | LinkedIn | Role |
| --- | --- | --- | --- | --- |
| Hasbi Anshari Simbolon| Politeknik Ganesha Medan | hasbianshrismbln1411@gmail.com | [link](www.linkedin.com/in/hasbiansharisimbolon) | Team Lead |
| Aldona Septiana | Universitas Amikom Purwokerto | aldonaseptiana19@gmail.com | [link]() | Team Member |
| Satriawan Adinugroho | Universitas Mercu Buana Yogyakarta | satriawan2210@gmail.com | [link]() | Team Member |
| Muhammad Saifuddin E N | Universitas Sebelas Maret| masoodinc1@gmail.com | [link](https://www.linkedin.com/in/m-saifuddin/) | Team Member |
| Amin Ridho A | Politeknik Negeri Sriwijaya | aminridhoa@gmail.com | [link](http://linkedin.com/in/aminridhoalhafidz) | Team Member |
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
  ![image](https://github.com/user-attachments/assets/ecbf73db-e109-40b2-8484-52749b6d5de3)


- Model Roberta
  
 ![image](https://github.com/user-attachments/assets/d016ce4b-c0ad-4d7c-b5c9-7465827cebf5)

### Testing
Show some implementations (demos) of this model. Show **at least 10 images** of how your model performs on the testing data.

- Model Bert

![image](https://github.com/user-attachments/assets/54c5c1c1-3b2f-4182-8887-4825792a8e88)
![image](https://github.com/user-attachments/assets/15bb1b53-fdf5-4aa4-9d85-6a3358045c6f)
![image](https://github.com/user-attachments/assets/e10e2c24-2251-4866-ba4a-2e89a04ff95d)
![image](https://github.com/user-attachments/assets/cb3d95a4-f325-45c9-8247-b35f9f1fedb4)
![image](https://github.com/user-attachments/assets/26f167a9-7753-4f29-bc8c-137cf36aedf6)
![image](https://github.com/user-attachments/assets/c5021de5-daf1-4ab4-ba38-4b70e0fafde3)
![image](https://github.com/user-attachments/assets/20a8b107-b678-493d-ad4e-94d84b22577d)
![image](https://github.com/user-attachments/assets/8eb26bef-b055-40b7-ba99-7f126c778cbd)
![image](https://github.com/user-attachments/assets/db823151-d4c5-4e25-90e2-8f828af3cbbc)
![image](https://github.com/user-attachments/assets/437ea2bb-4c05-4957-add8-985144ced0b1)
![image](https://github.com/user-attachments/assets/6288081f-05ae-4a59-83f0-a8f1e38a9204)


### Deployment
![image](https://github.com/user-attachments/assets/0b647a91-39a3-4a7a-8b03-2fd9cc9f1232)


#### Overview
This project implements a robust and scalable web application using a modern frontend-backend architecture. The frontend is built with React, providing a dynamic and responsive user interface, while the backend is developed using FastAPI, ensuring high performance and ease of API development.

#### Frontend Deployment 
For deployment, the React frontend is hosted on Vercel, a platform optimized for modern web development. Vercel simplifies the deployment process with features like automatic builds and easy integration with Git repositories, ensuring fast and efficient delivery of the frontend.

#### Backend Deployment
The FastAPI backend is deployed on Hugging Face Spaces, a platform tailored for hosting machine learning models and APIs. Hugging Face Spaces allows straightforward deployment by uploading the backend repository, where it automatically manages the environment setup and server execution. This approach ensures that the backend is accessible through stable and secure endpoints.

#### Deployment Link
- [Emocare App](https://emocare-five.vercel.app/)
- [Frontend Sourcecode](https://github.com/Fluffy-Fri3nd/EmoCare.git)
- [Backend Sourcecode](https://github.com/Fluffy-Fri3nd/EmoCare_API.git)

## Supporting Documents
### Presentation Deck
- [Presentation Deck](https://docs.google.com/presentation/d/1podeyZnUNthTiiGFHfMBZm6gUVloEGNF/edit?usp=drive_link&ouid=113800992605900316686&rtpof=true&sd=true)

### Business Model Canvas
Provide a screenshot of your Business Model Canvas (BMC). Give some explanations, if necessary.
![image](https://github.com/user-attachments/assets/271b9e0f-6709-402a-8274-8ec9421d33ed)

### Short Video
Provide a link to your short video, that should includes the project background and how it works.
- [Short Video](https://youtu.be/snWSZvopZKs)

## References
Here are the key references that support this final project:
- **GoEmotions Dataset (Kaggle)**  
  A comprehensive dataset for emotion analysis, used in this project for training emotion detection models.  
  [GoEmotions Dataset](https://www.kaggle.com/datasets/debarshichanda/goemotions)
- **React Documentation**  
  Official documentation to learn and work with React, the frontend framework used in this project.  
  [React Documentation](https://react.dev/learn)
- **Hugging Face Hub Documentation**  
  A platform for sharing machine learning models and datasets. The backend deployment utilizes Hugging Face Spaces.  
  [Hugging Face Documentation](https://huggingface.co/docs/hub/index)
- **Deploy React Application In Vercel**  
  Watch the video how to deploy react app to Vercel.  
  [Watch Video Tutorial](https://youtu.be/IeFlfBR1lxw?si=82ilkhn8ipwtdxKs)
- **Deploying FastAPI Applications to Hugging Face Spaces**  
  Watch the video how to deploy fastAPI to Hugging Face.  
  [Watch Video Tutorial](https://youtu.be/0v9ZsleUuEg?si=BhJM1g6yHdjgC6me)


## Additional Comments
- **Team Collaboration**: This project is the result of a solid team effort with diverse backgrounds, contributing to every stage of development, from data processing to application implementation.
- **Challenges**: Handling the diversity of emotional data and developing a dynamic interface were key challenges, but they were successfully overcome through iteration and collaboration.
- **Mental Health Impact**: EmoCare is expected to help users understand and manage their emotions, supporting overall mental health.
- **Acknowledgments**: We would like to thank all parties who have supported and provided valuable feedback for the development of this application.
- **Hope**: We hope EmoCare can be expanded to various contexts, such as education and workplaces, to enhance empathy and communication.

## How to Cite
If you find this project useful, we'd grateful if you cite this repository:
### BibTeX
```bibtex
@misc{emocare2024,
  author = {Hasbi Anshari Simbolon and Aldona Septiana and Satriawan Adinugroho and Muhammad Saifuddin E N and Amin Ridho A and Feni Fitriani and Aries Fitriawan},
  title = {EmoCare: Digital Emotion Assistant for Mental Health},
  year = {2024},
  url = {https://github.com/Fluffy-Fri3nd/EmoCare},
  note = {Accessed: 2024-12-06}
}
```
### APA
```APA
Simbolon, H. A., Septiana, A., Adinugroho, S., E N, M. S., Ridho A, A., Fitriani, F., & Fitriawan, A. (2024). EmoCare: Digital Emotion Assistant for Mental Health. GitHub repository. https://github.com/Fluffy-Fri3nd/EmoCare
```

### MLA
```MLA
Simbolon, Hasbi Anshari, et al. "EmoCare: Digital Emotion Assistant for Mental Health." GitHub, 2024, https://github.com/Fluffy-Fri3nd/EmoCare.
```

## License
For academic and non-commercial use only.

## Acknowledgement
This project entitled <b>"EmoCare: Digital Emotion Assistant for Mental Health"</b> is supported and funded by Startup Campus Indonesia and Indonesian Ministry of Education and Culture through the "**Kampus Merdeka: Magang dan Studi Independen Bersertifikasi (MSIB)**" program.
