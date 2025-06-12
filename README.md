What is ESRGAN?

ESRGAN (Enhanced Super-Resolution GAN) is a state-of-the-art deep learning model that restores photo-realistic details from low-res images. It's an enhanced version of SRGAN with powerful upgrades for better sharpness, texture realism, and perceptual quality.

💡 ESRGAN introduces:
❌ Removal of Batch Normalization (BN) — to eliminate artifacts.

🔁 Residual-in-Residual Dense Blocks (RRDB) — for better deep feature learning.

🧠 Relativistic Average GAN (RaGAN) — to generate more realistic details.

🎨 Perceptual Loss using pre-activation VGG features — for superior visual output.

ESRGAN is the enhanced version of the SRGAN. Authors of the ESRGAN tried to enhance the SRGAN by modifying the model architecture and loss functions.

Before diving into the ESRGAN first let’s get a high-level understanding of the GAN. GANs are capable of generating Fake data that looks realistic. Some of the GAN applications are to enhance the quality of the image. The high-level architecture of the GAN contains two main networks namely the generator network and the discriminator network. The generator network tries to generate the fake data and the discriminator network tries to distinguish between real and fake data, hence helping the generator to generate more realistic data.
