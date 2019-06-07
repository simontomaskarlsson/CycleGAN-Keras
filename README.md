

## Keras implementation of CycleGAN
Implementation using a tensorflow backend. Testing and evaluation done on
street view images.

### Results - 256x256 pixel images

#### Day 2 night
<table>
  <tr>
    <th>Input</th>
    <th>Translation</th>
    <th>Input</th>
    <th>Translation</th>
  </tr>
  <tr>
    <td><img src="./ReadMe/images/day2night_r_1.png" alt="drawing" width="200px"/></td>
    <td><img src="./ReadMe/images/day2night_s_1.png" alt="drawing" width="200px"/></td>
    <td><img src="./ReadMe/images/day2night_r_2.png" alt="drawing" width="200px"/></td>
    <td><img src="./ReadMe/images/day2night_s_2.png" alt="drawing" width="200px"/></td>
  </tr>
  <tr>
    <td><img src="./ReadMe/images/day2night_r_3.png" alt="drawing" width="200px"/></td>
    <td><img src="./ReadMe/images/day2night_s_3.png" alt="drawing" width="200px"/></td>
    <td><img src="./ReadMe/images/day2night_r_4.png" alt="drawing" width="200px"/></td>
    <td><img src="./ReadMe/images/day2night_s_4.png" alt="drawing" width="200px"/></td>
  </tr>
</table>

#### Night 2 day
<table>
  <tr>
    <th>Input</th>
    <th>Translation</th>
    <th>Input</th>
    <th>Translation</th>
  </tr>
  <tr>
    <td><img src="./ReadMe/images/night2day_r_1.png" alt="drawing" width="200px"/></td>
    <td><img src="./ReadMe/images/night2day_s_1.png" alt="drawing" width="200px"/></td>
    <td><img src="./ReadMe/images/night2day_r_2.png" alt="drawing" width="200px"/></td>
    <td><img src="./ReadMe/images/night2day_s_2.png" alt="drawing" width="200px"/></td>
  </tr>
  <tr>
    <td><img src="./ReadMe/images/night2day_r_3.png" alt="drawing" width="200px"/></td>
    <td><img src="./ReadMe/images/night2day_s_3.png" alt="drawing" width="200px"/></td>
    <td><img src="./ReadMe/images/night2day_r_4.png" alt="drawing" width="200px"/></td>
    <td><img src="./ReadMe/images/night2day_s_4.png" alt="drawing" width="200px"/></td>
  </tr>
</table>

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

The following gif shows an example of the training
progression in a translation from day to night.

**Left:** Input image. **Middle:** Translated images. **Right:** Reconstructed images.
<img src="./ReadMe/gifs/CG_bl_streetview_progression.gif" alt="drawing" width="455px"/>


---

### More results

#### Day 2 night - gif
<img src="./ReadMe/gifs/city_day2night_2_short.gif" alt="drawing" width="400px"/>

#### Rainy 2 sunny - gif
<img src="./ReadMe/gifs/highway_rainy2sunny2.gif" alt="drawing" width="400px"/>

#### Sunny 2 rainy - gif
<img src="./ReadMe/gifs/highway_sunny2rainy_2.gif" alt="drawing" width="400px"/>
