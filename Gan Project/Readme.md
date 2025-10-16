# Galaxy Image Generation with GANs

This project uses a Generative Adversarial Network (GAN) to generate realistic 
galaxy images. The model is trained on real astronomical data and learns to 
reproduce structures such as spiral arms, elliptical shapes, and irregular galaxies.  

## Features  
- GAN implementation in PyTorch  
- Preprocessing pipeline for galaxy datasets  
- Tools to visualize generated samples during training  
- Sersic fitting analysis and radial color analysis to evaluate accuracy of GAN outputs

## Usage  
1. Prepare the dataset of galaxy images.  
2. Run the training script to train the GAN.  
3. View generated galaxy images in the output folder.  
4. Sort galaxies manually into categories (hoping to replace with a CNN soon)

## Future Improvements  
- Add conditional generation (cGAN) for specific galaxy types  
- Add a CNN for automated sorting into galaxy types  
- Improve evaluation with metrics like FID  
- Train on larger datasets for higher resolution results  

## Sources  
- Chat GPT was used in this process, but strictly for debugging and organization (of charts, graphs, etc.) purposes. The rest of the code was done by hand by me!  
- The GAN model was adapted from the starting point given in the PyTorch official GAN tutorial found here: https://docs.pytorch.org/tutorials/beginner/dcgan_faces_tutorial.html  
- Worked on with the help of Ayaan de Silva!
