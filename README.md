Zhang et al. (2018) demonstrated that a Convolutional Neural Network (CNN) could predict human eye movements by extracting features from target and search images. A previous project using the same top-down modulation methodology added color to the target image and investigated whether this color could attract attention when presented in the search image. Although searching for the target was irrelevant to the target image's color, the CNN model showed enhanced attention to stimuli with the same color. These results resembled the memory-driven attentional capture observed in human behavioral studies, where pre-cue color influences visual attention.

However, the CNN model and search approach differed from human attention mechanisms. In human visual search tasks, when a color singleton is presented as a distractor while searching for a specific target, a stimulus-driven attentional capture occurs. When applying this to the previous project, the top-down modulation actually suppressed the salient stimulus. While the model effectively implemented the top-down search process for identifying targets, it failed to adopt the bottom-up processing of salient stimuli.

According to Treisman and Gelade's feature integration theory, when viewing an image, various feature maps (color, orientation, motion, contrast) are processed through different pathways and then integrated into a master map for attention allocation. This theory is functionally implemented in CNN models. The weights of trainable filters capture various feature information during object classification training. Lower layers process local and detailed features, while higher layers address more global and abstract characteristics.

I sought to overcome the previous project's limitation of missing bottom-up information by leveraging the structural characteristics of CNN models and feature integration theory. Pre-trained CNN filters from ImageNet can effectively detect various image stimulus features. I hypothesized that the model's output would well represent bottom-up information about stimuli. Similar to the previous project, top-down information was obtained through pixel-wise multiplication of target image features and search image bottom-up information. These two attention map informations were combined to predict eye movements using CNN.

The project used 2,880 TL task images, with conditions including target-nontarget similarity (Low vs High) and color singleton distractor (Absent vs Present).


Example of images. Target image; Search image; BU atteniton map; TD attention map
<img width="700" alt="image" src="https://github.com/user-attachments/assets/c65a2927-643e-4976-9ca9-58ce736b944b" />

Example of search processing.
<img width="515" alt="image" src="https://github.com/user-attachments/assets/46f35543-20c7-4ff2-8524-a3adb57e6c39" />


