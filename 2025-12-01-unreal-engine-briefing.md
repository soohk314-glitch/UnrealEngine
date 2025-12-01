# 언리얼 엔진 데일리 브리핑 | 2025년 12월 01일

실무 개발자를 위한 언리얼 엔진의 최신 기술 업데이트 및 이슈 정보를 정리한 일일 보고서입니다. 본 보고서는 2025년 12월 01일 한국 표준시(KST) 기준으로 작성되었습니다.

## 1. 핵심 요약

금일 브리핑의 핵심은 최근 공식 릴리즈된 **언리얼 엔진 5.7**의 주요 기능들이 프로덕션 단계에 진입했거나 실험적 기능으로 공개되었다는 점입니다. 특히 렌더링 및 애니메이션 분야에서 주목할 만한 업데이트가 다수 확인되었습니다.

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 (Top 3)** | 1. **Substrate** 머티리얼 시스템이 **프로덕션 준비 완료(Production-Ready)** 상태로 전환되었습니다. 2. **MegaLights** 기능이 **베타** 단계로 진입하며 성능 및 지원 범위가 확장되었습니다. 3. **Nanite Foliage and Skinning**이 **실험적 기능**으로 공개되어 고성능의 사실적인 식물 렌더링 경로를 제공합니다. |
| **즉시 확인 필요 사항** | UE 5.7 마이그레이션 시 **Gameplay Ability System** 관련 일부 기능에서 Deprecation Warning이 발생할 수 있습니다. 프로젝트의 입력 설정에서 `bEnabledLegacyMappingDeprecationWarnings` 옵션을 확인하십시오. |
| **출처 URL 및 게시일** | [Unreal Engine 5.7 Release Notes][1] (2025-11-12) |

## 2. 공식 릴리즈 및 패치

**버전 릴리즈:** Unreal Engine 5.7

Unreal Engine 5.7 버전이 공식 릴리즈되었습니다. 이 버전은 렌더링, 캐릭터 및 애니메이션, 월드 빌딩 등 광범위한 영역에서 개선 사항을 제공합니다.

| 구분 | 내용 |
| :--- | :--- |
| **버전 번호** | 5.7 |
| **주요 변경사항** | **Substrate**가 기본 셰이딩 모델을 대체하며 프로덕션 준비 완료 상태가 되었고, **MegaLights**가 베타로 전환되었습니다. FBIK 및 리타겟팅 성능이 약 20% 향상되었습니다. |
| **Breaking Changes** | 공식 릴리즈 노트에 별도의 'Breaking Changes' 섹션은 명시되지 않았으나, **Gameplay Ability System** 관련 일부 CVar 및 옵션에서 Deprecation Warning이 확인되었습니다. |
| **릴리즈 노트 URL** | [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes][1] |

## 3. 버그 및 이슈

Unreal Engine Issue Tracker에 보고된 최신 버그 및 수정 사항입니다. (최근 7일간의 업데이트가 명확히 표시되지 않아, 최신 정보를 포함합니다.)

### 새로 보고된 주요 버그 (Latest Bugs)

*   **Material LocalPosition node does not work correctly with Nanite Skinned meshes** (UE - Graphics Features): Nanite 스킨드 메시에서 일부 섀도우 패스에 대해 `LocalPosition` 노드가 올바르게 작동하지 않습니다.
*   **Memory leak in Landscape edit mode** (UE - Graphics Tools - Terrain - Landscape): 랜드스케이프 편집 모드에서 메모리 누수가 발생합니다.
*   **PIE also rendering in-active / unfocused editor viewport** (UE - Graphics Features): PIE(Play In Editor) 진입 후 비활성/비포커스된 에디터 뷰포트도 렌더링되어 성능이 저하됩니다.

### 수정된 버그 (Latest Fixes)

*   **Landscape weight-blended layers don't paint exclusively anymore** (UE - Graphics Tools - Terrain - Landscape): 랜드스케이프 가중치 블렌딩 레이어가 더 이상 독점적으로 페인팅되지 않는 문제가 수정되었습니다.
*   **HLOD generation can run out of space in the FName table** (UE - World Creation - Worldbuilding Tools): 대규모 WP 기반 레벨에서 HLOD 생성 시 FName 테이블 공간 부족 문제가 발생할 수 있는 문제가 수정되었습니다.

