---
title: 사용자 역할 및 권한 할당 | 파트너 센터
ms.topic: article
ms.date: 10/10/2019
description: 파트너 센터에서 작업을 해야 하는 모든 직원에게 역할을 할당해야 합니다.
author: LauraBrenner
ms.author: labrenne
keywords: 역할, 권한, 관리자, 에이전트
ms.localizationpriority: high
ms.openlocfilehash: 0bbc9af84b8a1464f255c17147fdc10a7504eb43
ms.sourcegitcommit: 1ccc27092949deb6f6404e64fd6a628fd7b5fd5c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/11/2019
ms.locfileid: "72276094"
---
# <a name="assign-users-roles-and-permissions"></a>사용자 역할 및 권한 할당


법적 이름과 주소, 지원 세부 정보, 면세 정보, 은행 정보, 회사의 기본 연락처를 비롯한 파트너 프로필을 설정했습니다. 다음 단계: 사용자가 파트너 센터에서 작업을 시작할 수 있도록 암호와 역할을 사용하여 사용자를 설정합니다.

## <a name="set-up-your-employees-to-work-in-partner-center"></a>파트너 센터에서 작업할 수 있도록 직원 설정

사용자에게 부여할 파트너 센터에 대한 액세스 유형을 역할 및 권한을 기준으로 결정합니다. 역할은 비즈니스가 개입된 프로그램과 관련이 있습니다. 예를 들어 비즈니스가 CSP(클라우드 솔루션 공급자) 비즈니스인 경우 글로벌 관리자 같은 표준 Azure AD 테넌트 관리 역할을 갖게 되겠지만, CSP 프로그램과 관련된 역할도 필요합니다. 프로그램마다 특정 역할이 있습니다.

>[!Note]
> AAD(Azure Active Directory) 테넌트 역할에는 글로벌 관리자, 사용자 관리자 및 CSP 역할이 포함됩니다. 비 AAD 역할은 테넌트를 관리하지 않는 역할이며, 여기에는 MPN 관리자, 비즈니스 프로필 관리자, 조회 관리자, 인센티브 관리자 및 인센티브 사용자가 포함됩니다. 

### <a name="manage-commercial-transactions-in-partner-center-azure-ad-and-csp-roles"></a>파트너 센터에서 상업 트랜잭션 관리(Azure AD 및 CSP 역할)

|**역할**|**수행할 수 있는 작업**|
|----------------------------------|:---------------------------------|
|전역 관리자|• 전체 권한으로 모든 Microsoft 계정/서비스에 액세스할 수 있음
|      |• 파트너 센터에 대한 지원 티켓 만들기
||• 계약, 가격표 및 제품 보기
||• 파트너 사용자 보기, 만들기 및 관리|
||  청구 정보, 청구서 및 조정 파일 보기, 만들기 및 관리
|사용자 관리 관리자   | • 사용자 보기, 만들기 및 관리
||• 모든 파트너 프로필 보기
||• 파트너 사용자 보기, 만들기 및 관리  |
|청구 관리자 | - 청구 정보, 청구서 및 조정 파일 보기, 만들기 및 관리|
|기본 사용자|  내 프로필 보기   |
|관리자 에이전트 | • 고객 관리
||• 파트너 센터에 디바이스 목록 추가
||• 프로필을 만들고 디바이스에 적용
||• 구독 관리
||• 고객의 서비스 상태 및 서비스 요청
||• 위임된 관리자 권한 요청
||• 가격 및 제품 보기
||• 청구
||• 고객을 대신하여 관리
||• 부가 가치 재판매인 등록|
|영업 에이전트 | • 고객 관리
||• 파트너 센터에 디바이스 목록 추가
||• 구독 관리
||• 지원 티켓 보기
||• 고객과의 관계 요청
||• 잠재 고객 관리
||• 고객 계약 보기
||• 부가 가치 재판매인 등록|
|기술 지원팀 에이전트| • 고객 검색 및 보기
||• 고객 세부 정보 편집
||• 청구 또는 구독 관리와 관련된 고객 문제 해결 지원
||• 고객을 대신하여 지원 요청(참고: Office 365 구독에 대해 이 작업을 완료하려면 관리 에이전트여야 함)
||• 고객을 대신하여 구독 및 청구 이슈 관리(참고: Office 365 구독에 대해 이 작업을 완료하려면 관리 에이전트여야 함)|

