Very Deep Convolutional Networks For Large-Scale Image Recognition
============================================================================
논문 링크 : <https://arxiv.org/pdf/1409.1556.pdf>   
   
   
   
논문요약
--------
>1. ILSVRC 2014 대회에서 2등을 차지한, Karen Simonyan과 Andrew Zisserman이 만든 CNN 모델
>2. VGGnet, GoogleNet 이전의 depth는 8layers 수준에서 머물렀다면 GoogleNet, VGGnet 이후 크게 깊어졌다.
>3. 
>4. 최근에는 이미지 특징(feature)을 추출하는 데 이용되는 등 기본 네트워크 모델로 활용되고 있음.
>5. 매우 많은 파라미터를 이용하여 연산한다는 단점이 있음.

receptive field
---------------
VGGNet 이전에 Convolutional Network를 활용하여 이미지 분류에서 좋은 성과를 보였던 Model들은 비교적 큰 Receptive Field를 갖는 11x11 Convolution Filter나 7x7 Convolution Filter를 포함한다. 하지만 VGG 모델에서는 3x3 Convolution Filter만으로 이미지 분류 정확도를 개선시켰다.   

#### 더 깊은 모델을 만들 수 있다.
---
7x7 Convolution Filter를 1stack을 3x3 Convolution Filter를 3 stack으로 구현 할 수 있어 조금 더 깊이 있는 레이어를 가진  모델을 만들 수 있다. Convolution layer의 ReLU 함수의 중복으로 비선형성이 증가하게 되어 모델의 특징의 식별성 증가한다. 
<br>   
#### 학습 파라미터 수의 감소   
---
VGGNet의 특징은 작은 Convolution Filter(3x3, 1 strides)로 깊은 레이어(16-19 weight layers)를 만들어 좋은 성능을 낸다. Convolutional Network 구조를 학습할 때 1개의 Convolution Filter의 파라미터 수는 필터 크기에 해당한다. 따라서 7x7의 학습 파라미터 수는 49개 이고 3x3 Convolution Filter 3 stack 구조는 3 * 3 * 3 = 27 개이다. 이와같이 작은 크기의 Convolution Filter를 사용하여 학습 파라미터 수를 감소 시켜 학습 속도를 높힐 수 있다.



실험 내용
---------
><모델간 layer 및 파라미터 비교> 
<img src="/image/1.JPG" width="80%" height="80%" title="img1" alt="img1"></img>   
><모델의 성능>   
<img src="/image/2.JPG" width="80%" height="80%" title="img1" alt="img1"></img>   
VGGNet은 224x224 크기의 color image를 input으로 하여 1개 이상의 convolutional layer 뒤에 max-pooling layer 가 오는 단순 구조로 되어 있으며 기존 CNN 구조와 마찬가지로 Fully-connected layer가 온다. A 모델과  A-LRN 모델 사이의 LRN layer의 유무에 따른 모델 성능을 비교한 결과 top-1 val.error와 top-5 val.error의 성능 향상이 없다고 판단하여  B 모델 ~ E 모델은 layer 깊이에 따른 모델 성능의 변화를 비교 하였다. 


