
# 프로필  
## 이런 개발자입니다
- <b>게임 개발 과정에서 협업이 중요하다는 것을 알고, 동료 직원들과의 협업을 위한 고민을 많이 합니다.</b>  
- <b>개인 업무에 그치지 않고 동료의 업무를 도우며 팀에 일이 주어지면 먼저 나서서 일을 받아 수행합니다.</b>
- <b>새로운 기술에 대한 학습과 도전을 멈추지 않습니다. </b>

### Contact
- Email.  kyaya12345@gmail.com

### Channel
- Blog.  https://chocobubble.github.io/
- GitHub.  https://github.com/chocobubble/

<br>

## ️ 기술 스택

### 개발 언어

`C#` `C++` `Python`  

### 게임 엔진

`DirectX` `Unity` `Unreal Engine`



<br><br>

# 사이드 프로젝트

<br>

## 1. DirectX12 3D 렌더링 엔진

### 프로젝트 소개

DirectX 12를 기반으로 구축한 3D 렌더링 엔진입니다. 현대적인 그래픽스 기법들을 단계적으로 구현하며, 각 기능의 개발 과정과 문제 해결 과정을 문서화했습니다.

> GitHub : [DirectX12 Graphics Engine](https://github.com/chocobubble/DirectX12-Graphics)  
> Wiki : [DirectX12 Graphics Wiki](https://github.com/chocobubble/DirectX12-Graphics/wiki)

- 프로젝트 유형 : 3D 렌더링 엔진
- 제작 기간 : 2025. 6. ~ 현재
- 제작 인원 : 1인 (개인 프로젝트)
- 사용 기술 : DirectX 12, C++, HLSL
- 언어 : C++

![lunar](./Images/lunar.png)




### 주요 구현 기능

- **PBR (Physically Based Rendering)** - Cook-Torrance BRDF 모델
- **IBL (Image Based Lighting)** - HDR 환경 맵 기반 조명
- **테셀레이션** - Hull/Domain Shader를 활용한 적응적 지오메트리 세분화
- **그림자 매핑** - 깊이 버퍼 기반 실시간 그림자
- **노말 매핑** - TBN 공간 변환을 통한 디테일 향상
- **GPU 기반 파티클 시스템** - Compute Shader 활용
- **거울 반사** - Stencil Buffer를 활용한 평면 반사
- **빌보드 렌더링** - Geometry Shader 기반
- **포스트 프로세싱** - Compute Shader 활용한 가우시안 블러

### 상세 문서

#### **[프로젝트 위키 바로가기](../../wiki)**

### 주요 결과물

| 기능 | 구현 내용 | 개발일지 |
|------|-----------|----------|
| PBR 렌더링 | Cook-Torrance 모델, Metallic-Roughness  | [상세보기](../../wiki/2025-07-06-PBR) |
| IBL 시스템 | Irradiance Map, Prefiltered Environment Map | [상세보기](../../wiki/2025-07-12-Ibl) |
| 테셀레이션 | 거리 기반 적응적 지오메트리 세분화, 와이어프레임 시각화 | [상세보기](../../wiki/2025-07-09-Tessellation) |
| 파티클 시스템 | GPU 기반 물리 시뮬레이션 | [상세보기](../../wiki/2025-07-05-Particle) |

### 학습 자료

이 프로젝트는 다음 자료들을 참고하여 개발되었습니다:

- [홍정모 연구소 컴퓨터 그래픽스 새싹코스](https://www.honglab.ai/courses/graphicspt1)
- DirectX 12를 이용한 3D 게임 프로그래밍 입문 (Frank Luna)


<br><br>

## 2. LooterShooter

> 자세한 프로젝트 관련 내용은 [하단](#ls) 혹은 [Github Wiki](https://github.com/chocobubble/LooterShooter/wiki)에서 확인 가능합니다.
### 개요
- 게임 장르 : looter shooter(TPS + RPG)  
- 제작 기간 : 2023. 6. ~ 10.
- 제작 인원 : 1인 (개인 프로젝트)
- 사용 엔진 : Unreal Engine v5.2 
- 언어 : C++
- 플레이 영상 : 
  - 이미지 클릭 시 유튜브에서 영상이 실행됩니다.  
    [![play](https://img.youtube.com/vi/FKlwz-1G0EQ/0.jpg)](https://youtu.be/FKlwz-1G0EQ)

### 프로젝트를 진행하면서 얻은 점
#### 1. GitHub의 Project, Issue, Wiki를 이용하여 프로젝트 관리를 했습니다.
  - 문제점
    -  프로젝트를 구체적 기획없이 개발을 시작하려고 하니 개발 우선순위 및 순서 결정 등의 어려운 부분이 있었습니다.
  - 해결 방안
    -  구현하려는 기능, 프로젝트의 전체적인 구조 등을 Github Projects를 이용해 시각적으로 계획하고 진행해나가니 이전 프로젝트 보다 더 효율적인 개발이 가능했습니다.
  - [GitHub Projects 링크](https://github.com/users/chocobubble/projects/2)
#### 2. 데이터 시스템을 구축하여 데이터를 코드와 분리하고, 비프로그래머도 수정이 가능하도록 했습니다.
  - 문제점
    -  처음에는 코드에 스탯 등 관련 데이터들을 넣어 하드코딩했습니다. 그러다 보니 프로젝트를 진행하며 각종 수치들을 변경할 때마다 매번 코드를 수정하고 다시 컴파일을 하느라 시간이 많이 소모되었습니다.
  - 해결 방안
    -  csv를 이용한 데이터 시스템과 블루프린트를 이용해 데이터를 코드와 분리하여 수치를 변경할 수 있도록 시스템을 구축했습니다.
  -  [코드 링크](https://github.com/chocobubble/LS/tree/main/Source/LooterShooter/System)
#### 3. 컴포넌트를 활용하여 방대해진 클래스의 크기를 줄이고, 다른 객체에 재활용했습니다.  
  - 문제점
    - 플레이어 캐릭터 클래스를 제작하면서 관련 기능 대부분을 한 클래스에 제작하다 보니 클래스가 너무 커져 유지 보수가 점점 어려워졌습니다. 그리고 같은 기능을 몬스터 클래스에도 재활용해야 하는 상황이 발생했습니다.
  - 해결 방안
    - 컴포넌트 디자인 패턴을 활용해 각 기능들을 분리하고 재활용했습니다. 
  - [코드 링크](https://github.com/chocobubble/LS/tree/main/Source/LooterShooter/Component)
#### 4. 유연하고 확장성 있는 기능 구현을 위해 다형성을 이용했습니다.
  - 문제점
    -  처음 스킬 구현 시 플레이어 캐릭터 클래스 내에 구현하고 시전을 했는데, 스킬을 추가할 때 기존의 코드를 활용하지 못해 클래스 크기가 비효율적으로 커지는 문제점이 있었습니다.
  - 해결 방안
    -  스킬 부모 클래스를 만들고 각 스킬의 세부사항은 자식 클래스로 구현한 뒤, 캐릭터는 부모 클래스의 스킬 시전 메서드만 호출하는 식으로 간소화했습니다.
  - [코드 링크](https://github.com/chocobubble/LS/tree/main/Source/LooterShooter/Skill)

<br>

<br>

## 기술 블로그
- 게임 클라이언트 프로그래머가 되기 위해 관련 지식을 책과 유데미 강의를 통해 쌓았습니다.
- 이를 정리하여 Github 블로그에 포스팅하고 있습니다.  
  [<img width="523" alt="blog" src="./Images/Blog.png">](https://chocobubble.github.io/)

---

> 이하 각 프로젝트의 세부 설명입니다.

<br><br>

# LooterShooter

## 프로젝트 소개
> GitHub : [LS Project](https://github.com/chocobubble/LooterShooter)  
> Wiki : [LS Wiki](https://github.com/chocobubble/LooterShooter/wiki)

- 게임 장르 : looter shooter(RPG + TPS)  
- 제작 기간 : 2023. 6. ~ 현재
- 제작 인원 : 1인 (개인 프로젝트)
- 사용 엔진 : Unreal Engine v5.2 
- 언어 : C++

### 플레이 영상
- 이미지 클릭 시 유튜브에서 영상이 실행됩니다.

[![play](https://img.youtube.com/vi/FKlwz-1G0EQ/0.jpg)](https://youtu.be/FKlwz-1G0EQ)

<br>

## 주요 내용

### 1. GitHub의 Project, Issue, Wiki 등을 이용한 프로젝트 관리
프로젝트 일정 및 목표 관리, 코드 기록 등의 필요성을 느끼고 GitHub의 Project, Issue, Wiki 등의 기능을 이용해 프로젝트를 제작했습니다. 

- Project
  - GitHub의 Project를 이용하여 프로젝트 일정을 관리 했습니다.
  
     [<img width="750" alt="project" src="./Images/Project_main.JPG">](https://github.com/users/chocobubble/projects/2)

- Issue
  - GitHub의 Project에 들어가는 Issue들이며, Git Commit 과 연동해 각 Issue에 해당하는 Commit들을 바로 확인할 수 있었습니다.
  - 체크박스를 통해 세부 목표관리를 했습니다.
  
   [<img width="750" alt="Issue" src="./Images/Project_issue_2.JPG">](https://github.com/chocobubble/LS/issues/11)


- Wiki
  - 프로젝트에서 구현한 기능들을 GitHub의 Wiki를 통해 정리했습니다.
  
   [<img width="523" alt="wiki" src="./Images/Wiki.png">](https://github.com/chocobubble/LS/wiki)


<br>

### 2. 데이터 시스템을 구축을 통한 데이터와 코드의 분리
>  [[Wiki]](https://github.com/chocobubble/LS/wiki/%EB%8D%B0%EC%9D%B4%ED%84%B0-%EC%8B%9C%EC%8A%A4%ED%85%9C)
- 프로젝트 초기에는 무기나 캐릭터 스탯 등 수치들을 코드로 설정했고, 프로젝트가 진행되면서 이런 데이터를 수정할 때마다 코드 수정 과정에서 에러가 생기는 등의 문제가 있었습니다. 
- 해결 방법으로 데이터 시스템을 구축해했고, C++ 코드에 의존적이지 않게 데이터들을 관리할 수 있게 했습니다. 
- 또한 이렇게 구축한 데이터 시스템을 통해 비프로그래머도 프로그래머의 도움 없이 게임 내 데이터 수정이 가능합니다.


<br>

### 3. 클래스의 크기를 줄이고, 다른 객체에 재활용하기 위한 컴포넌트 활용
> [[Wiki]](https://github.com/chocobubble/LS/wiki/%EC%BB%B4%ED%8F%AC%EB%84%8C%ED%8A%B8)
- RPG 게임 특성상 캐릭터를 구현하는 클래스의 크기가 커져 수정 및 확장이 용이하지 않았습니다. 
- 이런 문제를 해결하기 위해 컴포넌트 기반 설계를 도입했습니다. 
- Defense, Resource, Equipment, Inventory 등의 기능을 컴포넌트로 분리했으며, 이를 몬스터 구현 등에 재사용했습니다. 
- 그리고 컴포넌트 간의 의존성을 줄이기 위해 delegate를 이용했습니다.

<br>

### 4. 유연하고 확장성 있는 기능 구현을 위한 다형성 활용
> [[Wiki]](https://github.com/chocobubble/LS/wiki/%EB%8B%A4%ED%98%95%EC%84%B1)
- 스킬을 추가하는 과정에서 캐릭터 클래스가 과도하게 커지는 경향이 있었고, 그 과정 속에서 에러가 발생하는 경우가 있었습니다.
- 해결 방안으로 다형성을 이용하여 유연하고 확장성 있게 부가 속성을 구현했습니다.
 
---

<br>

### 프로젝트 Wiki
> [[Document]](https://github.com/chocobubble/LooterShooter/wiki/Document)

- GitHub의 Wiki에 프로젝트에서 구현한 기능들을 정리했습니다.
- 아래 링크를 통해 확인 가능합니다.

### 프로젝트 소스 코드
> [[GitHub]](https://github.com/chocobubble/LooterShooter/tree/main/Source/LooterShooter)

- 프로젝트의 GitHub 링크입니다.

<br><br>

> [Back to Top](#프로젝트)

