# Shape Tower Defense

## 목차
### 1) [컨셉](#컨셉)
### 2) [관련 자료](#관련-자료)
### 3) [구성 요소](#구성-요소)
### 4) [시스템 디자인](#시스템-디자인)
### 5) [개발 요구사항](#개발-요구사항)
<br>

## 컨셉
### 메인 컨셉
- 디펜스 (타워 디펜스)
### 서브 컨셉 : 도형
- 각이 점점 늘어날수록 강해지는 타워들 / 적 컨셉(미정)

<br>

## 관련 자료
- 랜덤 다이스 상점
<br>
<img src="./img/store1.jpeg"> 
<img src="./img/store2.png">
<br>

- 랜덤 다이스 플레이 화면
<br>
<img src="./img/battle_scene1.png">
<br>

## 구성 요소
### 매커니즘
- 정해진 타일에 타워를 설치해 적들을 없애며 최대한 오래 라운드를 버텨 클리어 하는것이 목표
- 적이 정해진 루트를 정해진 횟수만큼 돌면 라이프 차감
- 정해진 라이프가 전부 소진 될 경우 게임 오버
<br>

### 재미 요소
- 한정된 타일 갯수와 종류별 타워로 전략적 재미를 느낄 수 있음
- 라운드마다 바뀌는 새로운 루트
<br>


## 시스템 디자인
### 파라미터
- UI

속성 | 명칭 | 설명
---- | ---- | ----
체력 | HP | 현재 체력 / 최대 체력 <img src="./img/HP.PNG">
보스 카운트 | BOSS | 현재 라운드 / 목표 라운드 <img src="./img/보스 카운트.PNG">
몬스터 수 | count | 남은 몬스터 / 현재 라운드 전체 몬스터 <img src="./img/남은 몬스터 수.PNG">
재화 | gold | 현재 보유중인 재화 <img src="./img/재화.PNG">


- 타워 공통

속성 | 명칭 | 설명
---- | ---- | ----
레벨 | level | 타워의 업그레이드 단계
사거리 | range | 공격 범위 및 효과가 미치는 범위
구매 가격 | price | 타워 구매시 필요한 재화량
판매 가격 | sell | 타워 판매시 얻는 재화량
업그레이드 비용 | upgrade | 타워 업그레이드시 필요한 재화량

- 공격 타워

속성 | 명칭 | 설명
---- | ---- | ----
데미지 | damage | 타워가 공격시 입히는 발당/초당 데미지

- 기타 타워

속성 | 명칭 | 설명
---- | ---- | ----
버프 | buff | 버프타워의 버프량. 해당 %만큼 사거리 내의 타워들의 데미지 상승
슬로우 | slow | 슬로우타워의 감속량. 해당 %만큼 사거리 내의 적들의 이동 속도 감소


## 게임에서 사용될 공식

### 데미지 공식
- 속성 저항력과 데미지, 속도 등의 공식
### UI
- 라운드, 재화, 체력, 타일
### 씬 관리 및 옵션
- 사운드, 클릭, 종료 등

## 개발 요구사항
- 메인 메뉴의 시작/상점/옵션/종료 버튼 및 씬 이동
- 시작버튼 누를시 라운드 선택
- 아직 깨지 못한 라운드 잠금
- 상점의 뽑기 시스템, 보유중인 타워, 게임에 가져갈 타워 슬롯
- 옵션의 볼륨 조절,음소거 및 씬별 연동
- 적이 이동하는 경로
- 타워가 적을 인식하는 범위 및 계산식
- 타워가 적을 인식시 각 타워별 공격 발사(클론 생성)
- 타워의 공격 적과 충돌시 소멸 및 이펙트 발생
- 적이 정해진 루트를 모두 이동했을 경우 피격 이펙트가 발생하며 체력 감소
- 타워를 설치 할 수 있는 타일
- UI 및 시작버튼, 인벤토리
- 재화 및 설치 갯수 제한에 걸린 타워 설치시 설치 불가 경고문 출력
- 인벤토리의 타워 클릭 시 클론 생성 후 타일 클릭시 조건 만족 후 설치
- 타워 판매 및 업그레이드 구현
- 체력 소진시 게임 오버창 오버로딩
- 게임 오버씬 생성
- 게임 오버씬에서 라운드 선택 및 메인 메뉴 이동 선택 버튼
