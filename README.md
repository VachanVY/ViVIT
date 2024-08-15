# ViViT
![alt text](images/image.png)

## Embedding Video Clips
* ![alt text](images/image-1.png)
* ![alt text](images/image-2.png)

## Transformer model for Video
### Model 1: Spatio-temporal attention
* This model simply forwards all spatio-temporal tokens extracted from the video, $z_0$, through the transformer encoder

### Model 2: Factorised encoder
* ![alt text](images/image-3.png)
![alt text](images/image-4.png)

### Model 3: Factorized self-attention
* ![alt text](images/image-9.png)\
Factorised self-attention (Model 3). Within each transformer block, the multi-headed self-attention operation is factorised into two operations (indicated by striped boxes) that first only compute self-attention spatially, and then temporally\
* ![alt text](images/image-5.png)

### Model 4: Factorised dot-product attention
* ![alt text](images/image-6.png)

---
***Spatial Attention: Across H and W dimension\
Temporal Attention:   Across T dimension***

---

## Ablation
### Model Varients
* ![alt text](images/image-7.png)
* The unfactorised model (Model 1) performs the best on Kinetics 400. However, it can also overfit on smaller datasets such as Epic Kitchens, where we find our “Factorised Encoder” (Model 2) to perform the best
* 