# 언리얼 엔진 데일리 브리핑 | 2025년 12월 09일

작성일: 2025-12-09 (KST)

## 1. 핵심 요약

언리얼 엔진 5.7.1 핫픽스가 릴리즈되어 약 100여 개의 버그가 수정되었으며, 특히 Game Animation Sample Project(GASP)를 통해 **Mover 플러그인**의 새로운 기능들이 공개되었습니다.

### 주요 업데이트 상위 3개

1.  **UE 5.7.1 핫픽스 릴리즈:** 5.7 버전의 안정성을 높이는 약 100여 개의 버그 수정 및 업데이트가 포함된 핫픽스가 릴리즈되었습니다.
2.  **Mover 플러그인 (Experimental) 기능 공개:** GASP 업데이트를 통해 롤백 네트워킹을 지원하는 Mover 플러그인의 새로운 이동 모드(Simple Spring Walking Mode, Smooth Walking Mode)와 슬라이드 메커니즘이 공개되었습니다.
3.  **주요 버그 수정:** Path Tracer의 노멀 맵 이슈, Niagara 이펙터 상속 문제, Sequencer의 Python 트랜스폼 베이킹 문제 등 다수의 중요 버그가 해결되었습니다.

### 즉시 확인 필요 사항

*   **Linux SDL3 전환:** UE 5.7부터 Linux 플랫폼은 SDL2에서 SDL3로 전환됩니다. Linux 환경에서 SDL2 코드를 커스터마이징한 개발자는 **SDL3에 맞게 변경 사항을 재작업**해야 합니다.
*   **Texture Streaming 메모리 스파이크 버그:** 텍스처 스트리밍에서 레이스 컨디션으로 인해 모든 밉(Mip)이 로드되어 **대규모 메모리 스파이크**를 유발할 수 있는 버그(UE-348042)가 새로 보고되었습니다.

### 출처 URL 및 게시일

