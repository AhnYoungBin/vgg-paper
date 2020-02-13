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
VGG 모델 이전에 Convolutional Network를 활용하여 이미지 분류에서 좋은 성과를 보였던 모델들은 비교적 큰 Receptive Field를 갖는 11x11 Convolution Filter나 7x7 Convolution Filter를 포함한다. 하지만 VGG 모델에서는 3x3 Convolution Filter만으로 이미지 분류 정확도를 개선시켰다.   
#### 1. 더 깊은 모델을 만들 수 있다.   

5x5 Convolution Filter를 1stack을 3x3 Convolution Filter를 2stack으로 구현 할 수있음으로 인하여 조금 더 깊이 있는 레이어를 가진  모델을 만들 수 있다. 
#### 2. 학습 파라미터 수의 감소   
VGGNet의 특징은 작은 컨볼루션 필터(3x3, 1 strides)로 깊은 레이어(16-19 weight layers)를 만들어 좋은 성능을 낸다.

모델 구조
--------
