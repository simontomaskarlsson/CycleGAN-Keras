

## Keras implementation of CycleGAN
Implementation using a tensorflow backend. Testing and evaluation done on
street view images. The following gif shows an example of the training
progression in a translation from day to night.

**Left:** Input image. **Middle:** Translated images. **Right:** Reconstructed images.
![](./ReadMe/gifs/CG_bl_streetview_progression.gif?)

### Model additions as training options
* Identity learning (on different modulus of training iterations)
* PatchGAN in discriminators
* Multi-scale discriminators
* Resize convolution in generators
* Supervised learning with training weight
* Data generator (if using a large dataset)
* Weight on discriminator training labels on real images

---

### Code usage  
1. Prepare your dataset under the directory 'data' and set dataset name to
parameter 'image_folder' in CycleGAN init function.
  * Directory structure on new dataset needed for training and testing:
    * data/Dataset-name/trainA
    * data/Dataset-name/trainB
    * data/Dataset-name/testA
    * data/Dataset-name/testB  

2. Set wanted training options, also found in the init function.

3. Train a model by:
```
python CycleGAN.py
```

4. Generate synthetic images by following specifications under:
  * generate_images/ReadMe.rtf

---

### Results - 256x256 pixel images  
**Left:** Input image. **Right:** Translated image

#### Day 2 night
![](./ReadMe/images/day2night_r_1.png?) ![](./ReadMe/images/day2night_s_1.png?)
![](./ReadMe/images/day2night_r_2.png?) ![](./ReadMe/images/day2night_s_2.png?)
![](./ReadMe/images/day2night_r_3.png?) ![](./ReadMe/images/day2night_s_3.png?)
![](./ReadMe/images/day2night_r_4.png?) ![](./ReadMe/images/day2night_s_4.png?)
![](./ReadMe/images/day2night_r_5.png?) ![](./ReadMe/images/day2night_s_5.png?)

#### Night 2 day
![](./ReadMe/images/night2day_r_1.png?) ![](./ReadMe/images/night2day_s_1.png?)
![](./ReadMe/images/night2day_r_2.png?) ![](./ReadMe/images/night2day_s_2.png?)
![](./ReadMe/images/night2day_r_3.png?) ![](./ReadMe/images/night2day_s_3.png?)

#### Day 2 night - gif
![](./ReadMe/gifs/city_day2night_2_short.gif?)

#### Rainy 2 sunny - gif
![](./ReadMe/gifs/highway_rainy2sunny2.gif?)

#### Sunny 2 rainy - gif
![](./ReadMe/gifs/highway_sunny2rainy_2.gif?)
---
