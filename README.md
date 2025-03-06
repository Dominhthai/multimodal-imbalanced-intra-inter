# A method for Balanced Multimodal Learning 
This project solves the imbalanced problem of learning among modalities in 2 steps: Intra- and Inter- Learning.

## Intra-: Implemented at Feed-forward stage and inside each single modality. 
* At feed-forward stage, we drop features of strong modalities probabilistically.
* Inside each modality, we update the weights in the way that "slow down" the gradients of strong modalities and vice versa.

## Inter-: Implemented at Fusion-Module of modalities.
We first estimate the similarity between unimodal gradient directions and that of multi- fusion. That way, we can update modalities weights at fusion in a way that
