# 🧠 Secured Text-Based CAPTCHA using Style Transfer Approach

## 📘 Project Overview

This project proposes a **Style Transfer-based approach** to generate **secure, text-based CAPTCHAs** that are resistant to deep learning and OCR attacks while maintaining readability for human users.  
Traditional CAPTCHAs often fail due to advanced AI solvers like CNNs and GAN-based models that can easily decode distorted text. Our solution applies **Neural Style Transfer (NST)** techniques to introduce complex yet human-recognizable patterns into CAPTCHA text.

---

## 🎯 Problem Statement

- Traditional text-based CAPTCHAs are **vulnerable** to deep learning and OCR-based attacks.  
- Adding excessive distortion decreases **human usability**.  
- Static CAPTCHAs fail to **adapt to evolving AI-based solvers**.  

---

## 💡 Proposed Solution

We integrate **Neural Style Transfer (NST)** using **Convolutional Neural Networks (CNNs)** to generate dynamically stylized CAPTCHAs with:
- Complex textures inspired by artistic styles (e.g., Van Gogh, Cubism, Abstract).  
- Enhanced resistance against machine-based solvers.  
- Maintained readability for human users.  

Additionally, we explore **GAN-based enhancements** to dynamically generate evolving CAPTCHA backgrounds and distortions.

---

## 🧩 Methodology

### 1. **Dataset**
- Source: [CAPTCHA Dataset by Wilhelmy & Rosas (2013)](https://www.researchgate.net/publication/248380891_captcha_dataset)  
- Contains 200x50 PNG images of 5-character alphanumeric words with noise (blur and lines).

### 2. **Model Components**
- **Neural Style Transfer (NST):** Extracts content and style features from images using CNN layers.  
- **Style Loss & Content Loss Optimization:** Maintains legibility while embedding diverse artistic patterns.  
- **GAN Integration:** Generates dynamic backgrounds and noise textures to prevent pattern learning.  

### 3. **Workflow**
1. Input CAPTCHA →  
2. Apply Style Transfer (using pre-trained CNNs) →  
3. Optimize for readability and complexity →  
4. Generate CAPTCHA image output →  
5. Evaluate against CNN/OCR/GAN attacks.  

---

## 🧠 Literature Survey Highlights

| Paper | Key Contribution | Outcome |
|-------|------------------|----------|
| *Image-based CAPTCHAs via NST (IET, 2019)* | Introduced style transfer to CAPTCHAs | 75–84% human success, low attack success |
| *Neural Algorithm of Artistic Style (Gatys et al.)* | Separated content & style using CNNs | Enabled high-quality artistic transformations |
| *Secured Text-Based CAPTCHA (IEEE ICT, 2024)* | Used GANs + NST for background generation | 2.1% machine recognition rate |
| *Cycle-GAN CAPTCHA Attack (2020)* | Efficient CAPTCHA cracking | Highlighted need for adaptive defenses |
| *Adversarial CAPTCHAs (IEEE TCyb, 2022)* | Frequency-domain perturbations | Near-zero attack success rate |

---

## 🔬 Results

- **Without Style Transfer:** 98.68% recognition rate (easily cracked)  
- **With Proposed Model:** 2.1% recognition rate  
- **Human Success Rate:** ~80–85%  
- **Usability:** Improved over traditional CAPTCHAs due to balanced style-content tradeoff  

---

## 🧱 Architecture

```
+----------------------+
|   CAPTCHA Dataset    |
+----------+-----------+
           |
           v
+----------------------+
|  Neural Style Transfer|
|  (Content + Style)   |
+----------+-----------+
           |
           v
+----------------------+
|  GAN-based Enhancer  |
|  (Dynamic Noise)     |
+----------+-----------+
           |
           v
+----------------------+
|  CAPTCHA Generator   |
| (Stylized Output)    |
+----------------------+
```

---

## ⚙️ Technologies Used

- **Python**
- **TensorFlow / PyTorch**
- **OpenCV**
- **Matplotlib**
- **NumPy**
- **Pillow**
- **Neural Style Transfer (VGG-19 based)**
- **GAN Models (for background synthesis)**

---

## 🚀 Future Work

- Implement **adaptive CAPTCHAs** that evolve based on attack patterns.  
- Integrate **adversarial training** for improved robustness.  
- Reduce **computational cost** of GAN + NST processing.  
- Extend to **audio or multimodal CAPTCHA systems**.  

---

## 📚 References

1. Wilhelmy, R., & Rosas, H. (2013). *CAPTCHA Dataset*.  
2. Gatys et al., *A Neural Algorithm of Artistic Style*.  
3. IEEE ICT 2024 – *Secured Text-Based CAPTCHA using Customized CNN with Style Transfer and GAN-based Approach*.  
4. IEEE Transactions on Cybernetics, 2022 – *Adversarial CAPTCHAs*.  
5. Preprint, 2020 – *End-to-End Attack on Text-Based CAPTCHAs using Cycle-GAN*.  

---

## 🏁 Conclusion

This project demonstrates that **Neural Style Transfer and GANs** can be effectively combined to create **secure, dynamic, and human-readable CAPTCHAs**.  
Our approach significantly reduces machine recognition rates while maintaining human usability, paving the way for next-generation CAPTCHA systems.