| 정보 출처 | 게시일 (YYYY-MM-DD) | URL |
| :--- | :--- | :--- |
| UE 5.7.1 Hotfix | 2025-12-02 | [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) |
| GASP 5.7 Update | 2025-12-03 | [https://www.unrealengine.com/en-US/tech-blog/explore-the-updates-to-the-game-animation-sample-project-in-ue-5-7](https://www.unrealengine.com/en-US/tech-blog/explore-the-updates-to-the-game-animation-sample-project-in-ue-5-7) |
| Issue Tracker | 2025-12-09 | [https://issues.unrealengine.com/](https://issues.unrealengine.com/) |

## 2. 공식 릴리즈 및 패치

### 버전 릴리즈 (정확한 버전 번호)

*   **Unreal Engine 5.7.1 Hotfix**

### 주요 변경사항 및 Breaking Changes

*   **주요 변경사항:** 약 100여 개의 버그 수정에 초점을 맞춘 안정화 핫픽스입니다.
*   **Breaking Changes:** UE 5.7 버전부터 **Linux 플랫폼**의 SDL 라이브러리가 **SDL2에서 SDL3로 전환**되었습니다. 기존 SDL2 코드를 커스터마이징한 경우, UE 5.7 이상 버전으로 전환 시 SDL3에 맞게 코드를 수정해야 합니다.

### 릴리즈 노트 URL

*   [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)

## 3. 버그 및 이슈

### 새로 보고된 주요 버그 (Latest Bugs)

| 이슈 ID | 요약 | 영향받는 시스템 |
| :--- | :--- | :--- |
| UE-348042 | **Texture Streaming**에서 레이스 컨디션으로 인해 모든 밉이 로드되어 **대규모 메모리 스파이크** 발생 가능성 | Graphics Features |
| UE-348043 | **Text3D**에서 `UText3DDefaultLayoutExtension::PreRendererUpdate()` 크래시 발생 | Text3D |
| UE-348759 | **RigVMDeveloper**에서 `URigVMNode::FindPin()` 크래시 발생 | RigVMDeveloper |
| UE-349638 | **PCG**에서 PIE(Play In Editor) 시 에디터와 게임 월드가 모두 렌더링되어 렌더링 비용이 두 배로 증가 | PCG |
| UE-349879 | **Landscape Spline** 중간 지점을 삭제하고 취소할 때 Assert/크래시 발생 | Landscape |

### 수정된 버그 (Latest Fixes in Issue Tracker & 5.7.1 Hotfix)

*   **Path Tracer Normals Issue:** Path Tracing에서 노멀 맵이 Lit 모드와 다르게 부정확하게 반영되던 문제 해결.
*   **Niagara Emitter Inheritance:** 이펙터의 보간된 스폰 모드를 "No Interpolation"으로 변경 후 모듈이 잠금 해제되고 상속이 손실되던 문제 해결.
*   **Sequencer Python:** Python 스크립트에서 `bake_transform_with_settings` 메서드가 5.7에서 작동하지 않던 문제 해결.
*   **Datasmith Lights:** Twinmotion 2025.1.1에서 Datasmith를 통해 가져온 라이트의 트랜스폼이 부정확하던 문제 해결.
*   **5.7.1 Hotfix 주요 수정:**
    *   Path Tracing 뷰 모드 활성화 시 에디터 응답 없음 (UE-193929)
    *   MetaHuman 캐릭터 LOD 변경 시 크래시 (MH-16702)
    *   Vulkan에서 Split Barriers 사용 시 `VkEvent` 핸들 누수 (UE-352196)

### Workaround

*   **Texture Streaming 메모리 스파이크 (UE-348042):** 현재 공식적인 Workaround는 없으나, 임시적으로 텍스처 스트리밍을 비활성화하거나 텍스처 풀 크기를 조정하여 완화할 수 있습니다.

### Issue Tracker URL

*   [https://issues.unrealengine.com/](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

### 주요 커밋 및 Pull Request

Epic Games의 공식 `EpicGames/UnrealEngine` 저장소에 대한 직접적인 접근은 제한되어 있으므로, 최근 7일간의 **사용자 저장소(`soohk314-glitch/UnrealEngine`)** 커밋 활동을 기준으로 보고합니다.

| 커밋 해시 | 커밋 메시지 | 커밋 날짜 (UTC-5) |
| :--- | :--- | :--- |
| `a0cd812` | Daily Briefing: Unreal Engine Update for 2025-12-08 | 2025-12-07 18:08:48 |
| `cc054ca` | Daily Briefing: 2025-12-06 Unreal Engine Update | 2025-12-06 18:04:23 |
| `e6f1f16` | Daily Briefing: Unreal Engine Updates for 2025-12-06 | 2025-12-05 18:06:21 |

### 영향받는 시스템

*   보고서 자동 생성 시스템 (Daily Briefing)

### GitHub URL

*   [https://github.com/soohk314-glitch/UnrealEngine](https://github.com/soohk314-glitch/UnrealEngine)

## 5. 공식 포럼 기술 논의

### Epic Staff 답변 기술 스레드

최근 7일 이내에 Epic Staff가 답변한 새로운 기술 스레드는 검색되지 않았습니다. 가장 최근의 공식 활동은 **UE 5.7.1 Hotfix 릴리즈** 공지입니다.

*   **스레드 제목:** 5.7.1 Hotfix Released
*   **주요 내용:** 5.7.1 핫픽스에 대한 공지 및 피드백 수렴. 핫픽스에는 약 100여 개의 수정 사항이 포함되어 있습니다.
*   **Epic Staff:** TinaWisdom (@Tina_Wisdom)
*   **게시일:** 2025-12-02

### 포럼 URL

*   [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7.1-hotfix-released/2681235)

## 6. 신기능 및 실험적 기능

### 새로 추가된 기능

*   **Game Animation Sample Project (GASP) 업데이트:** UE 5.7에 맞춰 GASP가 업데이트되었으며, 400개의 새로운 애니메이션과 함께 새로운 기능들이 추가되었습니다.

### Beta/Experimental 기능 및 주의사항

*   **Mover 플러그인 (Experimental):**
    *   **기능:** Network Prediction Plugin 또는 Chaos Networked Physics를 사용하여 **롤백 네트워킹**을 지원하는 액터 이동을 지원합니다.
    *   **목표:** 기존 Character Movement Component의 후속작으로, 개발자가 네트워킹 전문가가 아니더라도 모션 제작에 집중할 수 있도록 돕는 것을 목표로 합니다.
    *   **새로운 이동 모드:** `Simple Spring Walking Mode`와 `Smooth Walking Mode`가 추가되었습니다.
    *   **주의사항:** 현재 **Experimental** 단계에 있으며, UE 5.8에서 UAF(Unreal Animation Framework)와 함께 더욱 발전될 예정입니다.
*   **Unreal Animation Framework (UAF) 개발 현황:**
    *   **기능:** Anim Blueprints를 대체할 미래의 애니메이션 시스템입니다.
    *   **현황:** 5.7에서는 Control Rig에 `Footplacement Control Rig` 노드를 추가하는 등 기반을 다지고 있으며, **5.8에서 첫 번째 Experimental 버전**이 GASP에 포함될 예정입니다.

### 성능 영향도

*   **PCG 렌더링 비용 증가 (버그):** PCG에서 PIE 시 에디터와 게임 월드가 모두 렌더링되어 렌더링 비용이 두 배로 증가하는 버그(UE-349638)가 보고되었습니다. 이 버그가 수정되기 전까지는 PCG를 사용하는 프로젝트의 PIE 성능에 주의가 필요합니다.

## 7. 플러그인 및 문서 업데이트

### 공식 플러그인 업데이트

*   **EOS (Epic Online Services):** 5.7.1 핫픽스에 EOS 1.18.1.2 바이너리 업데이트가 포함되었습니다.
*   **Mover Plugin:** GASP 업데이트를 통해 새로운 기능이 추가되었습니다.

### 문서 주요 변경사항

*   **Game Animation Sample Project (GASP) 문서 업데이트:** Mover 플러그인, Smart Objects, 새로운 애니메이션 데이터셋 관련 내용이 업데이트되었습니다.
*   **SDL3 전환 문서:** Linux 개발자를 위한 SDL2에서 SDL3로의 전환 관련 문서가 중요하게 다뤄지고 있습니다.
