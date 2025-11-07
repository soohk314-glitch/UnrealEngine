# 언리얼 엔진 데일리 브리핑 | 2025년 11월 08일

## 1. 핵심 요약

언리얼 엔진의 최신 업데이트 동향을 분석한 결과, 현재 가장 중요한 이슈는 **CVE-2025-55247** 보안 취약점에 대한 대응입니다. 공식 핫픽스 릴리즈는 아직 확인되지 않았으나, Epic Games 포럼을 통해 해당 취약점이 **UE 5.4, 5.5, 5.6** 버전에 영향을 미치며, 임시적인 **Workaround**가 공유되었습니다. 또한, **UE 5.6.1 핫픽스**가 8월 12일에 릴리즈되어 **270개 이상의 수정 사항**을 포함하고 있음이 확인되었습니다.

| 순위 | 주요 업데이트 | 즉시 확인 필요 사항 | 출처 및 게시일 (KST) |
| :--- | :--- | :--- | :--- |
| 1 | **CVE-2025-55247 보안 취약점** | UE 5.4, 5.5, 5.6 사용자는 임시 Workaround 적용 검토 | [Epic Games Forum] [1] (2025-11-07) |
| 2 | **UE 5.6.1 핫픽스 릴리즈** | MetaHuman, PCG, 렌더링 등 270개 이상 버그 수정 | [Epic Games Forum] [2] (2025-08-12) |
| 3 | **UE 5.7 버전의 SDL3 전환 예고** | UE 5.7부터 Linux 환경에서 SDL2에서 SDL3로 전환 예정. 커스터마이징 사용자 변경 필요 | [Epic Games Forum] [2] (2025-08-12) |

## 2. 공식 릴리즈 및 패치

가장 최근의 공식 패치 릴리즈는 **Unreal Engine 5.6.1 핫픽스**입니다.

- **버전 릴리즈:** Unreal Engine 5.6.1
- **주요 변경사항 및 Breaking Changes:**
    - **270개 이상의 버그 및 업데이트**가 포함되었습니다.
    - MetaHuman Character, PCG(Procedural Content Generation), 렌더링, 애니메이션 등 광범위한 영역의 안정성이 향상되었습니다.
    - **Breaking Change 예고:** UE 5.7부터 Linux 환경에서 SDL2가 SDL3로 전환될 예정입니다. SDL2 코드에 커스터마이징을 적용한 사용자는 UE 5.7로 전환 시 변경 사항을 재작업해야 합니다.
- **릴리즈 노트 URL:** 공식 릴리즈 노트는 포럼 게시글에 포함되어 있으며, 전체 수정 목록은 해당 스레드에서 확인할 수 있습니다.
    - [5.6.1 Hotfix Released - Epic Developer Community Forums] [2]

## 3. 버그 및 이슈

### 새로 보고된 주요 버그 (최근 7일간)

언리얼 엔진 이슈 트래커에서 최근 7일간 **해결(Fixed)**된 버그는 확인되지 않았습니다. 대신, **미해결(Unresolved)** 상태로 새로 보고된 주요 이슈는 다음과 같습니다.

| 이슈 ID | 요약 | 영향받는 시스템 | 보고일 (KST) |
| :--- | :--- | :--- | :--- |
| Unresolved | Landscape Splines in Partially Loaded World Partition Levels Can Cause Nanite Landscape Invalidation | Graphics Tools - Terrain, World Partition, Nanite | 2025-11-07 |
| Unresolved | net.ReplicateCustomDeltaPropertiesInRepIndexOrder is not respect the cvar for the custom properties | Networking, Replication | 2025-11-05 |
| Unresolved | [AI] Gaps between Nav Mesh tiles in World Partition map causing movement issues | AI - Navigation, World Partition | 2025-11-04 |

### 수정된 버그

- **최근 7일간 새로운 업데이트 사항이 없습니다.** 가장 최근의 수정된 버그 목록은 **UE 5.6.1 핫픽스** (2025년 8월 12일 릴리즈)에 포함되어 있습니다.

### Workaround (CVE-2025-55247)

