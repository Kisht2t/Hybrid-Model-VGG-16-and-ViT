# Hybrid-Model-VGG-16-and-ViT

IDE: This code uses the google collab, Google Collab is Preferred for T4 GPU.

How to use Google Collab and save dataset in google drive?

# Refer the link:
https://www.youtube.com/watch?v=Gvwuyx_F-28

A hybrid model using pretrained VGG16 layers to extract low-level features before passing them through ViT blocks.

A model Performace review is given at the end of this code comparing to the performance of 2 models on the same dataset. 

# Model 1: Vision Transformer (https://github.com/Kisht2t/Vision-Transformer)

# Model 2: Hybrid VGG 16 + ViT Model (Same Code)

Flow Work:

# Hybrid VGG16 +ViT Model

1. Pretrained VGG16 for Feature Extraction:

• Use pretrained VGG16 layers up to block3_conv3 or up to block5_conv3 ot extract initial
image features. The advantage of blocks_conv3 si that it produces a smaller output
(14x14x512) for ViT.

• Freeze these VGG16 layers to use them as a fixed feature extractor.

2. Implement the Hybrid Model:

• After extracting features with VGG16, feed the output into the VTi blocks.

• Ensure the output of VGG16 layers matches the VTi input shape requirements. 

• Add a classification head after the ViT blocks to produce predictions.

3. Training and Evaluation:

• Train the hybrid model on the CIFAR-10 or Cats and Dogs training set.

• Evaluate the hybrid model on the test set, tracking the same metrics as in Task. 

• Save checkpoints and visualize some predictions on test images.
