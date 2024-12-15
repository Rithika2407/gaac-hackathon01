
### Framework
![](paper_images/framework.gif)

#### Gibbs-BERT
![](paper_images/gibbs_bert_mask.gif)

#### Example of sentiment control
![](paper_images/sentimentcontrol.jpg)

### Preparation
Please download [CLIP](https://huggingface.co/openai/clip-vit-base-patch32) and [BERT](https://huggingface.co/bert-base-uncased) from Huggingface Space.

SketchyCOCOcaption benchmark in our work is available [here](https://drive.google.com/file/d/1WBaq8OdvyyXpbYtmuFIvko6855rESwHE/view?usp=share_link).

###Zero-Shot Image Captioning
📋 Project Overview
This project enables zero-shot image captioning, allowing users to generate captions for images in languages they choose, even for images the model has never seen before. It leverages Hugging Face Transformers, CLIP, and BERT models to provide versatile and language-independent captions.

🚀 Key Features
Zero-Shot Captioning:

Generates captions for unseen images without prior training on them.
Multilingual Support:

Users can specify captions in any desired language or provide example sentences for guidance.
Easy-to-Use:

Designed for people worldwide, with no language restrictions or barriers.
🛠️ Technologies Used
Python
Hugging Face Transformers
CLIP Model
BERT Model
💡 How It Works
Upload an Image:

Provide an input image that needs to be captioned.
Specify Language/Sentence:

Choose the desired language or provide a reference sentence.
Generate Caption:

The system generates a descriptive caption for the input image in the specified language.
⚙️ Setup and Installation
To run this project locally:

Clone the Repository:

bash
Copy code
git clone <repository-link>  
cd <repository-folder>  
Install Dependencies:
Make sure you have Python and required libraries installed.

bash
Copy code
pip install transformers torch pillow  
Run the Code:
Open the provided Colab Notebook or execute the Python script locally.

🌐 Try It Out on Google Colab
Open the Colab File Here

Run all the cells in the Colab file.
Upload your desired image when prompted.
Select the target language or input a sample sentence for the output caption.
📷 Example Usage
Input Image:
Upload an image of a dog sitting in a park.

Selected Language:
Spanish

Output Caption:
"Un perro sentado en un parque verde."


