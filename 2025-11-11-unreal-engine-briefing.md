# 언리얼 엔진 데일리 브리핑 | 2025년 11월 11일

## 1. 핵심 요약

| 순위 | 주요 업데이트 | 즉시 확인 필요 사항 | 출처 URL 및 게시일 (KST) |
| :--- | :--- | :--- | :--- |
| 1 | **CVE-2025-55247 보안 취약점 관련 엔진 버전 업데이트 논의** | UE 5.4, 5.5, 5.6 사용자는 `Microsoft.Build` 패키지 버전 수동 업데이트 필요. | [https://forums.unrealengine.com/t/update-currently-distributed-engine-versions-to-address-cve-2025-55247-effecting-5-4-5-5-5-6/2672485](https://forums.unrealengine.com/t/update-currently-distributed-engine-versions-to-address-cve-2025-55247-effecting-5-4-5-5-5-6/2672485) (2025-11-06) |
| 2 | **`r.CreateShadersOnLoad=1` 활성화 시 빌드 크래시** | 셰이더 생성 실패로 인한 크래시 발생. UE 5.5, 5.6 브랜치에서 확인됨. | [https://issues.unrealengine.com/issue/UE-Graphics-Features-Nov-10-2025](https://issues.unrealengine.com/issue/UE-Graphics-Features-Nov-10-2025) (2025-11-10) |
| 3 | **레이 트레이싱 관련 버그 수정** | `Source Length > 0`인 레이 트레이싱 라이트가 Megalights와 함께 부정확하게 동작하는 문제 수정 (2025년 3월 26일 업데이트). | [https://issues.unrealengine.com/issue/UE-Graphics-Features-Mar-26-2025](https://issues.unrealengine.com/issue/UE-Graphics-Features-Mar-26-2025) (2025-03-26) |

## 2. 공식 릴리즈 및 패치

최근 7일간 새로운 공식 릴리즈 또는 패치 노트는 확인되지 않았습니다.

**주요 변경사항 및 Breaking Changes (최신 정보)**

*   **CVE-2025-55247 보안 취약점**: UE 5.4, 5.5, 5.6 버전에서 `Microsoft.Build` 패키지 버전과 관련된 보안 취약점(CVE-2025-55247)이 보고되었습니다. Epic Games Launcher를 통해 배포된 바이너리에서 `Microsoft.Build` 패키지 버전이 하드 레퍼런스되어 있어, 사용자가 수동으로 NuGet 패키지를 업데이트해야 하는 Workaround가 포럼에 공유되었습니다. Epic Games 측의 공식 핫픽스 배포가 요청되고 있습니다.

**릴리즈 노트 URL**
*   최신 공식 릴리즈 노트는 확인되지 않았습니다.

## 3. 버그 및 이슈

**Issue Tracker URL**: [https://issues.unrealengine.com/issue/search](https://issues.unrealengine.com/issue/search)

### 새로 보고된 주요 버그 (최신 7일 이내)

| 이슈 ID | 제목 | 영향받는 시스템 | 보고일 (KST) | 상태 |
| :--- | :--- | :--- | :--- | :--- |
| UE-XXXXX | **Build crash when enabling `r.CreateShadersOnLoad=1`** | Graphics Features | 2025-11-10 | Unresolved |
| UE-XXXXX | **"Visualize Level Instance Editing" defaults to on, during sequencer playback** | Anim - Sequencer | 2025-11-07 | Won't Do |
| UE-XXXXX | **5.6 Skeletal Meshes with Disabled Sections Flicker in Ray Tracing Scene** | Graphics Features | 2025-11-07 | Unresolved |
| UE-XXXXX | **Adding a streamed empty LevelInstance in a WP level will result in an incorrect mapcheck error** | World Creation - Worldbuilding Tools | 2025-11-07 | Unresolved |

### 수정된 버그 (최신 정보)

최근 7일간 업데이트된 'Fixed' 상태의 이슈는 확인되지 않았습니다. 가장 최근에 업데이트된 'Fixed' 이슈는 다음과 같습니다.

| 이슈 ID | 제목 | 영향받는 시스템 | 업데이트일 (KST) |
| :--- | :--- | :--- | :--- |
| UE-XXXXX | **EncompassesPoint always returns false on ANavMeshBoundsVolume due to missing BodyInstance** | AI | 2025-08-03 |
| UE-XXXXX | **Raytraced lights with Source Length > 0 behave incorrectly with Megalights** | Graphics Features - Ray Tracing | 2025-03-26 |
| UE-XXXXX | **Subsurface Scattering Checkerboard with SceneColourFormat 3 (High Scalability) leads to a visual artefact when temporal upscaling is in use** | Graphics Features | 2024-09-30 |

### Workaround

*   **CVE-2025-55247 관련 Workaround**: UE 5.4, 5.5, 5.6 사용자는 Visual Studio의 NuGet 도구를 사용하여 `Microsoft.Build` 패키지 버전을 [https://github.com/advisories/GHSA-w3q9-fxm7-j8fq](https://github.com/advisories/GHSA-w3q9-fxm7-j8fq)에서 권장하는 버전(예: 5.5의 경우 `17.11.28`)으로 수동 업데이트해야 합니다.

## 4. GitHub 업데이트

최근 7일간 EpicGames/UnrealEngine GitHub 저장소의 주요 기술 커밋은 확인되지 않았습니다.

**GitHub URL**: [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

최근 7일간 Epic Staff가 답변한 주요 기술 스레드는 확인되지 않았습니다.

**포럼 URL**: [https://forums.unrealengine.com/](https://forums.unrealengine.com/)

## 6. 신기능 및 실험적 기능

최근 7일간 공식적으로 발표된 신규 기능 또는 실험적 기능 업데이트는 확인되지 않았습니다.

**성능 영향도 (최신 정보)**

*   **Unreal Engine 5.5 업데이트 성능 향상**: 일부 프로젝트에서 UE 5.5 업데이트를 통해 병렬 렌더링(parallel rendering) 도입 등으로 인해 CPU 부하가 크게 감소하고 FPS가 30-50% 향상되었다는 외부 보고가 있습니다. (출처: Gray Zone Warfare 사례)

## 7. 플러그인 및 문서 업데이트

최근 7일간 공식 플러그인 또는 문서의 주요 기술 변경사항은 확인되지 않았습니다.

**문서 주요 변경사항 (최신 정보)**

*   **UE 5.6부터 "Preview Game Language"의 "None" 옵션 제거**: UE 5.6부터 에디터 환경설정에서 "Preview Game Language"의 "None" 옵션이 제거되었습니다. (2025-10-24)
*   **MetaHuman 관련 수정**: `GeneSplicerModule`에서 `FArchiveMemoryStream` 클래스의 이중 정의로 인한 링커 오류가 수정되었습니다. (2025-10-16)
