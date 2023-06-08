# Lecture 18

## Types of neural networks
- computer vision (image analysis) CNN
- sequence-to-sequence translation (speech, text) RNN
- persective on model-based vs model-free approaches to AI

## Convolutional Neural Networks
- local detection of features/patterns
- aggregation/abstraction

## Convolution
- use a filter on image
- multiply each corresponding number, and add all together
- 6x6 apply 3x3 filter to get 4x4
  - technically can also be represented by 36 nodes to 16 nodes, each of 16 nodes connects to 9 previous nodes
- size of filter is a hyperparameter
- add padding to still get details at edges
  - depending on size of filter and image, can add padding to get same size
  - same convolution
- padding p, filter f, stride s
- greater size of stride, smaller result

## Colors
- H x W x C
- height by width by channels
- filter also has 3 channels

## Multiple Filters
- end with H x W x C, C is number of filters

## Max Pooling
- 2x2 max pooling, every 4 turns into 1, just take max

## CNN Architecture (example)
- input, then convolve on 8 filters
- max pooling, still have 8 channels
- 16 filters afterwards
- pooling, still 16
- fully connected
  - uses the most weights
  - common for number of filters to increase
