# MQImagePicker
简单的自定义相机 支持正反镜头
在 初始化预览层的地方  有这个代码：
    self.previewLayer = [AVCaptureVideoPreviewLayer layerWithSession:self.session];
    
    [self.previewLayer setVideoGravity:AVLayerVideoGravityResize];
    self.previewLayer.frame = self.bounds;
    [self.layer addSublayer:self.previewLayer];
    
    // 为了使剪裁的效果没有偏差  这里应该选这个AVLayerVideoGravityResize类型。 demo里面选的是别的类型， 记得修改哦
