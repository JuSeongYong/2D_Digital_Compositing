# 2D_Digital_Compositing
## Week 02 Assignment
### What is digital compositing?
+ 사전적 정의

    > Digital compositing is the process of digitally assembling multiple images to make a final image,
  typically for print, motion pictures or screen display. It is the digital analogue of optical film compositing. [Wikipedia](https://en.wikipedia.org/wiki/Digital_compositing)

    > 연속된 이미지나 합성 이미지를 만들기 위해 적어도 2개 이상의 소스 이미지들을 디지털로 합성하는 것. [Naver](https://terms.naver.com/entry.nhn?docId=1649302&cid=50372&categoryId=50372)

#### Digital Compositing
<pre>
<code>
- VFX Pipeline(post production)의 마무리 단계
- 여러가지 소스(영상, 이미지, 3D asset..)를 하나의 영상 또는 이미지로 통합하는 과정
</code>
</pre>

![alt](https://github.com/JuSeongYong/2D_Digital_Compositing/blob/master/Week03/the-vfx-pipeline.jpg)
+ Chroma Key
<pre>
<code>
- 두개의 영상을 합성하는 기술로 두개의 영상 중 상위 레이어의 특정한 색깔을 제거한다.
- 제거하고 싶은 색깔과 보여주고 싶은 오브젝트의 색깔이 겹치면 오류가 발생한다.
- 초록과 파랑이 자주 쓰인다.(=사람의 피부와 가장 구별되는 색깔)
Ex.) Green screen(most common), Blue screen, magic pink
</code>
</pre>

+ Rotoscoping
<pre>
<code>
- 상위레이어에 있는 개체 위로 마스크를 움직여 배경과 분리하는 과정
Ex.) Masking, Roto brush, Tracking, Planal tracking
</code>
</pre>

+ Matte painting
<pre>
<code>
- 디지털이나 아날로그 회화기법으로 새로운 이미지를 제작하는 기법
- 카메라로 촬영하기 힘든 장소를 재현하는데 주로 쓰임
- 디지털 기술 이후로 3D카메라로 2.5차원의 평면을 입체적으로 움직이며 복잡한 작업이 가능해짐
</code>
</pre>

+ Digital compositing을 위한 개인 역량과 지식
<pre>
<code>
- 색에 대한 이해도
- 카메라와 렌즈에 대한 지식
- 빛(조명)에 대한 지식
</code>
</pre>

+ Digital compositing tools
<pre>
<code>
- Paint Programs
- Color Correction utilities
- Warping/Morphing Tools
- Matte-Extraction software
- General-purpose compositing packages
Ex.) : NUKE, AE, Photoshop...
</code>
</pre>
[참조링크](http://mlab.taik.fi/touch/DCN/DGbackup.html)

---------------------
### What is Alpha and Color(Digital color)?

#### Alpha channel
<pre>
<code>
- RGBA(RGB채널에 투명도가 추가됨)에서 A=투명도를 나타냄
- straight alpha (unassociated alpha; Non-Premultiplied Alpha; unmatted RGB + alpha) : 
   알파값만이 투명도를 나타내고, RGB는 투명도와 관계없이 빨강, 초록, 파랑의 강도만 표현
- premultiplied alpha (associated alpha; matted RGB + alpha) : 
   RGB에 불투명도를 미리 곱해둔 값; 알파값 없이 RGB만으로도 투명도가 적용된 색상을 얻을 수 있음
</code>
</pre>

 - Non-Premultiplied Alpha
 
![Alt](https://github.com/JuSeongYong/2D_Digital_Compositing/blob/master/Week03/Non-Premultiplied%20alpha.png)

 - Premultiplied Alpha
 
![Alt](https://github.com/JuSeongYong/2D_Digital_Compositing/blob/master/Week03/Premultiplied%20alpha.png)

[참조링크](https://www.cgdirector.com/premultiplied-alpha-vs-straight-alpha/)

#### Color(Digital Color)
- 색의 3요소
<pre>
<code>
- Value(명도) : light to dark
- Saturation(채도) : how close to pure is it
- Hue(색상) : red, purple, green, yellow, orange, etc.
</code>
</pre>

 - Color Models
 <pre>
 <code>
 
 - CMYK : C(Cyan), M(Magenta), Y(Yellow), K(Black)의 4색을 조합하여 색을 나타낸다;
   감법 혼색<sup>(1)</sup>을 사용하며, CMYK 각각의 범위는 0~100
 
 - RGB : 빛의 3원색인 빨강, 초록, 파랑을 혼합하여 색을 나타낸다; 
   가법 혼색<sup>(2)</sup>을 사용하며, RGB의 각각의 채널값의 범위는 0~255 (R=0,G=0,B=0)의 좌표로 표시
   
 감법 혼색<sup>(1)</sup> : 색료의 혼합으로 새로운 색을 얻는 것; 혼색할수록 색이 어두워짐
 가법 혼색<sup>(2)</sup> : 색광(빛)을 혼합하여 새로운 색채를 만들어 내는 것; 색광을 동시에 혼색해서 생기는 색은 이전의 색보다 명도가 높아짐

 </code>
 </pre>
 [감법혼색과 가법혼색](https://blog.naver.com/01194508303/70072410087)
 ![Alt](https://github.com/JuSeongYong/2D_Digital_Compositing/blob/master/Week03/%EA%B0%90%EB%B2%95%ED%98%BC%EC%83%89%EA%B3%BC%20%EA%B0%80%EB%B2%95%ED%98%BC%EC%83%89.jpg)
 
 #### Why Photoshop shows transparency as gray and white checker?
 - 시각적인 목적; 아무것도 없는 텅빈 공간을 표현하기 위해 흰색과 회색의 체크를 사용했고, 사용자들한테 메타포로 심어졌다.

[참조링크-Doug Kerr](https://openphotographyforums.com/forums/threads/photoshop-the-light-gray-checkerboard.14116/)
