# 언리얼 엔진 데일리 브리핑 | 2025년 11월 03일

작성일: 2025년 11월 03일 (KST)

## 1. 핵심 요약

금일은 공식 안정화 버전의 패치 업데이트는 확인되지 않았으나, **Unreal Engine 5.7 Preview** 버전의 주요 기술 업데이트 내용이 확인되었습니다. 실무 개발자들은 5.7 Preview의 새로운 기능들을 미리 확인하고 프로젝트에 미칠 영향을 검토할 필요가 있습니다.

| 주요 업데이트 | 내용 | 출처 URL | 게시일 |
| :--- | :--- | :--- | :--- |
| **PCG 정식 출시 준비** | Procedural Content Generation (PCG) 프레임워크가 **Production-Ready**로 지정되었으며, 성능이 UE 5.5 대비 약 2배 향상되었습니다. | [1] | 2025-10-17 |
| **Nanite Foliage (실험적)** | Nanite Assemblies, Nanite Skinning, Nanite Voxel을 포함하는 새로운 **Nanite Foliage** 시스템이 실험적 기능으로 추가되어 고밀도 애니메이션 폴리지 렌더링을 지원합니다. | [1] | 2025-10-17 |
| **Substrate Materials 정식 출시** | 모듈형 셰이딩 시스템인 **Substrate Materials**가 베타를 벗어나 정식 출시(Production-Ready)되었습니다. | [1] | 2025-10-17 |

**즉시 확인 필요 사항:**
*   **Unreal Engine 5.7 Preview** 버전의 새로운 기능(PCG, Nanite Foliage, Substrate)이 기존 프로젝트에 미치는 영향 및 성능 변화를 테스트해야 합니다.
*   Preview 버전은 불안정할 수 있으므로, 프로덕션 프로젝트에 적용하기 전 반드시 별도의 복사본에서 테스트해야 합니다.

## 2. 공식 릴리즈 및 패치

**버전 릴리즈:**
*   **Unreal Engine 5.7 Preview** (2025년 10월 17일 공개)
*   최근 7일간 공식 안정화 버전(예: 5.4.x)의 패치 릴리즈는 확인되지 않았습니다.

**주요 변경사항 및 Breaking Changes:**
*   **PCG 성능 최적화:** GPU 및 게임 스레드 최적화를 통해 UE 5.5 대비 약 2배의 성능 향상을 달성했습니다.
*   **Substrate Materials:** 레거시 고정 셰이딩 모델을 대체하는 모듈형 시스템이 정식 출시되었습니다. **Adaptive GBuffer**와 **Blendable GBuffer**를 모두 지원하여 유연성을 높였습니다.
*   **MetaHuman Creator 플러그인:** **Linux 및 macOS** 지원이 추가되었으며, 대부분의 편집/조립 작업이 Python 및 Blueprint API를 통해 노출되었습니다.

