# FINAL PROJECT TITLE HERE

## Project Description
Please describe your Startup Campus final project here. You may include your model architecture in JPEG or GIF.

## Contributor
| Full Name | Affiliation | Email | Role |
| --- | --- | --- | --- |
| ... | ... | ... | ... |
| ... | ... | ... | ... |
| Nicholas Dominic | Startup Campus, AI Track | nic.dominic@icloud.com | Supervisor |

## Setup
### Prerequisite Packages (Dependencies)
- package name (version: ...)
- package name (version: ...)
- pandas==2.1.0
- openai==0.28.0
- google-cloud-aiplatform==1.34.0
- google-cloud-bigquery==3.12.0

### Environment
| | |
| --- | --- |
| CPU | Example: Apple M3 Pro 12-core CPU |
| GPU | Example: Nvidia A100 (x1) |
| ROM | Example: 1 TB SSD |
| RAM | Example: 36 GB |
| OS | Example: macOS Sonoma v14.1.1 |

## Dataset
Describe your dataset information here. Provide a screenshot for some of your dataset samples (for example, if you're using CIFAR10 dataset, then show an image for each class).

## Results
### Model Performance
Describe all results found in your final project experiments, including hyperparameters tuning and architecture modification performances. Put it into table format. Please show pictures (of model accuracy, loss, etc.) for more clarity.
1. Metrics
   | model | epoch | learning_rate | batch_size | optimizer | loss | acc | f1_score | ... |
   | --- | --- | --- | --- | --- | --- | --- | --- | --- |
   | vit_b_16 | 1000 |  0.0001 | 32 | Adam | 0.093 | 88.34% | 84.15% | ... |
   | vit_l_32 | 2500 | 0.00001 | 128 | SGD | 0.041 | 90.19% | 87.55% | ... |
   | ... | ... | ... | ... | ... | ... | ... | ... | ... | 

2. Ablation Study
   | model | layer_A | layer_B | layer_C | ... | top1_acc | top5_acc |
   | --- | --- | --- | --- | --- | --- | --- |
   | vit_b_16 | Conv(3x3, 64) x2 | Conv(3x3, 512) x3 | Conv(1x1, 2048) x3) | ... | 77.43% | 80.08% |
   | vit_b_16 | Conv(3x3, 32) x3 | Conv(3x3, 128) x3 | Conv(1x1, 1028) x2) | ... | 72.11% | 76.84% |
   | ... | ... | ... | ... | ... | ... | ... | 
 
### Testing
Show some implementations (demos) of this model. For example, if your team works on object detection tasks, show an image or a video (or GIF) of how your model performs on the testing data.

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
This project entitled <b>YOUR PROJECT TITLE HERE</b> is supported and funded by Startup Campus Indonesia and Indonesian Ministry of Education and Culture through the "Kampus Merdeka: Magang dan Studi Independen Bersertifikasi (MSIB)" program.
