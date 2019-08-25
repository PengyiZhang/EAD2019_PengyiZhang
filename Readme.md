# Ensemble Mask-aided R-CNN

This is the test code of ensemble mask-aided r-cnn for EAD2019 challenge workshop

## Requirements

Pytorch==1.0.0
maskrcnn-benchmark==0.1

## pre-trained models


ID | Model | Backbone | Weights
- | :-: | :-: | -: 
0 | Faster R-CNN | Resnet50 | [model_final.pth](https://drive.google.com/open?id=1Q4zTLX5_m7SKStTALkK2OaJ3nhxdpamu)
1 | Mask-aided R-CNN | Resnet50 | [model_final.pth](https://drive.google.com/open?id=1XLRRFhrpSDZBRMJntbzoWocGL-hJbAqs) 
2 | Faster R-CNN | Resnet50+FPN | [model_final.pth](https://drive.google.com/open?id=1SO0iNVftgBYFX2kHFs-WCbjTvHcaneCJ)
3 | Mask-aided R-CNN | Resnet50+FPN | [model_final.pth](https://drive.google.com/open?id=1BVuIIn3Rxh39vfyYkj1AV77Bh8t3pBid) 
4 | Faster R-CNN | Resnet101+FPN | [model_final.pth](https://drive.google.com/open?id=1-foszOeQ7nYWzf-TEVR9q433Gia9MZeM)
5 | Mask-aided R-CNN | Resnet101+FPN | [model_final.pth](https://drive.google.com/open?id=1QdqRucutSdU6wUWpZzrSr6yurvXmLg-6)
6 | Faster R-CNN | ResneXt101+FPN | [model_final.pth](https://drive.google.com/open?id=1JCex2jgS60SdbH4dsTifVEUgXod9SDkE)
7 | Mask-aided R-CNN | ResneXt101+FPN | [model_final.pth](https://drive.google.com/open?id=1MpczZ-IUdDYm0KXMXMwdAK8yC5g5aHmB)


## test

    python3.6 tools/test_net.py --config-file "configs/e2e_mask_rcnn_R_50_C4_1x_ead_whole.yaml" MODEL.MASK_ON True MODEL.ROI_BOX_HEAD.NUM_CLASSES 6 TEST.IMS_PER_BATCH 1 OUTPUT_DIR "./Checkpoint/01_resnet50_mask_decay_1e_4"