**릴리즈 노트 URL:**
*   공식 릴리즈 노트는 Cloudflare 보안 검사 및 GitHub 로그인 문제로 직접 접근이 어려웠습니다.
*   **Unreal Engine 5.7 Preview 주요 기능 요약:** [https://digitalproduction.com/2025/10/17/unreal-5-7-preview-pcg-grows-up-foliage-gets-fancy/](https://digitalproduction.com/2025/10/17/unreal-5-7-preview-pcg-grows-up-foliage-gets-fancy/)

## 3. 버그 및 이슈

최근 7일간의 공식 버그 트래커(Issue Tracker)에서 수정된 버그 목록은 직접 접근이 어려웠습니다. 가장 최근의 버그 트래커 정보는 다음과 같습니다.

*   **Issue Tracker URL:** [https://issues.unrealengine.com/](https://issues.unrealengine.com/) (최근 3일 전 업데이트 확인)

**새로 보고된 주요 버그 (포럼 기반):**
*   **Ambiguous identifier launch error (v38.00):** 최신 업데이트(v38.00)에서 Verse 빌드 오류가 발생하며, 새로운 "result" 인터페이스와 관련된 문제로 추정됩니다. ([https://forums.unrealengine.com/t/ambiguous-identifier-launch-error/2670887](https://forums.unrealengine.com/t/ambiguous-identifier-launch-error/2670887), 21시간 전)

**Workaround:**
*   공식적인 Workaround는 확인되지 않았습니다.

## 4. GitHub 업데이트

GitHub 저장소 `EpicGames/UnrealEngine`의 커밋 기록은 로그인 문제로 직접 접근이 어려웠습니다.

*   **GitHub URL:** [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)
*   **최근 7일간 새로운 업데이트 사항이 없습니다.** (접근 불가로 인한 정보 부재)

## 5. 공식 포럼 기술 논의

공식 포럼에서 Epic Staff가 답변한 최신 기술 스레드는 직접 확인되지 않았습니다. 가장 최근의 포럼 활동은 다음과 같습니다.

*   **포럼 URL (최신 토픽):** [https://forums.unrealengine.com/latest](https://forums.unrealengine.com/latest)

**Epic Staff 답변 기술 스레드:**
*   **최근 7일간 Epic Staff 답변이 포함된 주요 기술 스레드는 확인되지 않았습니다.**

## 6. 신기능 및 실험적 기능

**새로 추가된 기능 (UE 5.7 Preview 기준):**
*   **PCG 에디터 모드:** 스플라인 드로잉, 페인트, 볼륨 툴이 추가되어 에디터 내에서 콘텐츠 생성 작업이 용이해졌습니다.
*   **애니메이션 Selection Sets:** 애니메이터가 컨트롤 그룹을 정의하고 팀 간에 공유할 수 있게 되어 작업 효율성이 향상되었습니다.

**Beta/Experimental 기능 및 주의사항 (UE 5.7 Preview 기준):**
*   **Experimental Procedural Vegetation Editor:** PCG 노드를 기반으로 하며, 에디터 내에서 Nanite-ready 폴리지를 실시간으로 생성, 조각, 변형할 수 있습니다.
*   **Experimental Nanite Foliage:** Nanite Assemblies, Nanite Skinning, Nanite Voxel의 세 가지 시스템으로 구성되어 고밀도 폴리지의 렌더링 및 애니메이션을 최적화합니다.
*   **Beta MegaLights:** 방향성 광원, Niagara 파티클 조명, 반투명 조명, 헤어 그룸을 지원하도록 기능이 확장되었습니다.
*   **주의사항:** Preview 빌드는 불안정하며, 프로젝트 복사본에서 테스트할 것을 권장합니다.

**성능 영향도:**
*   **PCG:** UE 5.5 대비 약 2배의 성능 향상 (GPU 및 게임 스레드 최적화).
*   **Nanite Foliage:** 현세대 하드웨어에서 고밀도 폴리지를 60fps로 렌더링 및 애니메이션할 수 있도록 설계되었습니다.

## 7. 플러그인 및 문서 업데이트

**공식 플러그인 업데이트:**
*   **MetaHuman Creator 플러그인:** Linux 및 macOS 지원 추가.

**문서 주요 변경사항:**
*   **최근 7일간 공식 문서의 주요 변경사항은 확인되지 않았습니다.**

---
### 참고 자료 (References)

[1] Unreal 5.7 Preview: PCG Grows Up, Foliage Gets Fancy. DIGITAL PRODUCTION. [https://digitalproduction.com/2025/10/17/unreal-5-7-preview-pcg-grows-up-foliage-gets-fancy/](https://digitalproduction.com/2025/10/17/unreal-5-7-preview-pcg-grows-up-foliage-gets-fancy/)
[2] Unreal Engine Issues and Bug Tracker. [https://issues.unrealengine.com/](https://issues.unrealengine.com/)
[3] Ambiguous identifier launch error - Issues and Bug Reporting. Epic Developer Community Forums. [https://forums.unrealengine.com/t/ambiguous-identifier-launch-error/2670887](https://forums.unrealengine.com/t/ambiguous-identifier-launch-error/2670887)
[4] EpicGames/UnrealEngine GitHub Repository. [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)
[5] Epic Developer Community Forums - Latest. [https://forums.unrealengine.com/latest](https://forums.unrealengine.com/latest)
