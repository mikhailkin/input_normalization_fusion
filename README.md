# input_normalization_fusion
Input Normalization with the first layer fusion

## About 

In this repository a simplistic implementation of input fusion with the first layer is presented. 
This repository might be used to speed up preprocessing step.

## How it works

We know that both input normalization and the first layer most often are linear operations. Input normalization can be noted as xn = 𝓦n ○ x + bn. Where 𝓦n is a multiplicative part and bn is a bias or an additive part.
Let 𝓛(𝓦, b, x) be the first layer of our neural network. What we intend to do is to substitute 𝓛(𝓦, b, 𝓦n ○ x + bn) for 𝓛(𝓦’, b’, x), or in other words to make fusion.

## TODO

- [ ] Tensorflow.
- [ ] Performance benchmarks.

## Acknowledgements

Thanks to [@lext](https://github.com/lext) for the [Batch Norm Fusion for Pytorch](https://github.com/MIPT-Oulu/pytorch_bn_fusion) and author of the [blog](https://tehnokv.com/posts/fusing-batchnorm-and-conv/)
Funny pictures might be found [here](https://medium.com/@mikhailkin/accelerating-nns-for-free-getting-rid-of-ridiculous-input-normalization-before-feeding-your-nns-ced759c1ec58)
