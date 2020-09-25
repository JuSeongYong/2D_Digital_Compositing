# 2D_Digital_Compositing
## Week 03 Assignment
### What is colorspace?
- Colorspace
<pre>
<code>
- 색 표시계(color system)를 3차원으로 표현한 공간 개념이다. 
- 색 표시계의 모든 색들은 이 색 공간에서 3차원 좌표로 나타낸다.
- 색상(hue), 명도(lightness), 채도(chroma)를 3차원 공간의 각각의 기본 축으로 하는 공간
</code>
</pre>

- 색공간의 이해
<pre>
<code>
- 색의 3속성 색상, 명도, 채도를 3차원 공간의 각각의 축으로 형성
- 자주 쓰이는 색 공간 : RGB색공간, CMYK색공간, HSV색공간, CIE색공간
</code>
</pre>

- RGB색공간

![Alt](https://github.com/JuSeongYong/2D_Digital_Compositing/blob/master/Week04/images/200px-RGBCube_b.svg.png)


- CMYK색공간

![Alt](https://github.com/JuSeongYong/2D_Digital_Compositing/blob/master/Week04/images/%EB%8B%A4%EC%9A%B4%EB%A1%9C%EB%93%9C.jpg)


- HSV색공간

![Alt](https://github.com/JuSeongYong/2D_Digital_Compositing/blob/master/Week04/images/200px-HSV_cone.jpg)

#### CIE 색공간
CIE는 국제 조명 위원회(프랑스어: Commission internationale de l'éclairage)를 프랑스어식으로 표기한 준말이며, CIE 색 공간이란 컬러 매칭 실험을 통하여 생성된 R, G, B 데이터를 바탕으로 만들어진 CIEXYZ 색 공간과 CIELAB 색 공간, 그리고 CIELUV 색 공간이 대표적인 색 공간이다.

여기서 CIEXYZ 색 공간은 '균등 색 공간<sup>(1)</sup>'이 아니어서, 이를 수식적으로 변환하여 만들어진 것이 CIELAB 색 공간과 CIELUV 색 공간이며, 이 두 색 공간은 색차를 계산할 때 비교적 정확한 계산이 이루어진다.

여기서 '균등 색 공간'이란 '불균등 색 공간'의 대립 개념이며, 불균등 공간에서는 색상들을 나타내는 선, 채도들을 나타내는 선들이 일정하지 않고 불규칙하게 배열되기 때문에 색 공간에서 두 점의 거리 즉, 색의 차이를 계산하면 정확하지 않다.

- CIE xyz 색공간 : XYZ 색 공간은 RGB 색 공간으로부터 선형변환<sup>(2)</sup>을 통해 얻을 수 있으며, 모든 값이 양수를 갖는다.

![Alt](https://github.com/JuSeongYong/2D_Digital_Compositing/blob/master/Week04/images/CIE-1931-color-space.jpg)


- CIE lab 색공간 : Lab 색 공간은 인간 시각의 길항 이론에 의거하여, CIE XYZ 색 공간을 비선형 변환하여 만들어진 색 공간

![Alt](https://github.com/JuSeongYong/2D_Digital_Compositing/blob/master/Week04/images/CIE-LAB-1976-color-space.png)


- CIE luv 색공간 : CIE가 1976년에 정한 균등 색공간의 하나로서 다음의 3차원 직교 좌표를 이용하는 색공간

![Alt](https://github.com/JuSeongYong/2D_Digital_Compositing/blob/master/Week04/images/CIELUV.png)

균등 색공간<sup>(1)</sup> : 동일한 크기로 지각되는 색차가 공간 내의 동일한 거리와 대응하도록 의도한 색공간

선형 변환<sup>(2)</sup> : 자료의 분포 모양을 그대로 유지하면서 점수 혹은 측정치를 일정 규칙에 따라 다른 점수 혹은 척도로 바꾸는 것

#### YUV
YUV(YIQ/YCbCr/YPbPr)는 색을 구성하는 방법 중 하나로 밝기(=휘도)(Y)와 청색 색차(U), 적색 색차(V) 정보로 색을 구성

Lab과 마찬가지로 인간이 색을 인식하는 방식으로 구성

영상 장치가 영상을 만들 때, 빛을 인식하여 RGB를 YUV로 바꿔 주게 되며, YUV의 데이터 양을 줄이고 효율을 유지하기 위해 서브 샘플링을 하여 저장장치에 저장하게 된다.

※ RGB는 원색신호에 대한 정보, YUV는 색차신호에 대한 정보를 포함하고 있음.

YUV를 전송방식에 따라 YPbPr과 YCbCr로 나눈다.

- YPbPr : Analog color signal(아날로그 시스템을 위해 디자인된 것)
- YCbCr : Digital color codes(디지털 비디오에 사용되도록 디자인된 것)
<pre>
<code>
- Y(Luma) : 밝기 / Cb(Chroma blue) : 청색-밝기 / Cr(Chroma red) : 적색-밝기
- Color정보를 디지털화 시킨 값
</code>
</pre>

#### ACES(Academy Color Encoding System) Colorspace

- ACES는 모든 인풋 소스(영화, CG 등)으로부터 색상을 표준화하고, 모든 프로덕션 파이프라인의 단계에서 아티스트들이 일할 수 있도록 하는 미래가 보장되는 작업 환경을 제공하는 색상 시스템을 의미

- CG아티스트에게 있어서, ACEScg의 큰 장점은 색상 전체 영역(colour gamut)

[출처](https://blog.naver.com/jygoldturtel/221827788379)

![Alt](https://github.com/JuSeongYong/2D_Digital_Compositing/blob/master/Week04/images/%EB%8B%A4%EC%9A%B4%EB%A1%9C%EB%93%9C%20(1).jpg)

-------------
### Gamma / Linear workflow

#### What is Gamma?

- Gamma

<pre>
<code>
- 감광 재료의 콘트라스트 상태를 나타내는 척도로 농도 변화 및 노광량의 변화를 수치로 나타낸 것
- 감마는 디스플레이에 입력되는 신호의 밝기(Gray Level)와 화면상에 나타나는 영상의 휘도 간 상관 관계를 결정하는 수치
- 감마값에 따라 같은 화면이라도 표현되는 밝기 톤의 차이가 나타남
- 감마값이 1인 경우는 입력과 출력의 밝기가 같지만, 1보다 크면 중·저계조 영역에서 화면이 좀 더 어둡게 표현이 되고, 
  반대로 1보다 작으면 밝게 표현
</code>
</pre>

0 Gray부터 255 Gray까지 단계별로 한 칸씩 각각의 밝기를 지정하고, Gray가 올라갈수록 해당되는 Gray의 휘도가 점점 높아지게 설정을 합니다. 만약, 감마값이 1이라면 Gray Level에 따른 휘도 값이 정비례하게 나타나게 되겠지요. 하지만, 인간의 눈은 어두운 곳의 차이는 잘 구분하지만 밝은 곳의 차이는 잘 구분하지 못하기 때문에 감마값을 1로 정비례하게 설정을 해 놓는다면 높은 Gray로 갈수록 밝은 색을 잘 구분하지 못하게 됩니다.

이를 보완하기 위해 인간의 눈에 최적화시킨 감마값을 맞추는 것이 중요한데요. 그 값이 NTSC(National Television System Committee) 표준 감마값인 2.2입니다.

![Alt](https://github.com/JuSeongYong/2D_Digital_Compositing/blob/master/Week04/images/gammacurve.jpg)

그래프에서 보시다시피, 감마값 2.2는 1보다 낮게 깔려 있는데요. 이는 중·저계조 영역에서 출력되는 휘도의 변화가 크지 않지만 고계조로 갈수록 Gray Level에 따른 휘도의 변화가 큼을 의미합니다. 즉, 고계조 영역에서 밝기의 구분이 수월해진다는 것이지요. 만약 감마값이 2.2보다 큰 2.8의 경우, 저계조 영역에서 Gray Level에 따른 휘도의 변화가 거의 나지 않게 되어 이미지가 매우 어둡게 뭉쳐져서 보이게 되겠지요.

[gamma출처](https://news.samsungdisplay.com/1869)

#### Linear Workflow

<pre>
<code>
- 실제 세상의 빛은 linear로 작용, 우리가 보는 빛의 양은 광원들의 빛의 양을 합친 값이다. 즉, 실제 세상에서는 input이 output과 일정, 동등하다. 이를 linear라고 한다.
- 하지만 모니터에서는 이와 다르게 아래 그래프처럼 표시한다.
모니터가 이미지를 표현하기 위해서는 전압이 공급(input)되고, 모니터는 이를 빛의 정도로 환산해서 이미지(output)로 표현한다.
하지만 컴퓨터 모니터는 우리의 눈이 받아들일 수 있는 빛의 양을 표현할 방법이 없기 때문에 컴퓨터는 눈에 보이는 것과 유사하게 표시한다. 이를 color space라고 부른다.
- 모니터들이 가장 많이 사용하는 color space는 sRGB(non-linear, 8bit, gamma 2.2) 안에서 이뤄진다.
sRGB안에서는 gamma correction이라는 것이 작용하는데, 이는 우리가 본 luminance값을 비디오나 사진에서 암호화, 해독하던 방식을 말한다.
그래서 이를 다시 linear로 바로잡기 위해 의도적으로 수치값을 대입한다. 이 수치를 gamma라고 한다.
</code>
</pre>

![Alt](https://github.com/JuSeongYong/2D_Digital_Compositing/blob/master/Week04/images/%EB%A6%AC%EB%8B%88%EC%96%B4%EC%9B%8C%ED%81%AC%ED%94%8C%EB%A1%9C%EC%9A%B0.png)

![Alt](https://github.com/JuSeongYong/2D_Digital_Compositing/blob/master/Week04/images/asdf.png)

------------
### What is LUT? Color LookUpTable?

---------------
### What is Logspace and what is main difference wiht sRGB, why and when we use?
