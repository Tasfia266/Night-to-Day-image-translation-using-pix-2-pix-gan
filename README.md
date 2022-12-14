# Night-to-Day-image-translation-using-pix-2-pix-gan
Pix-2-pix is basically a conditional adversarial network which is an extended version of unconditional generative adversarial network (GAN). It is used for paired image to image translation in which an image is given as an input and the translated version of that image is generated as the output. It is also comprised of two networks 1. Discriminator and 2. Generator. The generator is nothing but the U-Net model architecture which works by downsampling an image to a bottleneck layer and upsampling it again with the help of skip connections.
![vanillau-net-architecture-768x429](https://user-images.githubusercontent.com/76652458/189713156-571fb06e-4cc4-4718-b655-36bebb1c364c.png)

For the discriminator, a PatchGAN model is used which is a deep convolutional neural network that gives prediction on the patches of an image as real or fake. The discriminator is run convolutionally across the image and then all the responses are averaged to a single score.
![Architecture-of-the-PatchGAN-Discriminator-network](https://user-images.githubusercontent.com/76652458/189714813-cfbf321d-dc4a-4ca8-8595-bc53038287bb.png)

In pix-2-pix gan, an adversarial loss which is binary-crossentropy and L1 loss (mean absolute loss between target image and generated image) are combined to form a composite loss for training the generator. 
![night_day](https://user-images.githubusercontent.com/76652458/189727486-884e7ef9-f36c-4d4a-9fe4-acebad7bc3b7.png)

The dataset that I used can be downloaded from here: http://efrosgans.eecs.berkeley.edu/pix2pix/datasets/
# References 
1. https://machinelearningmastery.com/a-gentle-introduction-to-pix2pix-generative-adversarial-network/#:~:text=The%20Pix2Pix%20GAN%20is%20a,on%20a%20given%20input%20image.

