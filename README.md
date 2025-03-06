# An Optimization method for Balanced Multimodal Learning in Emotion Recognition. 
This project aims to solve the imbalanced problem of learning among modalities that improve efficiency in sentimental dataset. My solution is inspired by idea from paper: 
https://mn.cs.tsinghua.edu.cn/xinwang/PDF/papers/2023_Intra-%20and%20Inter-Modal%20Curriculum%20for%20Multimodal%20Learning.pdf

My thought is that to solve the imbalanced learning between different data input types(Unimodal) when combining together (Multimodal), we shall optimize both **Intra-**(within each modal) and **Inter-** steps(concatenating modalities) .

## Intra-: Implemented at Feed-forward stage and inside each single modality. 
* At feed-forward stage, we drop features of strong modalities probabilistically.
* Inside each modality, we update the weights in the way that "slow down" the gradients of strong modalities and vice versa.

## Inter-: Implemented at Fusion-Module of modalities.
We first estimate the similarity between unimodal gradient directions and that of multi- fusion. That way, we can update modalities weights at fusion in a way that prioritizes towards the gradient direction of weaker unimodals.

### My method is trained + tested on 2 dataset: CREMA_D and CMU_MOSI.
