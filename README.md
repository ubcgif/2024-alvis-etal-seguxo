# Using convolutional neural networks to classify UXO with multicomponent electromagnetic induction data

_Jorge Lopez-Alvis, Lindsey J. Heagy, Douglas W. Oldenburg, Stephen Billings and Lin-Ping Song_

![thumbnail](./abstract/thumbnail.png)

## Summary 

 Electromagnetic induction (EMI) methods are commonly used to classify unexploded ordnance (UXO) in both terrestrial and marine settings. Modern time-domain systems used for classification are multicomponent which means they acquire many transmitter-receiver pairs at multiple time-channels. Traditionally, classification is done using a physics-based inversion approach where polarizability curves are estimated from the EMI data. These curves are then compared with those in a library to look for a match based on some misfit. 

 In this work, we developed a convolutional neural network (CNN) that classifies UXO directly from EMI data. In the architecture of the CNN, the input was defined as a two-dimensional data map considering a fixed number of transmitter cycles in the along-track direction and the spatial extent of the receivers in the cross-track direction. Analogous to an image segmentation problem, our CNN outputs a classification map that preserves the spatial dimensions of the input. In this way, our CNN produces high-resolution results and can handle the multiple transmitter-receiver pairs and the per-line acquisition of multicomponent systems. We train the CNN using synthetic data generated with a dipole forward model considering all possible UXO and clutter objects. A careful design of the clutter classes is needed to maximize clutter discrimination. A physics-based parameterization of the clutter classes is used to maximize clutter discrimination. 

 We tested our approach using field data acquired with the UltraTEMA-4 system in the Sequim Bay marine test site. We found that the CNN results can be affected by spatially and temporally correlated noise remaining in the preprocessed data. Including this systematic noise in our training dataset was crucial to improve our classification results for field data. To tackle this issue, we add a first step in our workflow that uses a CNN to get field data patches without metallic objects and then randomly add those patches containing only “background signal” to our synthetic data. Using this workflow, classification results for the field data show that our approach detects all UXOs and classifies more than 90% as the correct type while also discriminating ~70% of the clutter. A key advantage of our CNN is that, once trained, it may be used to provide real-time classification results on the field.

## Citation 


