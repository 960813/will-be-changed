# will-be-changed

## 개요

### 제안 배경

2020년 초 발생한 코로나바이러스 감염증(COVID-19)은 시간이 흘러 범유행 선언이 되면서 전 세계적으로 공포심을 유발하고 있다.

전 세계 국가들은 질병의 전염을 예방하기 위한 손 씻기, 공공장소에서 마스크 착용하기, 사회적 거리 두기 또는 생활적 거리 두기를 국가 정책으로 추진하고 있다.

이 중 사회적 거리 두기는 개인 간의 밀접한 접촉을 최소화하여 질병의 확산을 늦출 수 있다. 학교, 회사, 경기장, 극장, 쇼핑몰 등 공공장소를 폐쇄하기도 하며, 또한 사람들은 집에 머물고 여행을 제한하고 붐비는 지역을 피하고 악수하지 않으며 신 체적으로 다른 사람과 거리를 두어 사회적 거리를 두는 방법을 적용할 수 있다.

그러나 식당과 마트와 같이 생활 속에서 어쩔 수 없이 방문해야 하는 공공장소가 존재한다. 이때 사람들은 비교적 사람이 적은 장소, 인구 밀도가 낮은 장소를 찾아가는 것을 선호하는 경향이 있다.

우리는 사람들이 공공장소 인구 밀도와 같은 정보를 효과적으로 얻을 수 있는 모델과 서비스를 개발하여 최종적으로는 다중이 이용하는 시설의 분산 이용을 유도하여 코로나 19 전파의 주요 특징인 산발적인 연쇄감염을 감소시키고자 한다.

### 세부 내용

* 인구 밀도 탐색
  * RPI 8MP CAMERA BOARD 이용, 3280x2464 Photo, 1080p30, 720p60 Video Capture
  * 캡처된 영상(동영상, 정지영상)을 전처리하고 Object Detection(이때, 상황에 따라 칼만 필터나 RNN 기반 tracking 알고리즘 구상 가능성 있음)
  * Detection된 정보를 Remote Server Database에 저장
    with Device UUID, IP Address, Detection Object Information
* 인구 밀도 데이터 시각화
  * 수집된 인구 밀도 데이터를 Map PAI와 GeoIP를 활용해 시각화
  * 식당, 카페, 마트 등 위치 정보를 얻기 위한 소상공인 공공데이터 활용

### 기대효과

* 다중 이용 시설, 그중에서도 밀집되고 밀접한 접촉이 이루어지는 시설의 분산 이용 유도를 통한 코로나19 전파의 주요 특징인 산발적인 연쇄감염 감소
* 인구 밀도 통계를 바탕으로 밀도가 높은 시설의 위치, 업종을 분석하여 특화된 방역 수칙 제정 가능
* Web 기반 콘텐츠 제공으로 새로운 기능 개발이 수월하여 경쟁력 보유

### 발전 방향

* 통합 CMS 형태로 발전 시켜 방역 정보, 매장 이벤트 정보 등 다양한 정보를 디스플레이에 표시하여 새로운 수요 기대 가능
* 카메라와 디스플레이를 포함한 디바이스 전체를 새롭게 설치하는 것이 아닌 기존 CCTV 녹화기 등에 설치하는 형태로 발전 시켜 비용 절감 효과 기대 가능
* 방범용 카메라 등에 확대 설치하여 주요 지역 인구 밀도 통계 측정, 시각화 가능

### 팀 구성: 총괄 1명, 개발자 3명, 디자이너 1명

* 총괄: 하드웨어 회로 설계 및 개발, 모니터링 웹페이지 개발, AWS 서버 관리
* 개발자1: 하드웨어 코딩(Web API 연동 및 테스트)
* 개발자2: 웹페이지 코딩(인구 밀도 시각화 페이지 코딩)
* 개발자3: 웹페이지 코딩(인구 밀도 시각화 페이지 코딩)
* 디자이너: 하드웨어 외형 디자인 및 조립, 웹페이지 UI/UX 개발

## 설계/구조

1. 라즈베리 파이
   * 이미지 캡처
   * yolov3-tiny with OpenCV 연산
   * 

## ?