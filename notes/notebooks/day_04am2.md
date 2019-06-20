# Adversarial learning continued...

## Image to image translation. 
Automatic anime character creation using ML.
[Jin et al., Comiket 2017](https://arxiv.org/pdf/1708.05509.pdf)

## Text to image translation
[Zhang et al., ICC 2017](http://openaccess.thecvf.com/content_ICCV_2017/papers/Zhang_StackGAN_Text_to_ICCV_2017_paper.pdf)
[code](https://github.com/hanzhanggit/StackGAN)

## Basics and notation.
Denote the distribution of x as p(x) and x~p(x) as a sample x drawn from p(x).
Denote the expected value of x as Ep(x)[x] 
Denote the generator as x = f(epsilon, theta)
Denote the critic as D(x, ψ)
Theta and ψ are estimated via backpropogation of the objective function. 

## Learning adversarially revisited.
* Learn theta by minimizing the ability of the critic to identify fake samples.
* Learn psi by maximizing the critics ability to identify real samples. 

## Deep convolutional generative adversarial networks
Unsuprivised learning using generator-critic adversarial learning. 
[Rafford et al., ICLR 2016](https://arxiv.org/pdf/1511.06434.pdf)

## How to isolate style?
Adversarial disentanglement...
