# Ensemble Mask-aided R-CNN

This is the test code for ensemble mask-aided r-cnn in EAD2019 challenge workshop

## Requirements

Pytorch==1.0.0
maskrcnn-benchmark==0.1

## pre-trained models

ID | Model | Backbone | Weights
- | :-: | :-: | -: 
0 | Faster R-CNN | Resnet50 | [model_final.pth](00_resnet50_faster_decay_1e_4/model_final.pth)
1 | Mask-aided R-CNN | Resnet50 | [model_final.pth](01_resnet50_mask_decay_1e_4/model_final.pth) 
2 | Faster R-CNN | Resnet50+FPN | [model_final.pth](02_resnet50-fpn_faster_decay_1e_4/model_final.pth)
3 | Mask-aided R-CNN | Resnet50+FPN | [model_final.pth](03_resnet50-fpn_mask_decay_1e_4/model_final.pth) 
4 | Faster R-CNN | Resnet101+FPN | [model_final.pth](04_resnet101_faster_decay_2e_4/model_final.pth)
5 | Mask-aided R-CNN | Resnet101+FPN | [model_final.pth](05_resnet101-fpn_faster_decay_2e_4/model_final.pth)
6 | Faster R-CNN | ResneXt101+FPN | [model_final.pth](06_resnext101_faster_decay_2e_4/model_final.pth)
7 | Mask-aided R-CNN | ResneXt101+FPN | [model_final.pth](07_resnext101-fpn_faster_decay_2e_4/model_final.pth)


## test

    python3.6 tools/test_net.py --config-file "configs/e2e_mask_rcnn_R_50_C4_1x_ead_whole.yaml" MODEL.MASK_ON True MODEL.ROI_BOX_HEAD.NUM_CLASSES 6 TEST.IMS_PER_BATCH 1 OUTPUT_DIR "./Checkpoint/01_resnet50_mask_decay_1e_4"






