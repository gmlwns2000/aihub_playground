# 이희준의 aihub 정복기

과제하고 할일이 없으니, ai 허브가 준 공짜 데이터로 스스로를 괴롭혀 봅시다!

After I finish my university assignment I don't have anything to do... so time to torturing myself!




# How This Repository Work?

루트에서 각 폴더의 main 폴더 안의 스크립트를 실행하면된다...!





# Finished

- [ ] Nothing yet!







# Work In Progress

## Project, 영상 프리뷰 만들어주는 웹사이트

`project_video_preview_web`

- [ ] 2021/11/7~

비디오 요약 영상을 만드는 백엔드 서버와, 유튜브 url을 받아서 처리하는 프론트 엔드!

## Task, [비디오 요약 영상, Video Summary, 중간](https://aihub.or.kr/aidata/27717)

`task_video_summary_highlight`

- [ ] 2021/11/7~

그저 할뿐

## Project, 보행자용 객체 인식 라이다 알람 시스탬

`project_blind_lidar`

- [ ] 2021/11/7~

### 요약

시각장애인들은 앞이 보이지 않는다. 따라서 앞에 무슨 물체가 얼마나 멀리 있는지 알려줄 필요가 있다.

이것을 현재는 막대기가 수행하고 있지만, 카메라 하나만 있다면 depth 추정과 object detection을 사용해서 어느 각도 방향에 얼마나 멀리 무슨 물체가 있는지 알 수 있을것이다.

이것을 햅틱 피드백으로 사용자의 몸에 전달할수있다면 정말 좋은 인공지능이 될것이다. 마치 앞의 물건의 "기"를 느끼게 하는것이다.

### 사용할 데이터셋

- [1인칭 시점 보행영상, Object Detection, 쉬움](https://aihub.or.kr/aidata/34125)

## Task, [1인칭 시점 보행영상, Object Detection, 쉬움](https://aihub.or.kr/aidata/34125)

`task_first_person_walk`

- [ ] 2021/11/7~

### 요약

Object detection 모델을 제작한다.









# Looks Good To Do!

난이도: 어려움, 중간, 쉬움

## [비디오 요약 영상, Video Summary, 중간](https://aihub.or.kr/aidata/27717)

- [ ] gogo

### 요약

유튜브 영상을 무작위로 다운로드하여 하이라이트 구간과 그 구간별 가장 중요한 프레임을 추론해야 한다.

유튜브 영상을 3초 단위로 잘라 구간별 압축하여 사용한다.

### 기존 방법론

3초단위로 잘린 프레임들을 ResNet으로 피처 추출하고, 
영상에서 추출된 피처백터 리스트에 대해서 매프레임별 벡터를 키로 어탠션을 수행하여 영상 백터를 리덕션하고, 
각 구간별로 FC로 중요도 구간인것을 0과 1 로 MSE로 학습한다.

### 제안

음성인식과 택스트인식 결과, 이미지와 음성 피처를 기준으로 추론하면 좋을것같다.

어텐션만 쓰는게 아니라 트렌스포머를 쓰면 좋을것같다

트렌스포머를 쓸거면 pretrain은 어떻게 할것인지 (Masking으로 feature vector interpolation?), 메모리때문에 전체 비디오를 넣지 못하는 문제는 어떻게 해결할지 챌린징하다 (Heirachy하게 하면 좋을것 같다)

## [1인칭 시점 보행영상, Object Detection, 쉬움](https://aihub.or.kr/aidata/34125)

- [ ] 대기중

### 요약

사람이 목에 카메라를 걸고 걸어다니면서 찍은 사진들이다! 물체들이 박스로 라벨링 되어있다!

정말 간단한 데이터셋이다... object detection task로 학습 시키는것도 좋지만, 그냥 다른 자율주행 알고리즘 테스트용으로 쓰는게 맞지 않을까?

### 기존 방법론

소개영상이 없다 ㅎ


### 제안

depth estimation을 사용해서 뎁스를 추론해서 얼마 앞에 무슨 물체가 있는지 알려주는 것을 만들어도 좋을것 같다

