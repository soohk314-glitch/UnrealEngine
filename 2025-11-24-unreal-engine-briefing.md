# 언리얼 엔진 데일리 브리핑 | 2025년 11월 24일

## 1. 핵심 요약

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **Unreal Engine 5.7 공식 릴리즈** (Nanite Foliage, Substrate 프로덕션 준비 완료) [1] [2] <br> 2. **MegaLights 베타 전환** (Directional Light, Translucency, Hair Strands 지원 추가) [2] <br> 3. **Motion Matching Chooser 통합** (Experimental) [2] |
| **즉시 확인 필요 사항** | **UE 5.7의 Substrate 머티리얼**이 프로덕션 준비 완료(Production-ready) 상태로 기본 활성화되었으며, 기존 셰이딩 모델을 대체합니다. 프로젝트 마이그레이션 시 렌더링 결과에 미치는 영향을 확인해야 합니다. [2] |
| **출처 URL 및 게시일** | Unreal Engine 5.7 Release Notes [1] [2] (게시일: 2025-11-12) |

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈:** **Unreal Engine 5.7**
- **주요 변경사항 및 Breaking Changes:**
    - **Substrate 머티리얼**이 프로덕션 준비 완료 상태로 기본 활성화되었습니다. 이는 기존의 고정된 셰이딩 모델을 대체하는 모듈식의 물리 기반 머티리얼 프레임워크입니다. [2]
    - **MegaLights**가 베타로 전환되었으며, Directional Light, Translucency, Hair Strands에 대한 지원이 추가되었습니다. [2]
    - **Niagara Heterogeneous Volumes**가 베타로 전환되었으며, 그림자 캐스팅 개선에 중점을 두었습니다. [2]
    - **Breaking Changes**에 대한 구체적인 내용은 릴리즈 노트 전문에서 확인이 필요합니다.
- **릴리즈 노트 URL:** `https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes` [2]

## 3. 버그 및 이슈

- **새로 보고된 주요 버그:**
    - **UE 5.7 UI 버그:** 일부 사용자(특히 Linux 환경)에게서 UI 상호작용 문제 및 툴팁 위치 오류가 보고되었습니다. [4]
    - **Landscape Material Paint 문제:** UE 5.7에서 랜드스케이프 레이어 블렌드 웨이트 및 페인팅 관련 문제가 포럼에 보고되었습니다. [4]
- **수정된 버그 (UE 5.7 관련 최근 수정 사항):**
    - **Swarm Agent Binaries Missing:** 5.7 Preview 런처 버전에서 Swarm 바이너리가 누락되어 라이팅 빌드가 실패하는 문제. (수정일: 2025-10-23) [3]
    - **Merge Actors (Simplify) with Substrate:** Substrate 셰이더 모델 노드를 사용할 때 Merge Actors (Simplify) 기능이 깨지는 문제. (수정일: 2025-09-29) [3]
- **Workaround:**
    - **UE 5.7 Crash on Launch:** "Unable to use default cache graph" 오류로 인한 크래시 발생 시, 오버레이(Overlay)를 비활성화하거나 관련 캐시를 삭제하는 등의 해결책이 포럼에서 논의되고 있습니다. [4]
- **Issue Tracker URL:** `https://issues.unrealengine.com/` [3]

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request:**
    - Epic Games의 GitHub 저장소는 내부 Perforce 스트림과의 병합으로 인해 대규모 커밋이 주기적으로 발생합니다. [5]
    - 최근 7일 이내의 특정 기술적 커밋 내용은 검색 결과에서 명확히 확인되지 않았습니다.
- **영향받는 시스템:**
    - GitHub를 통해 소스 코드를 직접 빌드하는 개발자는 최신 변경 사항을 반영하기 위해 `main` 브랜치를 주기적으로 업데이트해야 합니다.
- **GitHub URL:** `https://github.com/EpicGames/UnrealEngine` [5]

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드:**
    - 최근 7일 이내에 Epic Staff가 직접 답변한 새로운 기술 스레드는 검색되지 않았습니다.
    - 포럼은 주로 커뮤니티 기반의 질의응답이 활발하며, Epic Staff는 라이선스, 정책, 주요 버그 등에 대해 답변하는 경향이 있습니다. [4]
- **포럼 URL:** `https://forums.unrealengine.com/` [4]

## 6. 신기능 및 실험적 기능

- **새로 추가된 기능:**
    - **Nanite Foliage:** Nanite Assemblies, Nanite Skinning, Nanite Voxels를 통합하여 사실적이고 애니메이션 가능한 폴리지(Foliage)를 고성능으로 렌더링하는 새로운 렌더링 경로. [2]
    - **Blendshapes and Sculpting Tools:** 스켈레탈 에디터에 블렌드셰이프 생성 및 편집, 본 배치, 웨이트 페인팅 기능을 통합하여 업계 표준의 스컬프팅 워크플로우를 제공. [2]
- **Beta/Experimental 기능 및 주의사항:**
    - **Nanite Foliage and Skinning (Experimental):** 실험적 기능이므로 프로덕션 사용 시 주의가 필요합니다. [2]
    - **Motion Matching Chooser Integration (Experimental):** 모션 매칭에 Chooser를 통합하여 에셋 선택에 대한 제어 기능을 제공합니다. [2]
    - **SMAA (Experimental):** 모바일 및 데스크톱 렌더러에서 Subpixel Morphological Anti-Aliasing을 지원합니다. [2]
- **성능 영향도:**
    - **FBIK 및 Retargeting 성능 향상:** Full Body IK 및 IK Retargeter의 성능이 약 20% 향상되었습니다. [2]
    - **Nanite Foliage:** 현재 세대 하드웨어에서 60fps 예산 내에서 사실적인 폴리지를 렌더링할 수 있도록 설계되었습니다. [2]

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트:**
    - **AMD FidelityFX Super Resolution 4 (FSR 4) 플러그인**이 Unreal Engine 5.7을 지원하도록 업데이트되었습니다. [6]
- **문서 주요 변경사항:**
    - Unreal Engine 5.7 릴리즈에 맞춰 전체 문서가 업데이트되었습니다.
    - 특히 **Substrate**, **Nanite Foliage**, **MegaLights** 등 주요 신기능에 대한 상세 문서가 추가되었습니다. [2]

***

### 참고 자료 (References)

[1] Unreal Engine 5.7 is now available (2025-11-12) - `https://www.unrealengine.com/en-US/news/unreal-engine-5-7-is-now-available`
[2] Unreal Engine 5.7 Release Notes - `https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes`
[3] Unreal Engine Issues and Bug Tracker - `https://issues.unrealengine.com/`
[4] Epic Developer Community Forums - `https://forums.unrealengine.com/`
[5] EpicGames/UnrealEngine GitHub - `https://github.com/EpicGames/UnrealEngine`
[6] AMD FidelityFX Super Resolution 4 plugin updated for Unreal Engine 5.7 (2025-11-16) - `https://gpuopen.com/learn/amd-fsr4-ue5-7-update/`
