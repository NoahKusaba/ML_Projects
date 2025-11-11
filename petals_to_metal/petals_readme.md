final_submission: 
    - Actually submitted with 96.06 % accuracy
    - Combined train + validation dataset, as model accuracy plateaued with just train data and needed more data to become more accurate. 
    - Ensemble model combining several pretrained models including:
        model_0 = timm.create_model('convnext_base', pretrained=True, num_classes=output_shape)
        model_1 = timm.create_model("efficientnet_b0", pretrained=True, num_classes=output_shape)
        model_2 = timm.create_model("resnet18", pretrained=True, num_classes=output_shape)
    - Ensemble model weights found using grid-search. 

Pogressive_training:
    - Fun experiment notebook using pogressive training by using lower resolution images to begin with, and pogressively using higher resolution images across epochs, to optimize training time. Didn't end up using this technique in final_submission. 

