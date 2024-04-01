# Multiclass Semantic Segmentation on Aerial Imagery Using U-Net and UNETR (Vision Transformers U-Net)

⚡ In this project, I built a couple of UNet-based models for the task of Multiclass Semantic Segmentation of satellite images of Dubai to compare their performance.

I built 5 models including the classic UNet and Vision-Transformer-based UNet (UNETR).
The other 3 models are variations of it (VGG10-UNet, Densenet-121-Unet, Attention-UNet)

⚡ In conclusion, using 2088 images to train models, Densenet-121-Unet achieved the best performance with an accuracy of 89% compared to others. 

The UNETR architecture utilizes a Transformer as the encoder to learn sequence representations of input images and effectively capture the global multi-scale information, following this, there is a CNN-based decoder to upsample the global representations and generate the final segmentation mask.

[UNETR: Transformers for 3D Medical Image Segmentation],
Ali Hatamizadeh, Dong Yang, Holger Roth, Daguang Xu. 2021. (https://arxiv.org/abs/2103.10504?context=cs.CV)

<img width="741" alt="19c387ec-df70-4d60-847f-331910aa384f" src="https://github.com/NiloofarAZAD/ViT-and-CNN-Based-UNet-Models-Semantic-Segmentation-Aerial-Imagery/assets/128168974/ea6af991-460c-4c84-a2f6-e0c15f99c99c">


⚡ Dataset: https://www.kaggle.com/datasets/humansintheloop/semantic-segmentation-of-aerial-imagery

The dataset consists of aerial imagery of Dubai obtained by MBRSC satellites and annotated with pixel-wise semantic segmentation in 6 classes. The total volume of the dataset is 72 images grouped into 6 larger tiles => cut up images into 256x256 pieces to create a larger training set. 
