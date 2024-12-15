# **Zero-Shot Image Captioning System**  

### **Problem Statement:**  
Develop a model that generates captions for images in **languages it has never been explicitly trained on**. The system must infer linguistic structure from minimal text examples provided in the target language while ensuring **semantic accuracy** and **contextual relevance**.  

---

## **Key Requirements:**  
1. **Zero-Shot Generalization**: No explicit target-language training while achieving accurate and meaningful captions.  
2. **Multimodal Contextual Understanding**: Combine visual features and limited language samples to infer caption structure.  
3. **Efficiency and Scalability**: The system must process images efficiently and adapt to unseen languages.  
4. **Semantic Alignment**: Captions must correctly describe the image content with linguistic coherence.  

---

## **Solution Approach**  
The system leverages a pipeline of **state-of-the-art models and techniques**:  

1. **CLIP (Contrastive Language-Image Pretraining)**  
2. **Language Model (LM) Fine-Tuning**  
3. **Mask Prediction and Prompting**  
4. **Post-Processing for Target Language**  

---

### **Workflow**  

1. **Visual Encoding with CLIP**  
   - The image is processed using **CLIP's visual encoder**, which extracts semantic embeddings representing objects, relationships, and visual features.  
   - CLIP’s pretraining aligns these embeddings to natural language descriptions in its source languages (e.g., English).  

2. **Linguistic Inference with Language Models**  
   - Use a **pretrained language model** (e.g., GPT, mBART, or BLOOM) capable of multilingual generalization.  
   - Adapt the LM to the **target language** by providing:  
      - **Few-shot prompting**: Supply a few sample sentences in the target language.  
      - **Masked token prediction**: Infer linguistic structure for unseen words.  

3. **Caption Generation (Zero-Shot)**  
   - Integrate visual embeddings (from CLIP) with the target language text embeddings to form multimodal input.  
   - Generate captions using **language-conditioned decoding** in the LM.  
   - Adjust parameters such as beam search, top-k sampling, or temperature for fluency.  


---

## **Architecture Diagram**  

```
             ![image](https://github.com/user-attachments/assets/b0738812-4cc5-48a5-a014-98c628148f92)

---

## **Technologies and Tools**  
1. **CLIP**: For vision-language alignment.  
2. **Multilingual Language Models**:  
   - **gert** for text generation.  
3. **Transformers Library**: Hugging Face for implementation.    
5. **Python Libraries**:  
   - `torch`, `transformers`, `PIL`, `numpy`, and `sentencepiece`.  

---

## **Challenges and Solutions**  

1. **Zero-Shot Target Language Adaptation**  
   - Use **prompt tuning** and **masked token inference** to learn linguistic structures from minimal examples.  

2. **Visual-Linguistic Misalignment**  
   - Leverage **CLIP embeddings** for robust semantic grounding, ensuring captions reflect visual content accurately.  

3. **Ambiguity in Caption Generation**  
   - Use **beam search decoding** with a grammar-correction post-processor to ensure coherent output.  

4. **Scalability for New Languages**  
   - The system can generalize to unseen languages by adapting the prompts or dictionary alignment without retraining.  



 **Caption Generation**  
   - Use the pretrained LM with prompt templates:  
     ```  
     Example Template:  
     "A photo of {object}. In <target language>: ..."  
     ```  
   - Integrate the visual features with textual embeddings and generate outputs.  

---

**Run the Code:**
Open the provided Colab Notebook or execute the Python script locally.

🌐 Try It Out on Google Colab
Open the Colab File Here
https://colab.research.google.com/drive/1LoDSWYE4QiASh0xgFEV7Ag8LlGtXxes5?usp=sharing

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


---

## **Key Advantages**  
1. **Zero-Shot Adaptability**: No need for target-language training.  
2. **Scalable**: Easily extendable to other languages with minimal changes.  
3. **Efficient**: Combines CLIP's visual power with multilingual LMs for robust captions.  



