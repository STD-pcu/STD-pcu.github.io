# Shape Tower Defense

## 목차
#### 1) [컨셉](#컨셉)
#### 2) [관련 자료](#관련-자료)
#### 3) [구성 요소](#구성-요소)
#### 4) [시스템 디자인](#시스템-디자인)
#### 5) [개발 요구사항](#개발-요구사항)
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
### 오브젝트
- 종류별 몬스터의 속도가 서로 다름
- 속성 저항력(화, 수, 명, 암)
- 종류별 몬스터마다 서로 다른 속성 저항력을 보유
- 속성 저항력% 만큼 해당 속성 데미지 감소
<br>
## 개발 요구사항

