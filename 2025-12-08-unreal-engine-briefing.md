# 언리얼 엔진 데일리 브리핑 | 2025년 12월 8일

본 보고서는 실무 개발자를 위해 언리얼 엔진의 최신 기술 업데이트, 릴리즈, 패치, 버그 정보를 요약하여 제공합니다.

## 1. 핵심 요약

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **UE 5.7.1 핫픽스 릴리즈**: 약 100여 개의 버그 및 업데이트 수정 [1].<br>2. **Substrate 정식 기능 전환**: 모듈식 물리 기반 머티리얼 프레임워크가 UE 5.7에서 정식으로 활성화 [3].<br>3. **Nanite Foliage 및 Skinning (실험적)**: 대규모 환경을 위한 새로운 렌더링 경로 도입 [3]. |
| **즉시 확인 필요 사항** | **UE 5.7.1 핫픽스**에 포함된 다수의 크래시 및 버그 수정 사항을 확인하고, 특히 **Linux 환경**에서 **SDL2에서 SDL3로의 전환**에 따른 사용자 정의 코드의 재작업 필요성을 인지해야 합니다 [1]. |
| **출처 URL 및 게시일** | - **UE 5.7.1 Hotfix**: [Epic Developer Community Forums](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) (2025-12-02) [1]<br>- **UE 5.7 Release Notes**: [Epic Developer Community Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (2025-11-12) [3] |

## 2. 공식 릴리즈 및 패치

### 버전 릴리즈
가장 최근의 공식 릴리즈는 **Unreal Engine 5.7.1 Hotfix**입니다. 이는 2025년 12월 2일에 릴리즈되었으며, 약 100여 개의 수정 사항을 포함하고 있습니다 [1].

### 주요 변경사항 및 Breaking Changes
UE 5.7.1 핫픽스는 주로 안정성 및 버그 수정에 초점을 맞추고 있습니다.

*   **주요 수정 사항**: 다수의 크래시 보고서(CrashReport) 관련 이슈 및 MetaHuman, nDisplay, PCG, Sequencer 등 다양한 시스템의 버그가 수정되었습니다 [1].
*   **Breaking Changes (UE 5.7 기준)**:
    *   **Linux 환경 SDL3 전환**: UE 5.7부터 Linux 환경에서 SDL2가 SDL3로 전환되었습니다. SDL2 코드를 사용자 정의한 경우, UE 5.7로 전환 시 해당 변경 사항을 SDL3에 맞게 재작업해야 합니다 [1].

### 릴리즈 노트 URL
*   **UE 5.7.1 Hotfix**: [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) [1]
*   **UE 5.7 Release Notes**: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) [3]

## 3. 버그 및 이슈

