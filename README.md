#  YRCars  

Machine Learning system that identifies car model from a photograph.

Upload an image of a car and receive ranked predictions with confidence scores.  
Powered by three EfficientNetB3 deep learning models trained on different datasets.

---

##  Live

https://ml-cars-iota.vercel.app/

---

##  Tech Stack

###  Machine Learning
- PyTorch  
- EfficientNetB3 (Transfer Learning)  
- Multi-model ensemble approach  

###  Backend
- FastAPI  
- Python 3.10  

###  Frontend
- React
- Vite  
- Framer Motion  

###  Deployment
- Railway (Backend)  
- Vercel (Frontend)  

---

##  How It Works

When a user uploads a car image:

1. The image is preprocessed and resized.
2. It is passed through three independently trained classifiers:
   - **Stanford Cars Model**  
     - 196 classes  
     - Predicts: make + model + body type + year  
   - **Custom Dataset Model**  
     - 48 classes  
   - **Dataset Brand Classifier**  
     - 33 car brands  
3. Predictions are combined.
4. Results are ranked by confidence.
5. The Top 5 predictions are returned.

This ensemble-style architecture improves robustness and prediction reliability.

---

All models are based on EfficientNetB3 using transfer learning and fine-tuning.

---


## 🛡️ License

MIT License  

---

## 👨‍💻 Author

@yessetkrodriguez
