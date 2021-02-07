# Vanilla-GAN
A simple PyTorch implementation of Ian Goodfellow's original Generative Adversarial Network on the MNIST dataset.

# Description
Basic code implementation of Goodfellow's original, basic GAN architecture along with the minimax optimization objectives outlined in his [2014 paper introducing GANs](https://arxiv.org/pdf/1406.2661.pdf).

### Minimax Loss Function (modelled on the Binary Cross-entropy Loss)
![image](https://user-images.githubusercontent.com/20011207/107147790-e8a2b700-6975-11eb-8c77-d693f51ce45a.png)
The primary intuition here is that the discriminator is trying maximize its probability of correctly classifying a real image as real and fake as fake, while the generator is trying to minimze the probability of the discriminator getting it right (i.e. fooling it).

# Results
## After 5 epochs
Initial noise sampled from a standard normal distribution
![Screen Shot 2021-02-07 at 18 45 19](https://user-images.githubusercontent.com/20011207/107147539-a2992380-6974-11eb-80d2-0593edd8364a.png)

## Halfway through training
Around this point, I was a bit concerned that it may be delving into a mode collapse failure, generating almost all digits which resembled '1'.
![Screen Shot 2021-02-07 at 18 46 43](https://user-images.githubusercontent.com/20011207/107147581-d4aa8580-6974-11eb-8d73-9c54780af2d3.png)

## After about 50 epochs
I had put the number of epochs at 100 but it was taking way too long after a point, I did not notice any major improvement so I decided to stop training. I'm not sure if it converged; I'll try plotting some learning curves to see how the error changes over epochs to get a better idea.
![Screen Shot 2021-02-07 at 18 42 34](https://user-images.githubusercontent.com/20011207/107147495-74b3df00-6974-11eb-9119-bfbabfde3726.png)
