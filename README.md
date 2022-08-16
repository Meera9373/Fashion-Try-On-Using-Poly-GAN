# Fashion-Try-On-Using-Poly-GAN

Virtual clothing try-on is in major demand in recent years, with the objective of transferring an input garment image onto a reference person. 

The goal of the typical try-on assignment is to match the target clothing item with the provided individual’s physique and therefore present the person’s try-on look. 

On the basis of different generative adversarial networks, a proposal is made for posture-guided virtual try-on method to attain this objective. 

Experiments would be conducted on the VITON dataset and a few of our own images. It features pairs of images; each pair comprises of a women’s front-view and an image of top piece of clothes image.

The Structural Similarity Index Measure (SSIM) will be used to assess the accuracy of the model. New outfits are generated onto existing human model images while retaining the body shape and pose of the wearer.

## Methodology

![image](https://user-images.githubusercontent.com/60151306/184825856-5697600e-952e-4bd5-a037-8552c686ebd1.png)

## Detailed Design

![image](https://user-images.githubusercontent.com/60151306/184826171-1fecb0ed-a9b4-44e1-9888-0b59e9435db1.png)

## Results

![image](https://user-images.githubusercontent.com/60151306/184826309-d6f6a75e-c5d9-4895-91c6-2b84fd449324.png)

## Conclusion

The Poly-GAN is trained with inputs being model images wearing clothing piece and another input garment (top clothing only). 

In the following stage, to infer the appearance flows between person representation (RGB model (Parsed)) and the garment image, conjugating a mask containing the lower body clothes region (garment mask), hair and face, and the individual’s body segmentation outcome, and the human posture assessment outcome as the individual representation. 

Then, at that point, the skeleton is utilized to generate the shape of the wrapping garments. 

Trained a generative module with these wrapped garments, the conserved areas on the model picture, and human posture estimates along channels as inputs to get the person image with the new outfit as our result.

The accuracy using the Structural Similarity Index Measure (SSIM) of the model was found to be between 75% to 90% which indicates the model can effectively work as a virtual try-on.
