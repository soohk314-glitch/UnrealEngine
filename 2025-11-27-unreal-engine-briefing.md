# 언리얼 엔진 데일리 브리핑 | 2025년 11월 27일

실무 개발자 여러분의 효율적인 정보 습득을 위해 언리얼 엔진의 최신 기술 업데이트를 정리했습니다.

## 1. 핵심 요약

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **Substrate 재질 프레임워크** 프로덕션 준비 완료 (UE 5.7) |
| | 2. **PCG 프레임워크** 프로덕션 지원 및 신규 툴 도입 (UE 5.7) |
| | 3. **Nanite Foliage 및 Skinning** 실험적 지원 강화 (UE 5.7) |
| **즉시 확인 필요 사항** | 현재까지 공식적인 긴급 패치나 치명적인 버그 보고는 확인되지 않았습니다. 최신 버전(UE 5.7)으로의 마이그레이션을 계획 중이라면, **Substrate** 및 **PCG** 시스템의 변경 사항을 우선적으로 검토해야 합니다. |
| **출처 URL 및 게시일** | [Unreal Engine 5.7 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (게시일: 2025-11-12) |

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈:** Unreal Engine 5.7.0
- **주요 변경사항 및 Breaking Changes:**
    - **Substrate:** 기존 셰이딩 모델을 대체하는 모듈형, 물리 기반 재질 시스템이 **프로덕션 준비 완료(Production Ready)** 상태로 기본 활성화되었습니다.
    - **PCG (Procedural Content Generation):** 프레임워크가 안정화되어 프로덕션 환경에 적합하며, **PCG 에디터 모드**와 **Procedural Vegetation Editor**가 도입되었습니다.
    - **Nanite:** **Foliage 및 Skinning**에 대한 실험적 지원이 강화되어, 고성능의 애니메이션 식생 구현이 가능해졌습니다.
    - **Breaking Changes:** 5.7 마이그레이션 가이드를 통해 기존 프로젝트에 영향을 미칠 수 있는 변경 사항을 반드시 확인해야 합니다.
- **릴리즈 노트 URL:** [Unreal Engine 5.7 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)

## 3. 버그 및 이슈

- **새로 보고된 주요 버그:** 최근 7일간 공식적으로 발표된 주요 버그 보고는 확인되지 않았습니다.
- **수정된 버그:** 최근 7일간 공식적으로 발표된 수정된 버그 목록은 확인되지 않았습니다.
- **Workaround:** 최근 7일간 공식적으로 발표된 Workaround 정보는 확인되지 않았습니다.
- **Issue Tracker URL:** [Unreal Engine Issues and Bug Tracker](https://issues.unrealengine.com/) (가장 최신 정보는 해당 트래커에서 직접 확인 필요)

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request:** 최근 7일간 EpicGames/UnrealEngine 저장소의 주요 커밋 정보는 확인되지 않았습니다.
- **영향받는 시스템:** 정보 없음
- **GitHub URL:** [EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine) (가장 최신 정보는 해당 저장소에서 직접 확인 필요)

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드:** 최근 7일간 Epic Staff가 답변한 주목할 만한 기술 스레드는 확인되지 않았습니다.
- **포럼 URL:** [Unreal Engine Forums](https://forums.unrealengine.com/) (가장 최신 정보는 해당 포럼에서 직접 확인 필요)

## 6. 신기능 및 실험적 기능

- **새로 추가된 기능:**
    - **MegaLights (Beta):** 새로운 조명 시스템.
    - **Niagara Heterogeneous Volumes:** Niagara를 사용한 볼륨 렌더링 기능.
- **Beta/Experimental 기능 및 주의사항:**
    - **Nanite Foliage and Skinning (Experimental):** 실험적 기능이므로 프로덕션 적용 시 충분한 테스트가 필요합니다.
    - **SMAA (Experimental):** 새로운 안티앨리어싱 솔루션.
    - **Motion Matching Chooser Integration (Experimental):** 애니메이션 관련 실험적 기능.
- **성능 영향도:** UE 5.7 릴리즈 노트에 따르면, 전반적인 성능 개선이 이루어졌으나, 새로운 기능(Substrate, Nanite Skinning 등) 사용 시에는 프로젝트의 복잡도에 따라 성능 영향도를 개별적으로 측정해야 합니다.

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트:** 최근 7일간 공식 플러그인 업데이트 정보는 확인되지 않았습니다.
- **문서 주요 변경사항:** UE 5.7 릴리즈에 맞춰 **Substrate**, **PCG**, **Nanite** 관련 문서가 대폭 업데이트되었습니다.

***

**참고:** 본 보고서는 2025년 11월 27일 18시 15분 (KST) 기준으로 작성되었으며, 정보 수집 시점 이후의 업데이트는 포함하지 않습니다. 최신 정보는 반드시 공식 출처를 통해 확인하시기 바랍니다.
