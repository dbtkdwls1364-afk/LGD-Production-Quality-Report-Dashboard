# LGD-Production-Quality-Report-Dashboard

# LG Display 생산·품질 보고서 웹 서비스

## 날짜

2026년 09월 14일

## 사용 라이브러리

* **Python**
* **Flask** : 웹 서버 및 REST API 구현
* **Werkzeug** : Flask 웹 서버 실행
* **Three.js** : 패널 검사·이송 설비 3D 시각화
* **OrbitControls.js** : 3D 설비 화면의 회전 및 확대·축소 기능
* **HTML / CSS / JavaScript** : 웹 UI 및 사용자 인터랙션 구현
* **JSON** : 생산·품질 데이터 및 보고서 데이터 저장
* **Cloudflared** : Google Colab에서 실행한 웹 서버의 외부 접속 주소 생성
* **Asyncio / Threading** : 서버 실행 및 파일 다운로드 등의 비동기 처리

## 설명

LG Display 생산 현장을 가정하여 제작한 **생산·품질 데이터 조회 및 보고서 작성 웹 서비스**입니다.

생산라인과 조회 기간을 선택하면 LOT별 생산량, 목표 생산량, 검사 수량 및 불량 데이터를 조회할 수 있으며, 이를 기반으로 **생산 달성률과 불량률을 자동 계산**합니다.

또한 Three.js를 활용하여 패널 검사·이송 설비를 3D 형태로 구현하고, 생산라인의 현재 모의 상태와 설비 사건 이력을 함께 확인할 수 있도록 구성하였습니다.

주요 기능은 다음과 같습니다.

* 날짜 및 생산라인별 생산·품질 데이터 조회
* LOT별 목표 생산량, 실제 생산량, 검사 수량 및 불량 수량 확인
* 생산 달성률 자동 계산
* 검사 수량 대비 불량률 자동 계산
* 일자별 불량률 시각화
* 설비 사건 및 조치 기록 조회
* Three.js 기반 패널 검사·이송 설비 3D 시각화
* 조회 데이터를 기반으로 생산·품질 보고서 초안 자동 생성
* 보고서 수정 및 검토 상태 저장
* 보고서 TXT 파일 다운로드
* 보고서 근거 데이터 JSON 파일 다운로드
* Cloudflared를 이용한 외부 웹 접속

본 프로젝트의 데이터는 실제 LG Display 생산 데이터가 아닌 **교육 목적으로 구성한 가상 데이터**이며, 보고서 초안 생성 과정에서도 별도의 LLM API를 사용하지 않고 정해진 규칙을 기반으로 문장을 생성하도록 구현하였습니다.

## 참고 문헌들

* Flask Documentation
  https://flask.palletsprojects.com/

* Three.js Documentation
  https://threejs.org/docs/

* Three.js OrbitControls Documentation
  https://threejs.org/docs/#examples/en/controls/OrbitControls

* Cloudflare Tunnel Documentation
  https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/

* Python Documentation
  https://docs.python.org/3/

* MDN Web Docs - HTML / CSS / JavaScript
  https://developer.mozilla.org/
