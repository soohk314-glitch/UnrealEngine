# 언리얼 엔진 데일리 브리핑 | 2025년 11월 11일

작성일: 2025년 11월 11일 (KST)

## 1. 핵심 요약

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **보안 업데이트 권고:** UE 5.4, 5.5, 5.6 버전에 영향을 미치는 .NET 관련 취약점 (**CVE-2025-55247**)에 대한 긴급 대응 및 워크어라운드 정보 공개. 2. **UE 5.7 Materials 시스템 업데이트 논의:** 공식 포럼에서 5.7 버전의 Materials 시스템 신기능 및 개선 사항에 대한 지식 기반 문서가 공유됨. 3. **RealityCapture 1.4 릴리즈:** Epic Games Launcher를 통해 RealityCapture 1.4 버전이 새로운 가격 정책과 함께 업데이트됨. |
| **즉시 확인 필요 사항** | **CVE-2025-55247 취약점 대응:** UE 5.4, 5.5, 5.6 버전을 소스 빌드하여 사용하는 개발팀은 Microsoft.Build 패키지 버전을 수동으로 업데이트해야 합니다. Epic Games의 공식 핫픽스 릴리즈를 주시해야 합니다. |
| **출처 URL 및 게시일** | [CVE-2025-55247 관련 포럼 공지](https://forums.unrealengine.com/t/update-currently-distributed-engine-versions-to-address-cve-2025-55247-effecting-5-4-5-5-5-6/2672485) (2025-11-06) |

## 2. 공식 릴리즈 및 패치

**최신 공식 릴리즈 정보:**

현재 시점(2025년 11월 11일) 기준으로 **최근 7일간 새로운 공식 엔진 버전 릴리즈(Hotfix, Minor, Major)는 확인되지 않았습니다.**

**가장 최근의 주요 업데이트 사항:**

*   **버전 릴리즈:** Epic Games는 UE 5.4, 5.5, 5.6 버전에 영향을 미치는 .NET 관련 보안 취약점 **CVE-2025-55247**에 대한 대응을 위해 엔진 버전 업데이트를 준비 중임을 알렸습니다.
*   **주요 변경사항 및 Breaking Changes:** 공식 핫픽스 릴리즈는 아직 발표되지 않았으나, 해당 취약점은 .NET의 `Microsoft.Build` 패키지 버전의 문제로, 소스 빌드 환경에서 권한 상승(Privilege Elevation) 공격에 노출될 수 있습니다.
*   **릴리즈 노트 URL:** 공식 릴리즈 노트는 아직 없으며, 관련 논의는 포럼을 통해 진행 중입니다.
    *   [CVE-2025-55247 관련 포럼 공지](https://forums.unrealengine.com/t/update-currently-distributed-engine-versions-to-address-cve-2025-55247-effecting-5-4-5-5-5-6/2672485)

## 3. 버그 및 이슈

**최신 버그 및 이슈 트래커 업데이트:**

Unreal Engine Issue Tracker([https://issues.unrealengine.com/](https://issues.unrealengine.com/))에서 **최근 7일간** 개발자에게 직접적으로 영향을 미치는 주요 버그의 신규 보고 또는 수정 사항은 특정되지 않았습니다.

| 구분 | 내용 |
| :--- | :--- |
| **새로 보고된 주요 버그** | 최근 7일간 새로운 업데이트 사항이 없습니다. |
| **수정된 버그** | 최근 7일간 새로운 업데이트 사항이 없습니다. |
| **Workaround (CVE-2025-55247 관련)** | 소스 빌드 사용자는 Visual Studio의 NuGet 도구를 사용하여 `Microsoft.Build` 패키지를 취약점이 해결된 버전(예: 5.5의 경우 `17.11.28`)으로 수동 업데이트해야 합니다. 자세한 절차는 포럼 공지사항을 참조하십시오. |
| **Issue Tracker URL** | [Unreal Engine Issues and Bug Tracker](https://issues.unrealengine.com/) |

## 4. GitHub 업데이트

**EpicGames/UnrealEngine 저장소 활동:**

Epic Games의 공식 GitHub 저장소([https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine))에서 **최근 7일간** 개발자에게 직접적인 영향을 미치는 주요 커밋이나 Pull Request 병합 활동은 확인되지 않았습니다.

*   **주요 커밋 및 Pull Request:** 최근 7일간 새로운 업데이트 사항이 없습니다.
*   **영향받는 시스템:** 해당 사항 없음.
*   **GitHub URL:** [EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

**Epic Staff 답변 기술 스레드:**

*   **Materials - New Features & Updates in Unreal Engine 5.7:** UE 5.7 버전의 Materials 시스템에 추가되거나 개선된 기능들을 정리한 지식 기반 문서가 공유되었습니다. 이는 곧 출시될 5.7 버전에 대한 사전 정보로 활용될 수 있습니다.
    *   **포럼 URL:** [Materials - New Features & Updates in Unreal Engine 5.7](https://forums.unrealengine.com/t/knowledge-base-materials-new-features-updates-in-unreal-engine-5-7/2673965) (게시일: 2025-11-11)
*   **CVE-2025-55247 보안 업데이트 논의:** UE 5.4, 5.5, 5.6의 보안 취약점 대응을 위한 엔진 버전 업데이트에 대한 논의가 활발히 진행되었습니다.
    *   **포럼 URL:** [update currently distributed Engine versions to address CVE-2025-55247](https://forums.unrealengine.com/t/update-currently-distributed-engine-versions-to-address-cve-2025-55247-effecting-5-4-5-5-5-6/2672485) (게시일: 2025-11-06)

## 6. 신기능 및 실험적 기능

**최신 신기능 및 실험적 기능 정보:**

*   **UE 5.7 Materials 시스템 개선:** 공식 포럼을 통해 5.7 버전에서 Materials 시스템에 대한 다양한 신기능 및 품질 개선(QoL)이 예정되어 있음이 확인되었습니다.
*   **Beta/Experimental 기능 및 주의사항:** 현재 시점에서 새로운 Beta/Experimental 기능에 대한 공식적인 발표는 없으나, 5.7 Preview 릴리즈를 통해 새로운 기능들이 공개될 예정입니다.
*   **성능 영향도:** 해당 사항 없음.

## 7. 플러그인 및 문서 업데이트

**최신 플러그인 및 문서 업데이트 정보:**

*   **공식 플러그인 업데이트:** **RealityCapture 1.4** 버전이 Epic Games Launcher 및 Epic Developer Portal을 통해 다운로드 가능하며, 새로운 가격 정책이 적용되었습니다. RealityCapture는 Epic Games가 인수한 3D 스캐닝 및 포토그라메트리 소프트웨어입니다.
    *   **출처:** [Latest Announcements topics - Epic Developer Community](https://forums.unrealengine.com/c/general/announcements/49) (게시일: 2025-11-11)
*   **문서 주요 변경사항:** 최근 7일간 Unreal Engine 공식 문서([https://dev.epicgames.com/documentation/en-us/unreal-engine](https://dev.epicgames.com/documentation/en-us/unreal-engine))의 주요 변경사항은 특정되지 않았습니다.

---
*본 보고서는 2025년 11월 11일 KST 기준 Epic Games의 공식 채널(포럼, 이슈 트래커, GitHub)에서 공개된 정보를 바탕으로 작성되었습니다.*
