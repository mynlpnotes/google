# Image Generation Model Families

* Variational Autoencoders (VAE):
  * Encode image to a compressed size, then decode them back to the original size while learning the distribution of the data
* Generative adversarial models (GAN):
  * Pit two NN against each other
  * Generates creates images
  * Discriminator predicts if its real or fake
  * Over time discriminator gets better at distinguishing between real and fake
  * And generator becomes better at creating real looking fakes
* Autoregressive models:
  * Generate images by treating an image as a sequence of pixels
  * Draws inspiration from how LLMs handle text
* Diffusion Models
