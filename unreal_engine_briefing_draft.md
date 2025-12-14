# 언리얼 엔진 데일리 브리핑 | 2025년 12월 14일

작성 시간: 18시 05분 48초 (KST)
출처: [1] [2] [3]

## 1. 핵심 요약

### 주요 업데이트 상위 3개
1.  **Unreal Engine 5.7.1 핫픽스 출시**: 100여 개에 달하는 주요 버그 및 크래시 문제가 수정되었습니다.
2.  **Substrate 프로덕션 레디**: 새로운 모듈형 머티리얼 프레임워크인 **Substrate**가 UE 5.7에서 정식 기능으로 전환되었습니다.
3.  **MegaLights 베타 진입**: 성능 개선 및 노이즈 감소와 함께 Directional Light, Translucency, Hair Strands 등을 지원하며 베타 단계로 진입했습니다.

### 즉시 확인 필요 사항
*   **Linux 개발 환경의 SDL3 전환**: UE 5.7부터 Linux 빌드 환경이 SDL2에서 **SDL3**로 전환되었습니다. SDL2 코드를 커스터마이징한 사용자는 SDL3에 맞게 코드를 수정해야 합니다.

### 출처 URL 및 게시일
| 업데이트 | 버전 | 게시일 (YYYY-MM-DD) | URL |
| :--- | :--- | :--- | :--- |
| 핫픽스 | 5.7.1 | 2025-12-02 | [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) |
| 메이저 릴리즈 | 5.7 | 2025-11-12 | [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) |

## 2. 공식 릴리즈 및 패치

### 버전 릴리즈 (정확한 버전 번호)
*   **Unreal Engine 5.7.1 Hotfix** (2025년 12월 2일 출시)

### 주요 변경사항 및 Breaking Changes
*   **주요 변경사항**: 5.7.1 핫픽스는 5.7 버전에서 발견된 약 100여 개의 버그 및 안정성 문제를 해결하는 데 중점을 두었습니다.
*   **Breaking Changes**: UE 5.7부터 Linux 개발 환경에서 **SDL2**가 **SDL3**로 대체되었습니다. SDL2 관련 커스터마이징 코드를 사용하는 개발자는 SDL3에 맞게 변경해야 합니다.

### 릴리즈 노트 URL
*   **UE 5.7.1 Hotfix**: [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)
*   **UE 5.7 Major Release**: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)

## 3. 버그 및 이슈

### 새로 보고된 주요 버그
*   최근 7일간 공식 이슈 트래커에서 주목할 만한 새로운 주요 버그 보고는 확인되지 않았습니다.

### 수정된 버그 (5.7.1 Hotfix 기준)
5.7.1 핫픽스에서 수정된 주요 버그 목록 (일부 발췌):
*   `UE-193929`: Path Tracing 뷰 모드 활성화 시 mGPU 환경에서 에디터 응답 없음 현상.
*   `UE-227868`: Cinematic MetaHumans가 레벨 뷰포트에 있을 때 AMD GPU 크래시.
*   `UE-349638`: PCG가 PIE(Play In Editor)에서 생성될 때 에디터와 게임 월드가 모두 렌더링되어 렌더링 비용이 두 배가 되는 문제.
*   `UE-352089`: Full Body IK Solver에 IK Goal 추가 시 크래시.
*   `MH-16864`: MetaHuman Creator에서 익스포트된 SKM과 상호작용 시 크래시.

### Workaround
*   최근 7일간 새로운 Workaround 정보는 확인되지 않았습니다.