언리얼 엔진 이슈 트래커([https://issues.unrealengine.com/](https://issues.unrealengine.com/))에서 확인된 주요 버그 및 수정 사항은 다음과 같습니다 [4].

### 새로 보고된 주요 버그 (Latest Bugs)
| 이슈 ID | 요약 | 영향받는 시스템 |
| :--- | :--- | :--- |
| (미제공) | Texture Streaming can randomly streams in all Mips, causing large memory spikes | Graphics Features |
| (미제공) | LI Property Override: LI internal references are broken when saving the overrides. | World Creation - Worldbuilding Tools - Level Instances |
| (미제공) | Morph target is not applied on the first frame in Level Sequence | Anim - Runtime |

### 수정된 버그 (Latest Fixes)
| 이슈 ID | 요약 | 영향받는 시스템 |
| :--- | :--- | :--- |
| (미제공) | Path Tracer Normals Issue | Graphics Features - Path Tracer |
| (미제공) | The bake\_transform\_with\_settings method works in 5.6 but not 5.7 | Anim - Sequencer |
| (미제공) | Issue with Niagara emitter inheritance | Niagara |

### Workaround
별도의 공식적인 Workaround는 제공되지 않았으나, 5.7.1 핫픽스에 다수의 크래시 및 버그 수정 사항이 포함되어 있으므로, 해당 버전으로의 업데이트를 권장합니다 [1].

### Issue Tracker URL
*   [https://issues.unrealengine.com/](https://issues.unrealengine.com/) [4]

## 4. GitHub 업데이트

Epic Games의 언리얼 엔진 GitHub 저장소는 비공개 저장소이므로, 최근 7일간의 커밋 로그에 대한 직접적인 접근은 불가능합니다.

### 주요 커밋 및 Pull Request
최근 7일간의 주요 커밋 정보는 공개적으로 제공되지 않습니다. 다만, **UE 5.7 릴리즈 노트**에는 커뮤니티 개발자들의 기여가 언급되어 있으며, 이는 지속적인 Pull Request 병합을 통해 이루어지고 있음을 시사합니다 [3].

### 영향받는 시스템
GitHub 커밋은 엔진의 모든 영역에 영향을 미치지만, 5.7.1 핫픽스에 포함된 수정 사항을 통해 **RHI, Control Rig, PCG, Sequencer** 등 다양한 시스템에서 버그 수정 및 안정화 작업이 이루어졌음을 유추할 수 있습니다 [1].

### GitHub URL
*   **EpicGames/UnrealEngine**: [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

### Epic Staff 답변 기술 스레드
최근 7일간 Epic Staff가 답변한 특정 기술 스레드는 검색되지 않았습니다. 가장 최근의 공식적인 포럼 활동은 **UE 5.7.1 Hotfix Released** 공지입니다 [1].

### 포럼 URL
*   **Epic Developer Community Forums - Announcements**: [https://forums.unrealengine.com/c/general/announcements/49](https://forums.unrealengine.com/c/general/announcements/49)

## 6. 신기능 및 실험적 기능

가장 최근의 주요 버전인 **Unreal Engine 5.7**에 포함된 신기능 및 실험적 기능은 다음과 같습니다 [3].

### 새로 추가된 기능
*   **Substrate**: 새로운 머티리얼 프레임워크가 **Production-Ready**로 전환되어 기본 활성화되었습니다.
*   **MegaLights (Beta)**: 노이즈 감소 및 성능 개선과 함께 Directional Light, Niagara Particle Lights, Translucency, Hair Strands 지원이 추가되었습니다.
*   **Niagara Heterogeneous Volumes (Beta)**: 그림자 캐스팅 개선(Cascade shadows, Beer Shadow Map) 및 성능 최적화가 이루어졌습니다.
*   **Blendshapes and Sculpting Tools**: 스켈레탈 에디터에 블렌드셰이프 생성 및 편집, 스킨 웨이트 페인팅 기능이 통합되었습니다.

### Beta/Experimental 기능 및 주의사항
| 기능 | 상태 | 주요 내용 및 주의사항 |
| :--- | :--- | :--- |
| **Nanite Foliage and Skinning** | Experimental | Nanite Assemblies, Nanite Skinning, Nanite Voxels를 활용한 대규모 환경 폴리지 렌더링 경로. |
| **SMAA (Subpixel Morphological Anti-Aliasing)** | Experimental | 모바일 및 데스크톱 렌더러 지원. `r.Mobile.AntiAliasing=5` 또는 `r.AntiAliasingMethod=5`로 활성화. |
| **Motion Matching Chooser Integration** | Experimental | 모션 매칭을 Chooser에 통합하여 에셋 선택에 대한 제어력 강화. |
| **Spatially Aware Retargeting** | Experimental | 리타겟팅 시 자체 충돌을 방지하기 위해 물리 기반으로 IK 목표를 밀어내는 기능. |

### 성능 영향도
*   **FBIK 및 Retargeting 성능**: Full Body IK 및 IK Retargeter의 성능이 약 **20%** 향상되었습니다 [3].
*   **SMAA**: 최소한의 성능 영향으로 높은 품질의 엣지 스무딩을 제공하여 모바일 게임에 효율적입니다 [3].

## 7. 플러그인 및 문서 업데이트

### 공식 플러그인 업데이트
*   **EOS (Epic Online Services)**: 5.7.1 핫픽스에 **EOS: 1.18.1.2 Binary Update**가 포함되었습니다 [1].
*   **Mover Plugin**: UE 5.7 업데이트와 함께 Game Animation Sample Project가 업데이트되었으며, **Mover 플러그인** 및 Smart Object 설정이 개선되었습니다 [5].

### 문서 주요 변경사항
*   **Unreal Engine 5.7 Documentation**이 릴리즈되었으며, 주요 신기능에 대한 상세 문서가 업데이트되었습니다 [3].
*   **Game Animation Sample Project**의 업데이트 내용이 기술 블로그를 통해 상세히 소개되었습니다 [5].

---
### References
[1] [5.7.1 Hotfix Released - General / Announcements - Epic Developer Community Forums](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)
[2] [Unreal Engine 5.7 is now available - Unreal Engine](https://www.unrealengine.com/en-US/news/unreal-engine-5-7-is-now-available)
[3] [Unreal Engine 5.7 Release Notes | Unreal Engine 5.7 Documentation | Epic Developer Community](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)
[4] [Unreal Engine Issues and Bug Tracker](https://issues.unrealengine.com/)
[5] [Explore the updates to the Game Animation Sample project in UE 5.7 - Unreal Engine](https://www.unrealengine.com/en-US/tech-blog/explore-the-updates-to-the-game-animation-sample-project-in-ue-5-7)
