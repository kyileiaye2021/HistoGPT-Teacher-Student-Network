# HistoGPT Pathology Vision Language Model
HistoGPT is a vision language model trained on slide level H&E WSI images (npdi image types) that achieved high performance in report generation, disease classifications, cancer subtyping, and predicting tumor thickness. Here, we are using it for detecting Basal Cell Carcinoma (BCC) skin cancer in Hematoxylin &amp; Eosin images and extending the model's ability to grayscale Optical Coherence Tomography microscopy image domain.

### HistoGPT Architecture
<img width="1750" height="1541" alt="image" src="https://github.com/user-attachments/assets/7b119271-4ab9-4f62-ae0b-0d4e9318f3ae" />


### HistoGPT Vision Module Architecture


```mermaid
flowchart LR
    A[H&E Slides] --> B{{Make Patches}}
    B --> C(Patch Encoder - CTransPath)
    C --> D{Patch Features}
    D -->|Concatenate all Patch Features| E{Slide Features}
    E --> F(Language Module)
    
