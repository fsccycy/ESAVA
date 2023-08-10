# ESAVA
Embryo Segmentation and Viability Assessment

## ABSTRACT
The selection of embryos is a key for the success of in vitro fertilization (IVF). Automatic quality assessment on human IVF embryos with optical microscope images is still challenging. In this study, we developed a clinical consensus-compliant deep learning approach called **Esava (Embryo Segmentation and Viability Assessment)** to quantitatively evaluate the development of IVF embryos of day-2 and day-3 with optical microscope images. By refining the baseline Faster R-CNN model, our Esava model was constructed, refined, trained, validated, and optimized for precise and robust embryonic cells detection. A novel algorithm **Crowd-NMS** was proposed and employed in Esava to enhance the object detection and to precisely quantify the embryonic cells and their sizes. The difference proportion of blastomere diameters were computed to evaluate their size uniformity. Another novel **GrabCut-based** unsupervised module was further applied in Esava to perform the segmentation of blastomeres and embryos.

## WORKFLOW
* The overall workflow of ESAVA is:
<p float="left">
  <img src="ESAVA_workflow.jpg?raw=true"/>
</p>

* The segmentation workflow is:
<p float="left">
  <img src="segmentation_workflow.jpg?raw=true"/>
</p>

## Model Checkpoint
- `Weights`: [resnet50_new_model_40000_ht_2.hdf5](http://www.liwzlab.cn/cy_data/qz/resnet50_new_model_40000_ht_2.hdf5)

## USAGE
* Install python3.6.
* Run the script **pip install -r requirements.txt**.
* Download the model weights "resnet50_new_model_40000_ht_2.hdf5" from [model checkpoint](#model-checkpoint), and put it in the same directory as [blastomere_detection_segmentation.py](#blastomere-detection-segmentation).
* Create the folder **images** with blastomere images in the same directory as the python files and run the script **python blastomere_detection_segmentation.py**.

## DEMO
<p float="left">
  <img src="detection_demo.png?raw=true" width="49.5%" />
  <img src="segmentation_demo.png?raw=true" width="47.9%" />
</p>