| 구분 | URL |
| :--- | :--- |
| **Issue Tracker URL** | [https://issues.unrealengine.com/][2] |

## 4. GitHub 업데이트

연결된 GitHub 저장소 `soohk314-glitch/UnrealEngine`의 최근 7일간 커밋 기록입니다. Epic Games의 공식 `EpicGames/UnrealEngine` 저장소의 주요 커밋 내용은 검색 결과에서 직접적인 기술 업데이트를 확인하지 못하여, 사용자 저장소의 활동을 대신 보고합니다.

| 커밋 해시 | 작성자 | 작성 시간 | 커밋 메시지 |
| :--- | :--- | :--- | :--- |
| `e379688` | Manus AI | 24 hours ago | Daily Briefing: 2025-12-01 |
| `d3707bb` | soohk314-glitch | 2 days ago | Daily Briefing: 2025-11-30 Unreal Engine Update |
| `05820c8` | soohk314-glitch | 3 days ago | Daily Briefing: 2025-11-28 Unreal Engine Update |
| `76841c4` | soohk314-glitch | 4 days ago | Daily Briefing: 2025-11-27 Unreal Engine Update Report |
| `474318a` | soohk314-glitch | 5 days ago | Daily Briefing: Unreal Engine 5.7 Release Notes (2025-11-27 KST) |

| 구분 | URL |
| :--- | :--- |
| **GitHub URL** | [https://github.com/soohk314-glitch/UnrealEngine][3] |

## 5. 공식 포럼 기술 논의

최근 7일간 Epic Staff가 답변한 주목할 만한 기술 스레드는 검색 결과에서 명확하게 확인되지 않았습니다. 공식 포럼에는 UE 5.7 릴리즈와 관련된 다양한 사용자 피드백 및 기술 질문이 활발하게 올라오고 있습니다.

| 구분 | URL |
| :--- | :--- |
| **포럼 URL** | [https://forums.unrealengine.com/latest][4] |

## 6. 신기능 및 실험적 기능

Unreal Engine 5.7에 포함된 주요 신기능 및 실험적 기능 목록입니다.

| 기능 | 상태 | 주요 내용 | 성능 영향도 |
| :--- | :--- | :--- | :--- |
| **Substrate** | Production-Ready | 모듈식 물리 기반 머티리얼 프레임워크. 기본 셰이딩 모델 대체. | 성능 최적화 및 유연성 향상. |
| **MegaLights** | Beta | 노이즈 감소 및 성능 개선. Directional Light, Niagara Particle Lights, Translucency, Hair Strands 지원. | 전반적인 성능 및 노이즈 감소 개선. |
| **Nanite Foliage and Skinning** | Experimental | Nanite Assemblies, Nanite Skinning, Nanite Voxels를 사용한 사실적인 식물 렌더링 경로. | 현재 세대 하드웨어에서 60fps 예산 내에서 구동 가능. |
| **SMAA** | Experimental | 모바일 및 데스크톱 렌더러를 위한 Subpixel Morphological Anti-Aliasing 지원. | 최소한의 성능 영향으로 시각적 충실도 향상. |
| **Motion Matching Chooser Integration** | Experimental | Chooser를 통해 모션 매칭 결과에 대한 제어 및 필터링 가능. | - |
| **Spatially Aware Retargeting** | Experimental | 리타겟팅 후 클린업 필요성을 줄이는 Body Interactions 및 Relative IK 오퍼레이터 추가. | - |

## 7. 플러그인 및 문서 업데이트

**MetaHuman Creator in Unreal Engine**이 이제 Linux 및 macOS에서도 사용 가능하며, Python 또는 블루프린트를 사용한 자동화 및 배치 처리를 지원합니다. 이는 MetaHuman 캐릭터 에셋을 파이프라인에 통합하는 데 큰 도움이 될 것입니다.

**Gameplay Ability System** 관련 Deprecation Warning이 확인되었으며, 이는 개발자들이 레거시 매핑에 대한 경고를 억제할 수 있는 옵션을 제공합니다.

---
### References

[1]: https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes "Unreal Engine 5.7 Release Notes"
[2]: https://issues.unrealengine.com/ "Unreal Engine Issues and Bug Tracker"
[3]: https://github.com/soohk314-glitch/UnrealEngine "soohk314-glitch/UnrealEngine"
[4]: https://forums.unrealengine.com/latest "Latest topics - Epic Developer Community Forums"