### Issue Tracker URL
*   [https://issues.unrealengine.com/](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

### 주요 커밋 및 Pull Request
*   최근 7일간 EpicGames/UnrealEngine 메인 브랜치에서 실무 개발자에게 직접적인 영향을 미치는 주요 기술 커밋이나 Pull Request는 확인되지 않았습니다.
*   **참고**: 5.7.1 핫픽스에는 커뮤니티 기여자들의 수정 사항이 포함되어 있습니다.

### 영향받는 시스템
*   최근 7일간 주요 업데이트 없음.

### GitHub URL
*   [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

### Epic Staff 답변 기술 스레드
*   **UE 5.7.1 Hotfix 출시** 공지 스레드가 가장 최근의 공식적인 기술 업데이트 논의입니다.
    *   **주요 내용**: Linux 개발 환경의 SDL2 → SDL3 전환에 대한 주의사항이 언급되었습니다.

### 포럼 URL
*   **5.7.1 Hotfix Released**: [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)
*   **Announcements**: [https://forums.unrealengine.com/c/general/announcements/49](https://forums.unrealengine.com/c/general/announcements/49)

## 6. 신기능 및 실험적 기능 (UE 5.7 기준)

### 새로 추가된 기능
*   **Substrate**: 프로덕션 레디로 전환되어 기본 활성화. 모듈형, 물리 기반 머티리얼 프레임워크.
*   **Blendshapes and Sculpting Tools**: 스켈레탈 에디터에 통합되어 모프 셰이프, 본, 스킨 웨이트를 에디터 내에서 편집 가능.
*   **World Collisions for Control Rig Physics**: Control Rig 물리 시뮬레이션에 레벨 충돌 지원 추가.

### Beta/Experimental 기능 및 주의사항
| 기능 | 상태 | 주요 내용 | 주의사항 |
| :--- | :--- | :--- | :--- |
| **MegaLights** | Beta | 노이즈 감소 및 성능 개선. Directional Light, Translucency, Hair Strands 지원. | 베타 기능으로 프로덕션 사용 시 주의 필요. |
| **Niagara Heterogeneous Volumes** | Beta | 그림자 캐스팅 개선. Cascade shadows, Beer Shadow Map 지원. | 베타 기능으로 프로덕션 사용 시 주의 필요. |
| **Nanite Foliage and Skinning** | Experimental | Nanite Assemblies, Nanite Skinning, Nanite Voxels를 활용한 고성능 포리지 렌더링. | 실험적 기능으로 API 변경 및 불안정성이 있을 수 있음. |
| **SMAA** | Experimental | 모바일 및 데스크톱 렌더러에서 Subpixel Morphological Anti-Aliasing 지원. | CVar (`r.Mobile.AntiAliasing=5`)를 통해 활성화 필요. |
| **Motion Matching Chooser Integration** | Experimental | 모션 매칭에 Chooser 통합. | 실험적 기능. |
| **Spatially Aware Retargeting** | Experimental | 리타겟팅 시 자체 충돌 방지 기능. | 실험적 기능. |

### 성능 영향도
*   **FBIK 및 Retargeting 성능 개선**: Full Body IK 성능 약 **20%** 향상.
*   **Nanite Foliage**: 현세대 하드웨어에서 60fps 예산 내에서 사실적인 애니메이션 포리지 구현 가능.

## 7. 플러그인 및 문서 업데이트

### 공식 플러그인 업데이트
*   **Microsoft GDK Plug-ins for Unreal Engine**: UE 5.7 릴리즈와 함께 GDK 플러그인이 출시되어 Xbox PC App으로의 게임 이식을 간소화합니다. (2025-12-12)

### 문서 주요 변경사항
*   **UE 5.7 Documentation** 업데이트: Substrate, PCG, 애니메이션 툴셋 등 새로운 기능에 대한 문서가 대폭 보강되었습니다.

## 참고 자료
[1] Unreal Engine 5.7 Release Notes. Epic Developer Community. [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)
[2] 5.7.1 Hotfix Released. Epic Developer Community Forums. [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)
[3] Microsoft GDK Plug-ins for Unreal Engine are Now Available. Microsoft Developer Blog. [https://developer.microsoft.com/en-us/games/articles/2025/12/microsoft-gdk-plug-ins-for-unreal-engine-now-available/](https://developer.microsoft.com/en-us/games/articles/2025/12/microsoft-gdk-plug-ins-for-unreal-engine-now-available/)