- **이슈:** CVE-2025-55247 보안 취약점은 UE 5.4, 5.5, 5.6 버전의 `Microsoft.Build` 패키지 하드 레퍼런스 문제로 인해 발생합니다.
- **임시 Workaround:** Visual Studio의 NuGet 도구를 사용하여 `Microsoft.Build` 패키지 버전을 [https://github.com/advisories/GHSA-w3q9-fxm7-j8fq] [3] 에 명시된 안전한 버전(예: 5.5의 경우 `17.11.28`)으로 수동 업데이트하고, 필요한 경우 `.csproj` 파일의 권한을 수정해야 합니다.
- **Issue Tracker URL:** [Unreal Engine Issues and Bug Tracker] [4]

## 4. GitHub 업데이트

- **최근 7일간 새로운 업데이트 사항이 없습니다.** 언리얼 엔진의 GitHub 저장소는 주로 대규모 업데이트나 핫픽스 릴리즈 시점에 통합 커밋이 발생합니다.

## 5. 공식 포럼 기술 논의

### Epic Staff 답변 기술 스레드

가장 최근의 중요한 기술 논의는 **CVE-2025-55247** 보안 취약점 대응에 대한 스레드입니다. Epic Games 직원의 공식 답변은 아직 확인되지 않았으나, 커뮤니티에서 활발하게 Workaround가 논의되고 있습니다.

- **주요 논의:** 현재 배포된 엔진 버전(5.4, 5.5, 5.6)에 영향을 미치는 CVE-2025-55247 취약점을 해결하기 위한 업데이트 요청 및 임시 해결책 공유.
- **포럼 URL:** [update currently distributed Engine versions to address CVE-2025-55247 effecting [5.4],[5.5],[5.6]] [1]

## 6. 신기능 및 실험적 기능

- **최근 7일간 새로운 업데이트 사항이 없습니다.** 가장 최근의 주요 신기능은 **Unreal Engine 5.6** 릴리즈에 포함되어 있습니다.

| 기능명 | 상태 | 주요 내용 | 성능 영향도 |
| :--- | :--- | :--- | :--- |
| **Lumen Hardware Ray Tracing Optimizations** | 정식 | HWRT 성능 향상, 소프트웨어 레이 트레이싱 모드와 유사한 프레임 예산 달성 | 긍정적 (CPU 리소스 확보, 60hz 일관성 향상) |
| **RHI - Renderer Parallelization** | 정식 | 렌더러 스레드 병렬화 개선, 멀티스레딩 활용 극대화 | 긍정적 (렌더 스레드 병목 현상 완화) |
| **Substrate Materials** | Beta | 모듈식 셰이딩 모델 프레임워크, 레거시 시스템 대비 성능 동등성 개선 | 중립/긍정적 (성능 동등성 개선) |
| **First Person Rendering** | Beta | 1인칭 에셋의 클리핑 방지, 별도 FOV 설정 가능, VSM 및 레이 트레이싱 통합 | 중립 (특정 워크플로우에 최적화) |

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트:**
    - **MetaHuman Character** 플러그인은 UE 5.6.1 핫픽스에서 다수의 버그(MH-15569, MH-15576 등)가 수정되었습니다.
- **문서 주요 변경사항:**
    - **최근 7일간 새로운 업데이트 사항이 없습니다.** 가장 최근의 주요 문서 업데이트는 UE 5.6 릴리즈 노트에 포함된 신규 기능(Lumen HWRT 최적화, RHI 병렬화, Substrate Materials 등)에 대한 내용입니다.

***

## References

[1] [update currently distributed Engine versions to address CVE-2025-55247 effecting [5.4],[5.5],[5.6] - Epic Developer Community Forums](https://forums.unrealengine.com/t/update-currently-distributed-engine-versions-to-address-cve-2025-55247-effecting-5-4-5-5-5-6/2672485)
[2] [5.6.1 Hotfix Released - Epic Developer Community Forums](https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316)
[3] [GHSA-w3q9-fxm7-j8fq - GitHub Advisory Database](https://github.com/advisories/GHSA-w3q9-fxm7-j8fq)
[4] [Unreal Engine Issues and Bug Tracker](https://issues.unrealengine.com/)
[5] [Unreal Engine 5.6 Release Notes - Epic Developer Community](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-release-notes)
