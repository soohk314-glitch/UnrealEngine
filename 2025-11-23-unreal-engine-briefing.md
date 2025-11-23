# 언리얼 엔진 데일리 브리핑 | 2025년 11월 23일

## 1. 핵심 요약

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **Substrate** 머티리얼 시스템 정식 버전 (Production-Ready) <br> 2. **MegaLights** (Beta) 및 **Niagara Heterogeneous Volumes** (Beta) 성능 개선 <br> 3. **Nanite Foliage and Skinning** (Experimental) 추가 |
| **즉시 확인 필요 사항** | **MSVC 컴파일러 업데이트:** UE 5.7부터 기본 Microsoft Visual C++ 컴파일러가 **MSVC 14.44**로 업데이트되었습니다. 기존 프로젝트의 빌드 환경 호환성을 확인해야 합니다. |
| **출처 URL 및 게시일** | [Unreal Engine 5.7 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (2025-11-12) |

---

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈:** Unreal Engine **5.7.0** (가장 최근의 메이저 릴리즈)
- **주요 변경사항 및 Breaking Changes:**
    - **Substrate** 머티리얼 시스템이 정식 버전으로 전환되어 기본으로 활성화됩니다.
    - **MSVC 컴파일러**가 **14.44**로 업데이트되었습니다.
- **릴리즈 노트 URL:** [Unreal Engine 5.7 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)

---

## 3. 버그 및 이슈

| 구분 | 내용 | 영향받는 시스템 | 이슈 ID 및 날짜 |
| :--- | :--- | :--- | :--- |
| **수정된 버그** | 전용 서버 빌드에서 `start/end state notify events`가 매 프레임 전송될 수 있던 문제 수정 | Anim - Gameplay | Fixed (2025-08-01) |
| | `Mutable`에서 스킨드 메시가 다중 UV 채널을 가질 때 모프 기능이 작동하지 않던 문제 수정 | Anim - Mutable | Fixed (2025-10-16) |
| **새로 보고된 주요 버그** | 최근 7일간 새로운 주요 버그 보고 사항은 없습니다. | - | - |
| **Workaround** | - | - | - |
- **Issue Tracker URL:** [Unreal Engine Issues and Bug Tracker](https://issues.unrealengine.com/)

---

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request:** 최근 7일간 주요 커밋/PR 업데이트 사항은 없습니다.
- **영향받는 시스템:** -
- **GitHub URL:** [Epic Games GitHub](https://github.com/epicgames)

---

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드:** 최근 7일간 Epic Staff 답변이 달린 주요 기술 스레드 업데이트 사항은 없습니다.
- **가장 활발한 논의:** Unreal Engine 5.7 릴리즈 관련 스레드에서 신규 기능에 대한 논의가 활발합니다.
- **포럼 URL:** [Unreal Engine 5.7 Released Thread](https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913)

---

## 6. 신기능 및 실험적 기능

| 기능 | 상태 | 주요 내용 | 성능 영향도 |
| :--- | :--- | :--- | :--- |
| **MegaLights** | Beta | 노이즈 감소 및 전반적인 성능 개선. Directional Light, Niagara Particle Lights, Translucency, Hair Strands 지원 추가. | 성능 개선 |
| **Niagara Heterogeneous Volumes** | Beta | 섀도우 캐스팅 개선. Cascade shadows 및 Beer Shadow Map 지원. | 섀도우 생성 시간 및 쿼리 속도 개선 |
| **Nanite Foliage and Skinning** | Experimental | Nanite Assemblies, Nanite Skinning, Nanite Voxels를 활용하여 60fps 예산 내에서 사실적인 애니메이션 폴리지 렌더링. | 60fps 예산 내에서 구현 가능 |
| **SMAA** | Experimental | 모바일 및 데스크톱 렌더러에 Subpixel Morphological Anti-Aliasing 지원. | 최소한의 성능 영향으로 시각적 충실도 향상 |
| **Motion Matching Chooser Integration** | Experimental | Motion Matching을 Choosers에 통합하여 게임 로직 기반으로 에셋 선택 제어. | - |
| **FBIK and Retargeting** | Stable | Full Body IK 및 IK Retargeter 성능 약 20% 향상. | 성능 개선 |

---

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트:** Unreal Engine 5.7 릴리즈에 맞춰 다양한 플러그인 업데이트가 진행되었습니다. (개별 플러그인 릴리즈 노트 확인 필요)
- **문서 주요 변경사항:** Unreal Engine 5.7 문서가 업데이트되어 MegaLights, Substrate, Nanite Foliage 등 신규 기능에 대한 상세 정보가 추가되었습니다.
- **문서 URL:** [What's New | Unreal Engine 5.7 Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/whats-new)
