# 언리얼 엔진 데일리 브리핑 | 2025년 11월 13일

실무 개발자를 위한 언리얼 엔진의 최신 기술 업데이트 및 이슈를 정리한 보고서입니다.

## 1. 핵심 요약

언리얼 엔진 5.7이 공식 출시(2025년 11월 12일)되면서 대규모 환경 생성 및 렌더링 기술에 큰 변화가 있었습니다. 특히 **PCG 프레임워크**와 **Substrate**가 정식 프로덕션 레디(Production-Ready)로 전환되어 즉각적인 프로젝트 도입이 가능해졌습니다.

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **PCG(Procedural Content Generation) 프레임워크** 정식 버전 출시 (대규모 환경 생성) |
| | 2. **Substrate** 머티리얼 시스템 정식 버전 출시 (고품질 레이어드 머티리얼) |
| | 3. **MegaLights** 기능 베타 전환 (동적 광원 성능 및 품질 향상) |
| **즉시 확인 필요 사항** | **C++20 기본값 변경:** 엔진의 기본 C++ 표준이 C++20으로 변경되어, 기존 C++ 코드를 사용하는 프로젝트는 컴파일 호환성 검토 및 업데이트가 필요합니다. |
| **출처 URL 및 게시일** | [Unreal Engine 5.7 is now available](https://www.unrealengine.com/en-US/news/unreal-engine-5-7-is-now-available) (2025-11-12) |

## 2. 공식 릴리즈 및 패치

### 버전 릴리즈

*   **버전 번호:** Unreal Engine 5.7
*   **릴리즈 날짜:** 2025년 11월 12일

### 주요 변경사항 및 Breaking Changes

| 카테고리 | 주요 변경사항 | Breaking Changes |
| :--- | :--- | :--- |
| **렌더링** | **Substrate** 정식 버전 출시. 레이어드 및 블렌딩 머티리얼을 위한 모듈식 프레임워크. | **C++20 기본값 변경:** 엔진의 기본 C++ 표준이 C++20으로 변경되었습니다. 이전 표준을 사용하는 프로젝트는 컴파일 오류가 발생할 수 있습니다. |
| **월드 빌딩** | **PCG 프레임워크** 정식 버전 출시. PCG GPU 컴퓨팅 성능 향상 및 PCG 에디터 모드 추가. | **Substrate 도입:** 기존 머티리얼 시스템과의 호환성 및 마이그레이션 전략 수립이 필요합니다. |
| **애니메이션** | **FBIK 및 리타겟팅 성능** 개선. **Control Rig Physics**를 위한 월드 충돌 지원. | |

### 릴리즈 노트 URL
*   [Unreal Engine 5.7 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)

## 3. 버그 및 이슈

언리얼 엔진 5.7 출시 직후이므로, 현재까지 공식 이슈 트래커에 5.7 관련 주요 버그가 대량으로 보고되지는 않았습니다. Issue Tracker에서 최근 7일간의 주요 버그 및 수정 사항을 확인했습니다.

| 구분 | 내용 |
| :--- | :--- |
| **새로 보고된 주요 버그** | **UE-353614:** (1일 전 보고) Issue Tracker에 새로운 이슈가 보고되었으나, 상세 내용은 비공개 상태입니다. |
| **수정된 버그** | **Rider 2025.3**에서 특정 예외 발생 시 언리얼 엔진 프로젝트 디버깅 중 IDE가 충돌하는 문제 수정 ([RIDER-74532](https://blog.jetbrains.com/dotnet/2025/11/11/what-s-been-fixed-in-rider-2025-3/)). |
| **Workaround** | **에디터 FPS 저하:** 에디터에서 에셋 배치 시 FPS가 5프레임 수준으로 급격히 저하되는 문제(38.10 버전 기준)가 포럼에 보고되었으며, 현재 공식적인 Workaround는 없습니다. |
| **Issue Tracker URL** | [Unreal Engine Issues and Bug Tracker](https://issues.unrealengine.com/) |

## 4. GitHub 업데이트

EpicGames/UnrealEngine GitHub 저장소에는 5.7 릴리즈와 관련된 대규모 커밋이 통합되었으며, 지속적인 개발이 이루어지고 있습니다.

| 구분 | 내용 |
| :--- | :--- |
| **주요 커밋 및 Pull Request** | 5.7 릴리즈를 위한 대규모 기능 통합 커밋이 완료되었습니다. |
| **영향받는 시스템** | 렌더링, 월드 빌딩, 애니메이션, C++ 빌드 시스템 전반 |
| **GitHub URL** | [EpicGames/UnrealEngine GitHub Repository](https://github.com/EpicGames/UnrealEngine) |

## 5. 공식 포럼 기술 논의

최근 포럼은 Unreal Engine 5.7 릴리즈와 관련된 새로운 기능 및 설치/설정 문제에 대한 논의가 활발합니다.

| 구분 | 내용 |
| :--- | :--- |
| **Epic Staff 답변 기술 스레드** | 최근 7일간 Epic Staff의 직접적인 답변이 포함된 주요 기술 스레드는 확인되지 않았습니다. |
| **주요 논의 주제** | 5.7 버전의 새로운 기능(PCG, Substrate) 사용법 및 설치/설정 관련 문제. |
| **포럼 URL** | [Epic Developer Community Forums](https://forums.unrealengine.com/) |

## 6. 신기능 및 실험적 기능

Unreal Engine 5.7에서 도입된 주요 신기능 및 실험적 기능 목록입니다.

| 구분 | 기능명 | 상태 | 주요 내용 | 성능 영향도 |
| :--- | :--- | :--- | :--- | :--- |
| **신기능** | **PCG 프레임워크** | Production-Ready | 대규모 환경의 절차적 생성. PCG GPU 컴퓨팅 성능 향상. | PCG GPU 컴퓨팅 성능 **향상** |
| | **Substrate** | Production-Ready | 물리적으로 정확한 레이어드 및 블렌딩 머티리얼. | UE5 타겟 플랫폼 전반에서 **일관된 성능** 제공 |
| **Beta 기능** | **MegaLights** | Beta | 동적 광원 수량 증가 및 성능 개선. Directional Light, Niagara Particle Lights 지원. | **성능 개선** 및 노이즈 감소 |
| | **Ease Curve** | Beta | 애니메이션 커브 UX 개선. | 미미함 |
| **실험적 기능** | **Nanite Foliage and Skinning** | Experimental | Nanite 기반의 고밀도 폴리지 렌더링 시스템. | 대규모 환경에서 **효율적인 렌더링** 기대 |
| | **SMAA** | Experimental | 새로운 안티앨리어싱 방법. | 추가적인 렌더링 비용 발생 가능 |
| | **Motion Matching Chooser Integration** | Experimental | 모션 매칭 기능 통합. | 애니메이션 시스템에 영향 |
| | **Spatially Aware Retargeting** | Experimental | 공간 인지 리타겟팅. | 애니메이션 시스템에 영향 |

## 7. 플러그인 및 문서 업데이트

### 공식 플러그인 업데이트

*   **MetaHuman Creator:** Linux 및 macOS 플랫폼 지원이 추가되었습니다.
*   **MetaHuman for Houdini:** 가이드 기반 헤어스타일 생성 워크플로우가 업데이트되었습니다.

### 문서 주요 변경사항

*   **Unreal Engine 5.7 Documentation**이 공식적으로 업데이트되었습니다.
*   **MetaHuman 5.7 Release Notes**가 게시되었습니다. (MetaHuman 5.6 릴리즈 노트에서 버그 수정 및 안정성 개선 내용 확인)
*   **문서 URL:** [Unreal Engine 5.7 Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-documentation)
