# Diffusion Model: What is it?

*

    <figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>
* The goal is that by training the model to denoise that model will be able to take in pure noise and from it synthesize a novel image
*

    <figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>
* We start with forward image diffusion process, we start with X0 the initial image to X1 with initial image with a bit of noise
* We can do this over and over again iteratively to add more and more noise to the image
* This distribution we call Q and it only depends on the previous step
* Once we do this for a high number of T, we reach pure noise
* In the initial research paper they had use T = 1000
* Now we want to go the reverse process, Xt noise image to Xt-1 less noisy image
* At each step we also learn reverse diffusion process
* We train a ML model that takes in noise image Xt and predicts the noise
*

    <figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>
* In training step, we take our initial image X and we sample at timestep t to create a noisy image X0
* We train a denoising model to predict the noise&#x20;
* This model is trained to minimize the difference between the predicted noise and actual noise added to the image
*

    <figure><img src="../../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>
* To generate an image, we can start with pure noise, and sent it through our denoising model, we can then take the predicted noise and subtract it from the initial noise, if we do this itteratively then we end up with generated image

