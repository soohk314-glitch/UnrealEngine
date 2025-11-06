# 언리얼 엔진 데일리 브리핑 | 2025년 11월 07일

**작성일:** 2025년 11월 07일 (KST)
**정보 출처:** Unreal Engine 공식 포럼, Issue Tracker, GitHub

## 1. 핵심 요약

| 순위 | 주요 업데이트 | 영향 시스템 | 출처 URL 및 게시일 |
| :--- | :--- | :--- | :--- |
| 1 | **UE 5.6.1 핫픽스 릴리즈** | 엔진 전반, MetaHuman, 렌더링, 시퀀서 | [포럼](https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316) (2025-08-12) |
| 2 | **MetaHuman 관련 버그 다수 수정** | MetaHuman Character, UEFN, DataFlow | [포럼](https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316) (2025-08-12) |
| 3 | **UE 5.7의 Linux SDL3 전환 예고** | Linux 빌드 시스템 | [포럼](https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316) (2025-08-12) |

**즉시 확인 필요 사항:**
*   **UE 5.6.1 핫픽스**는 270개 이상의 수정 사항을 포함하고 있으며, 특히 **MetaHuman** 관련 크래시 및 기능 문제가 다수 해결되었습니다. 5.6 버전을 사용하는 프로젝트는 안정성을 위해 업데이트를 고려해야 합니다.
*   **UE 5.7**부터 Linux 빌드 환경이 **SDL2에서 SDL3로 전환**될 예정입니다. Linux 환경에서 커스터마이징된 SDL2 코드를 사용하는 개발자는 사전 대비가 필요합니다.

## 2. 공식 릴리즈 및 패치

**버전 릴리즈:** Unreal Engine 5.6.1 Hotfix
**릴리즈 일자:** 2025년 08월 12일

**주요 변경사항 및 Breaking Changes:**
*   **주요 변경사항:** 5.6 버전의 안정성 및 버그 수정에 초점을 맞춘 핫픽스입니다. 270개 이상의 수정 사항이 포함되었습니다.
*   **Breaking Changes:** 릴리즈 노트에 명시된 주요 Breaking Change는 없으나, **UE 5.7**에서 Linux 빌드 시스템이 SDL2에서 SDL3로 전환될 예정임을 미리 고지했습니다. SDL2 코드를 커스터마이징한 경우 UE 5.7 전환 시 변경 작업이 필요합니다.

**릴리즈 노트 URL:**
[https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316](https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316)

## 3. 버그 및 이슈

**최근 7일간 새로운 업데이트 사항이 없습니다. (2025-11-07 기준)**

**새로 보고된 주요 버그 (Issue Tracker 최신 정보):**
| 이슈 ID | 요약 | 영향 시스템 |
| :--- | :--- | :--- |
| **UE-290873** | Third Person Platforming - 일부 경우 플레이어 캐릭터가 더블 점프를 수행할 수 없음 | Third Person Template |
| **UE-290607** | 네이밍 토큰 블루프린트 클래스 생성 시 크래시 발생 | 블루프린트 |
| **UE-290599** | MCR 에셋 컴파일 후 Modular Control Rig 레벨 시퀀스에서 Undo/Redo 시 크래시 발생 | Control Rig, Sequencer |

**수정된 버그 (Issue Tracker 최신 정보):**
| 이슈 ID | 요약 | 영향 시스템 |
| :--- | :--- | :--- |
| **UE-284851** | 체인이 구형 콜리전에서 튕겨나가는 문제 | Physics |
| **UE-282213** | PCG 자체 가지치기 및 복잡한 콜리전 사용 시 에디터 크래시 | PCG |
| **UE-274151** | Mac에서 카메라 액터를 복제하고 삭제할 때 크래시 발생 | Mac, Editor |

**Workaround:**
*   공식적으로 제공된 Workaround는 없습니다.

**Issue Tracker URL:**
[https://issues.unrealengine.com/](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

**최근 7일간 EpicGames/UnrealEngine 저장소의 주요 커밋 및 Pull Request 업데이트가 확인되지 않았습니다. (2025-11-07 기준)**

**가장 최근 확인된 주요 커밋 (UE 5.6.1 핫픽스 관련):**
*   **GitHub 11643**: `Allow Mutable CustomizableObjects to be compiled in -game mode` (UE-210136)
    *   **영향받는 시스템:** Mutable, Customizable Objects
    *   **내용:** Mutable Customizable Objects를 게임 모드에서 컴파일할 수 있도록 허용하는 변경 사항이 5.6.1 핫픽스에 포함되었습니다.

**GitHub URL:**
[https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

**최근 7일간 Epic Staff가 답변한 새로운 기술 스레드가 확인되지 않았습니다. (2025-11-07 기준)**

**가장 최근 주목할 만한 스레드 (2025-11-06):**
*   **제목:** `update currently distributed Engine versions to address CVE-2025-55247 effecting 5.4, 5.5, 5.6`
    *   **내용:** CVE-2025-55247 보안 취약점을 해결하기 위해 현재 배포 중인 엔진 버전(5.4, 5.5, 5.6)에 대한 업데이트 필요성이 논의되고 있습니다. 이는 잠재적인 보안 핫픽스 릴리즈를 예고할 수 있습니다.
    *   **포럼 URL:** [https://forums.unrealengine.com/t/update-currently-distributed-engine-versions-to-address-cve-2025-55247-effecting-5-4-5-5-5-6/2672485](https://forums.unrealengine.com/t/update-currently-distributed-engine-versions-to-address-cve-2025-55247-effecting-5-4-5-5-5-6/2672485)

## 6. 신기능 및 실험적 기능

**최근 7일간 새로운 신기능 또는 실험적 기능에 대한 공식 발표가 확인되지 않았습니다. (2025-11-07 기준)**

**가장 최근 주목할 만한 기능 (UE 5.6.1 핫픽스 노트 내):**
*   **기능:** **MetaHuman DataFlow** 관련 버그 수정 (MH-15708, MH-15709)
    *   **내용:** DataFlow가 에셋을 올바르게 업데이트하지 못하거나, 의상 리사이징을 위한 잘못된 바디를 선택하는 문제가 해결되었습니다. 이는 MetaHuman 파이프라인의 안정성을 향상시킵니다.
*   **기능:** **Motion Design** Primitive의 기본 투명 속성 변경 (UE-287600)
    *   **내용:** 2D 및 3D Motion Design Primitive의 기본 투명 속성 변경에 대한 수정 사항이 포함되었습니다.

## 7. 플러그인 및 문서 업데이트

**최근 7일간 공식 플러그인 또는 문서의 주요 변경사항에 대한 공식 발표가 확인되지 않았습니다. (2025-11-07 기준)**

**가장 최근 주목할 만한 업데이트 (UE 5.6.1 핫픽스 노트 내):**
*   **플러그인:** **Datasmith** - Mac에서 ArchiCAD 27 플러그인 로드 실패 문제 해결 (UE-284909)
*   **플러그인:** **MetaHuman** - MetaHuman 플러그인이 활성화된 프로젝트의 패키징 불가 문제 해결 (MH-15694)
*   **플러그인:** **Alias** - Alias 2026 지원 추가 (UE-229144)
