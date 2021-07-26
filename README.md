# Targeted-Backdoor-Attacks-on-Deep-Learning-Systems-Using-Data-Poisoning-

This is an implementation of the paper [*Targeted Backdoor Attacks on Deep Learning Systems Using Data Poisoning*](https://arxiv.org/abs/1712.05526) by *Chen et al*. <br>
The attention was on the **backdoor poisoning attacks** (attack is made by adding a few poisoning samples into the training dataset). <br>

## Dataset
The dataset used is [*YouTube Aligned Face*](https://www.cs.tau.ac.il/~wolf/ytfaces/).  <br>
The original dataset contained 1595 labels. We filtered the dataset by removing labels with less than 100 instances obtaining around 600.000 images and 1283 labels. The dataset was splitted in:
- **Training Set** contains 90 images for every label.
- **Test Set** contains 10 images for every label.
- **Validaton Set** contains 10 images for every label.
- **Poison Set** contains the remaining images.

## Models
The models implemented were [*DeepID*](https://openaccess.thecvf.com/content_cvpr_2015/html/Ouyang_DeepID-Net_Deformable_Deep_2015_CVPR_paper.html) and [*VGG-Face*](http://www.bmva.org/bmvc/2015/papers/paper041/index.html). <br>
We started from the TF 1.0 [implementation](https://github.com/jinze1994/DeepID1) of DeepID and we implemented a Keras version of the VGG-Face model.

## Attacks
- **Input-instance attack**: attacker chooses one of his face photos as the key *k* and selects the target label.
- **Blended-injection attack**: attacker chooses a *blend-ratio* between 0 and 1 (different for poison and backdoor instances).
- **Accessory-injection attack**: attacker chooses a key pattern like a pair of glasses.
- **Blended-accessory injection attack**: attacker chooses a blend-ratio between 0 and 1 (different for poison and backdoor instances) and a key pattern.




