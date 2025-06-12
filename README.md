What is ESRGAN?

ESRGAN (Enhanced Super-Resolution GAN) is a state-of-the-art deep learning model that restores photo-realistic details from low-res images. It's an enhanced version of SRGAN with powerful upgrades for better sharpness, texture realism, and perceptual quality.

💡 ESRGAN introduces:
 Removal of Batch Normalization (BN) — to eliminate artifacts.

 Residual-in-Residual Dense Blocks (RRDB) — for better deep feature learning.

 Relativistic Average GAN (RaGAN) — to generate more realistic details.

 Perceptual Loss using pre-activation VGG features — for superior visual output.

ESRGAN is the enhanced version of the SRGAN. Authors of the ESRGAN tried to enhance the SRGAN by modifying the model architecture and loss functions.

Before diving into the ESRGAN first let’s get a high-level understanding of the GAN. GANs are capable of generating Fake data that looks realistic. Some of the GAN applications are to enhance the quality of the image. The high-level architecture of the GAN contains two main networks namely the generator network and the discriminator network. The generator network tries to generate the fake data and the discriminator network tries to distinguish between real and fake data, hence helping the generator to generate more realistic data.

![Image Alt](https://github.com/Jyosnathallapakka/Super-Resolution-Image-Enhancement-using-ESRGAN/blob/4621b6ccdbed913e3661983b41060b698506ac29/gan1.webp)

ESRGAN
The main architecture of the ESRGAN is the same as the SRGAN with some modifications. ESRGAN has Residual in Residual Dense Block(RRDB) which combines multi-level residual network and dense connection without Batch Normalization.

Network architecture

![Image Alt](https://github.com/Jyosnathallapakka/Super-Resolution-Image-Enhancement-using-ESRGAN/blob/599e48ae7d3cc921d1432ef3f34c025e7b9ccba8/Esrgan1.webp)

Residual in Residual Dense Block(RRDB)

![Image Alt](https://github.com/Jyosnathallapakka/Super-Resolution-Image-Enhancement-using-ESRGAN/blob/599e48ae7d3cc921d1432ef3f34c025e7b9ccba8/esrgan2.webp)

                                                               🧱 Model Architecture

                                                                📥 Low-Resolution Input  
                                                                           ↓  
                                                        🔁 Residual-in-Residual Dense Blocks (RRDB)  
                                                                           ↓  
                                                                 📈 Upsampling Layers  
                                                                           ↓  
                                                                 🔍 Convolutional Layers  
                                                                           ↓  
                                                                 📤 Super-Resolved Output

🚀 Quick Start
🛠 Installation

<pre>git clone https://github.com/yourusername/ESRGAN
cd ESRGAN
pip install -r requirements.txt <pre>

If required, manually install:

<pre>pip install numpy opencv-python torch torchvision
</pre>

▶️ Run Inference
🗂️ Add your low-res images to ./LR/

⬇️ Download pretrained models and place them in ./models/

🧪 Run:
<pre>python test.py</pre>
📁 Results will be saved in the ./results/ folder.


📊 Performance Comparison

| Model         | **Set5 (PSNR/SSIM)** | Set14     | BSD100    | Urban100  | Manga109  |
| ------------- | -------------------- | --------- | --------- | --------- | --------- |
| **SRCNN**     | 30.48 / 0.8628       | 27.50     | 26.90     | 24.52     | 27.58     |
| **EDSR**      | 32.46 / 0.8968       | 28.80     | 27.71     | 26.64     | 31.02     |
| **RCAN**      | 32.63 / 0.9002       | 28.87     | 27.77     | 26.82     | 31.22     |
| **🔥 ESRGAN** | **32.73 / 0.9011**   | **28.99** | **27.85** | **27.03** | **31.66** |

🏆 Perceptual Super-Resolution Results

| Dataset  | ✅ ESRGAN | SRGAN | EnhanceNet |
| -------- | -------- | ----- | ---------- |
| Set5     | ✅        | ✅     | ✅          |
| Set14    | ✅        | ✅     | ✅          |
| BSD100   | ✅        | ✅     | ✅          |
| Urban100 | ✅        | ❌     | ✅          |
| PIRM-SR  | ✅        | ❌     | ✅          |
| OST300   | ✅        | ❌     | ✅          |
| DIV2K    | ✅        | ❌     | ✅          |

⚒️ Training Strategy
💥 Pro Tips for Best Results:

Use 0.1× MSRA weight initialization.

Apply residual scaling inside deep networks.

Train in two phases:

🎯 Stage 1: L1 loss-based PSNR optimization.

🔥 Stage 2: Fine-tune using adversarial + perceptual loss.

📌 Citation
If you use ESRGAN, please cite this paper:

<pre>
  @InProceedings{wang2018esrgan,
  author    = {Wang, Xintao and Yu, Ke and Wu, Shixiang and Gu, Jinjin and Liu, Yihao and Dong, Chao and Qiao, Yu and Loy, Chen Change},
  title     = {ESRGAN: Enhanced super-resolution generative adversarial networks},
  booktitle = {ECCV Workshops},
  year      = {2018}
}
</pre>
