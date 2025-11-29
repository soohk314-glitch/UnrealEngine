# 언리얼 엔진 데일리 브리핑 | 2025년 11월 30일

## 1. 핵심 요약

- **주요 업데이트 상위 3개**
    - **Substrate 정식 출시 (Production-Ready)**: 기존 고정 셰이딩 모델을 대체하는 모듈식 물리 기반 머티리얼 프레임워크가 프로덕션 준비를 완료했습니다.
    - **PCG 프레임워크 정식 출시 (Production-Ready)**: 대규모 오픈 월드 제작을 위한 절차적 콘텐츠 생성(PCG) 프레임워크가 정식 기능으로 승격되었습니다.
    - **MegaLights 베타 업데이트**: 노이즈 감소 및 성능이 향상되었으며, Directional Light, Translucency, Hair Strands 지원이 추가되었습니다.
- **즉시 확인 필요 사항**
    - **Substrate 도입 영향**: Substrate가 기존 고정 셰이딩 모델을 대체함에 따라, 커스텀 셰이딩 모델을 사용하는 프로젝트는 호환성 및 마이그레이션 가이드를 즉시 확인해야 합니다.
    - **Control Rig 크래시 버그**: Skeletal Mesh 이름에 "skel" 접두사가 포함될 경우 Control Rig 생성 시 엔진 크래시가 발생하는 버그가 보고되었습니다. 해당 명명 규칙을 사용하는 경우 주의가 필요합니다.
- **출처 URL 및 게시일 (YYYY-MM-DD)**
    - Unreal Engine 5.7 Release Notes: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (2025-11-12)
    - Unreal Engine Issue Tracker: [https://issues.unrealengine.com/](https://issues.unrealengine.com/) (2025-11-29 기준 최신 정보)

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈 (정확한 버전 번호)**
    - **Unreal Engine 5.7** (UE 5.7)
- **주요 변경사항 및 Breaking Changes**
    - **Substrate**: 프로덕션 준비 완료. 기존 셰이딩 모델을 대체하며, Adaptive GBuffer 및 Blendable GBuffer를 지원합니다.
    - **PCG**: 프로덕션 준비 완료. 새로운 에디터 모드, 독립형 그래프, GPU 지원, UX 개선 등 대규모 월드 제작 기능이 강화되었습니다.
    - **Nanite Foliage and Skinning (Experimental)**: Nanite Assemblies를 사용한 애니메이션 폴리지 관리 및 Nanite Skinning 기능이 실험적으로 추가되었습니다.
    - **Breaking Changes**: Substrate의 도입은 기존의 커스텀 셰이딩 모델에 영향을 미치는 가장 큰 변화입니다. 릴리즈 노트의 [Migration Guide](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-migration-guide)를 확인해야 합니다.
- **릴리즈 노트 URL**
    - [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)

## 3. 버그 및 이슈

- **새로 보고된 주요 버그**
    - **Control Rig Creation Crash Triggered by “skel” Prefix**: Skeletal Mesh 이름에 "skel" 접두사 사용 시 Control Rig 생성 중 엔진 크래시 발생. (UE - Anim - Rigging - Control Rig)
    - **bake_transform_with_settings method works in 5.6 but not 5.7**: Python 스크립트의 트랜스폼 베이킹 메서드가 UE 5.7에서 작동하지 않음. (UE - Anim - Sequencer)
    - **Dataless Mutable: Cloth Simulation Not Working With Skeletal Mesh Parameter Node?**: UE 5.7의 dataless Mutable 워크플로우에서 Skeletal Mesh Parameter 노드 사용 시 Cloth Simulation이 작동하지 않음. (UE - Anim - Mutable)
- **수정된 버그**
    - **Ortho near plane clips geometry in Editor Top view**: 에디터 Top(ortho) Lit 뷰에서 줌 인/아웃 시 근접 평면 클리핑 문제 수정. (UE - Graphics Features)
    - **[Material Substitution] Missing Material IDs in exported CSV in 2025.2**: Material ID 익스포트 시 CSV 누락 문제 수정. (TM - Interoperability)
    - **CLI: using the -load command doesn't work for COLMAP files**: COLMAP 파일에 `-load` 명령 사용 시 에러 발생 문제 수정. (RS - CLI)
- **Workaround**
    - 현재 보고된 주요 버그에 대한 공식적인 Workaround는 확인되지 않았습니다.
- **Issue Tracker URL**
    - [https://issues.unrealengine.com/](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request**
    - Epic Games의 메인 Unreal Engine 저장소는 비공개 저장소이므로, 최근 7일간의 주요 커밋 및 Pull Request 정보를 직접적으로 수집할 수 없습니다.
    - 가장 최근의 공식적인 기술 업데이트는 **Unreal Engine 5.7 릴리즈**에 포함되어 있습니다.
- **영향받는 시스템**
    - 해당 없음
- **GitHub URL**
    - [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드**
    - 최근 7일간 Epic Staff가 답변한 새로운 주요 기술 논의 스레드는 확인되지 않았습니다.
    - 가장 활발한 논의는 **Unreal Engine 5.7 릴리즈** 관련 내용이며, 공식 포럼의 [Announcements](https://forums.unrealengine.com/c/announcements/10) 섹션을 참고하십시오.
- **포럼 URL**
    - [https://forums.unrealengine.com/](https://forums.unrealengine.com/)

## 6. 신기능 및 실험적 기능

- **새로 추가된 기능**
    - **Substrate**: 정식 기능으로 승격.
    - **PCG Framework**: 정식 기능으로 승격.
- **Beta/Experimental 기능 및 주의사항**
    - **MegaLights (Beta)**: 성능 및 노이즈 개선. Directional Light, Translucency, Hair Strands 지원.
    - **Nanite Foliage and Skinning (Experimental)**: Nanite를 이용한 애니메이션 폴리지 및 스키닝. 대규모 환경에서 성능 최적화에 기여할 것으로 예상되나, 실험적 기능이므로 프로덕션 사용에 주의가 필요합니다.
    - **SMAA (Experimental)**: 모바일 및 데스크톱을 위한 고품질 안티앨리어싱.
    - **Motion Matching Chooser Integration (Experimental)**: 애니메이션 워크플로우 개선.
- **성능 영향도**
    - **UE 5.7**은 전반적인 성능 향상에 중점을 두었으며, 특히 **PCG**의 GPU 지원 및 **MegaLights**의 노이즈 감소 및 성능 개선이 눈에 뜁니다. **Nanite Foliage**는 대규모 폴리지 렌더링의 성능을 혁신적으로 개선할 잠재력이 있습니다.

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트**
    - **MetaHuman Creator**: Linux 및 macOS 지원이 추가되었으며, 배치 처리 및 API 통합이 개선되었습니다.
    - **Control Rig**: 새로운 디펜던시 뷰, 성능 개선, 피직스 지원 등 기능이 업데이트되었습니다.
    - **Live Link**: 브로드캐스트, 데이터 프리뷰, 멀티 유저 지원이 확장되었습니다.
- **문서 주요 변경사항**
    - **Unreal Engine 5.7 Documentation**이 릴리즈 노트를 포함하여 전반적으로 업데이트되었습니다.
    - **Landscape Overview** 문서 등 주요 섹션의 내용이 갱신되었습니다.
