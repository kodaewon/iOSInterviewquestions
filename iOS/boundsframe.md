## Bounds 와 Frame 의 차이점을 설명하시오



### Bounds

[Apple Developer Documentation] 

The bounds rectangle, which describes the view’s location and size in its own coordinate system. (구글 번역 - 경계 좌표 : 자체 좌표계에서 뷰의 위치와 크기를 설명합니다.)

간단하게 자기 좌표에서 위치와 크기를 나타낸다고 한다.

결국은 x, y는 0,0 으로 나올것이고 width, height는 자기 자신의 넓이, 높이 값을 나타낼 것 이다.



### Frame

[Apple Developer Documentation] 

The frame rectangle, which describes the view’s location and size in its superview’s coordinate system. (구글 번역 - 수퍼 뷰의 좌표계에서보기의 위치와 크기를 설명하는 프레임 사각형입니다.)

자기 좌표를 내가 속해있는 상위(부모) 뷰에 의해서 위치와 크기를 나타낸다고 합니다.

x,y는 왼쪽 위에 점 기준으로 점에 위치에 값을 나타내고 width, height는 자기 자신의 넓이, 높이 값을 나타낼 것 이다.





