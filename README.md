# YRCars  

Machine Learning system that identifies car model from a photograph.

Upload an image of a car and receive ranked predictions with confidence scores.  
Powered by three EfficientNetB3 deep learning models trained on different datasets.

---

<table>
  <tr>
    <td align="left" width="50%">
      <img
        src="https://github.com/user-attachments/assets/f289904f-0248-44fc-97a5-4ed98a1ef637"
        alt="System interface preview"
        width="90%"
      />
    </td>
    <td align="right" width="50%">
      <img
        src="https://github.com/user-attachments/assets/22d6d0b8-0900-431e-b99b-6f7cf74ca565"
        alt="Application dashboard view"
        width="90%"
      />
    </td>
  </tr>
</table>

---

## Live Application

**Try the application here:**  
https://ml-cars-iota.vercel.app/

---

## How It Works

When a user uploads a car image:

1. The image is preprocessed and resized.
2. It is passed through three independently trained classifiers:
   - **Stanford Cars Model**  
     - 196 classes  
     - Predicts: make + model + body type + year  
     - Includes vehicles manufactured between **1991 and 2012**
   - **Custom Dataset Model**  
     - 48 classes  
   - **Dataset Brand Classifier**  
     - 33 car brands  
     - Includes some more recent models (limited samples) such as Toyota, Ferrari, and other modern brands
3. Predictions are combined.
4. Results are ranked by confidence.
5. The Top 5 predictions are returned.

The Stanford Cars dataset mainly contains vehicles from **1991–2012**, while the brand classifier helps detect more updated vehicles, although in smaller quantities per brand.

This ensemble-style architecture improves robustness and prediction reliability.

---

## Infrastructure Constraints

Due to using the **Render Free Plan**, deployment resources are limited (RAM and disk size).  

Because of this:

- Some datasets had to be compressed.
- Model sizes were optimized.
- Larger architectures were avoided.
- Batch sizes were adjusted during inference.

These optimizations ensure the system runs reliably within free-tier constraints while maintaining strong prediction performance.

---

## Tech Stack

### Machine Learning
- PyTorch  
- EfficientNetB3 (Transfer Learning & Fine-Tuning)  
- Multi-model ensemble approach  

### Backend
- FastAPI  
- Python 3.10  

### Frontend
- React  
- Vite  
- Framer Motion  

### Deployment
- Render (Backend - Free Plan)  
- Vercel (Frontend)  

---

All models are based on EfficientNetB3 using transfer learning and fine-tuning.