### <a name="control-panel-vendor-cpv-csp-role-and-non-aad-role"></a>CPV(제어판 공급업체). (CSP 역할 및 비 AAD 역할)
CPV는 CSP(클라우드 솔루션 공급자) 파트너가 사용하는 앱을 개발하여 해당 시스템을 파트너 센터 API와 통합할 수 있게 해줍니다. 

|**역할**   |**수행 가능한 작업**|
|------------------------------|:----------------------------|
|전역 관리자| CPV 프로필을 보고 관리합니다.|
||CPV 기능에 액세스해야 하는 사용자를 보고 관리합니다.|

### <a name="guest-user-must-be-added-to-the-aad-tenant"></a>게스트 사용자(AAD 테넌트에 추가해야 함)

|**게스트 사용자**   | **역할**|
|---------------------------|:--------------------|
||MPN 파트너 관리자|
||계정 관리자|
||인센티브 관리자|
||비즈니스 프로필 관리자|
||조회 관리자|


## <a name="manage-mpn-membership-and-your-company-non-aad-roles-these-roles-manage-the-company-business-rather-than-the-tenant"></a>MPN 멤버 자격과 회사 관리(비 AAD 역할: 이 역할은 테넌트가 아닌 회사 비즈니스를 관리)

|**역할** | **수행 가능한 작업**|
|----------------------------|:----------------------------|
|MPN 파트너 관리자|• 파트너 서비스 요청 보기, 만들기 및 관리||
||• 법률, 회사, 비즈니스 및 MPN 프로필 보기
||• 사용자 정보 및 해당 기술 데이터 보기
||• 역량 보기
||• 혜택 보기 및 관리
||• MPN 제품 보기 및 구매
||• MPN 제품 주문 기록 및 청구서 보기
||• 파트너 기여 지표 데이터 보기
||• 바우처 유효성 검사 도구에서 작업 가능|
||- 고객 데이터 분석 정보 보기
|| 회사 내 다른 사용자 역할을 볼 수 있지만 역할을 할당할 수는 없음
|계정 관리자| 위치 추가
|| 관리자로 있는 계정과 관련된 프로필 관리 
||• 테넌트의 사용자에 대한 역할을 비 AAD 역할에 할당 
||• 프로그램에 위치 등록


## <a name="manage-referrals"></a>조회 관리 

|**역할**|**수행 가능한 작업**|
|-----------------------------|:------------------------|
|조회 관리자       |• 비즈니스 프로필 보기, 만들기 및 관리
||• 조회 받기 및 관리
||• 공동 판매 조회 보기, 만들기 및 관리|
||• 파트너 서비스 요청 보기, 만들기 및 관리
|비즈니스 프로필 관리자   |• 비즈니스 프로필 보기, 만들기 및 관리 
||• 파트너 서비스 요청 보기, 만들기 및 관리|

## <a name="manage-incentives"></a>인센티브 관리 

|**역할** | **수행 가능한 작업**|
|------------------------------|:-------------------------|
|인센티브 관리자|• 인센티브 시작 및 관리 
||• 인센티브 프로그램의 모든 측면을 보고 편집할 수 있음
||• 은행 및 세금 정보를 살펴보고 편집할 수 있음
||• 리베이트 및 협력 수익 보기
||• 액세스 지원
||• 분쟁 인센티브 결제|
|인센티브 사용자|• 인센티브 프로그램을 볼 수 있음
||• 인센티브 클레임을 보고 시작할 수 있음
||• 리베이트 및 협력 수익 보기
||• 액세스 지원












