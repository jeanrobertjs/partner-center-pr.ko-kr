---
title: Azure 플랜 하에서 구독 및 리소스 관리 | 파트너 센터
ms.topic: article
ms.date: 10/04/2019
description: 구독마다 주문을 제출하지 않고 여러 Azure 구독 구입
ms.assetid: ''
author: LauraBrenner
ms.author: labrenne
ms.localizationpriority: High
ms.openlocfilehash: 5aa39cbecc7f468329c9a5234dd975c776a63ea6
ms.sourcegitcommit: dcc2a2077ef17255ecf7a2fa5fae6bbeefaa9eb0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/07/2019
ms.locfileid: "71997867"
---
# <a name="manage-subscriptions-and-resources-under-the-azure-plan"></a>Azure 플랜 하에서 구독 및 리소스 관리

고객을 Azure 플랜으로 전환하면 기본적으로 Azure에서 권한 있는 관리자 권한(대신 관리를 통한 구독 소유자 권한)이 할당됩니다.

 > [!NOTE]
 > Azure 구독에 대한 관리자 권한은 고객이 구독, 리소스 그룹 또는 워크로드 수준에서 제거할 수 있습니다. 

 파트너는 RBAC(역할 기반 액세스 제어) 기능을 통해 제공되는 다양한 옵션을 사용하여 CSP에서 고객 Azure 리소스를 연중무휴 제어하고 관리할 수 있습니다. 

- **AOBO(대신 관리)** – AOBO를 사용하면 파트너 테넌트에서 관리 에이전트 역할이 있는 사용자는 CSP 프로그램을 통해 생성되는 Azure 구독에 대한 RBAC 소유자 액세스 권한을 갖게 됩니다.

- **Azure Lighthouse**: AOBO는 여러 고객을 대상으로 작동하는 별도의 그룹을 만들거나 그룹 또는 사용자에 대해 여러 역할을 사용할 수 있는 유연성을 허용하지 않습니다. Azure Lighthouse를 사용하면 여러 그룹을 여러 고객 또는 역할에 할당할 수 있습니다. 사용자는 Azure 위임된 리소스 관리를 통해 적절한 수준의 액세스 권한을 갖게 되므로 관리 에이전트 역할이 있는(따라서 전체 AOBO 액세스 권한을 갖는) 사용자 수를 줄일 수 있습니다. 이렇게 하면 고객 리소스에 대한 불필요한 액세스를 제한하여 보안을 향상할 수 있습니다. 또한 유연성이 향상되어 여러 고객을 대규모로 관리할 수 있습니다. 자세한 내용은 [Azure Lighthouse 및 클라우드 솔루션 공급자 프로그램](https://docs.microsoft.com/azure/lighthouse/concepts/cloud-solution-provider)을 참조하세요.

-  **디렉터리 또는 게스트 사용자 또는 [서비스 사용자](https://docs.microsoft.com/azure/active-directory/develop/app-objects-and-service-principals)** : 고객 디렉터리에 사용자를 추가하거나 게스트 사용자를 추가하고 특정 RBAC 역할을 할당하여 CSP 구독에 대한 세밀한 액세스 권한을 위임할 수 있습니다. 

보안을 위해 사용자에게 작업 수행에 필요한 최소한의 권한만 부여하는 것이 좋습니다. [Azure Active Directory 권한 있는 ID 관리 리소스](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-configure)를 참조하세요. 

## <a name="link-your-partner-id-mpn-idto-your-credentials-for-managing-customers-azure-resources"></a>고객의 Azure 리소스를 관리할 수 있도록 파트너 ID(MPN ID)를 자격 증명에 연결하세요.

다음 표에서는 파트너 ID를 다양한 RBAC 액세스 옵션과 연결하는 데 사용되는 방법을 보여줍니다.

|**범주**   |**시나리오**   |**MPN ID 연결**|
|-----------------|:------------------------|:------------------|
|AOBO   |CSP 직접 파트너 또는 간접 공급자는 고객용 구독을 만들고 AOBO를 사용하여 CSP 직접 파트너 또는 간접 공급자를 구독의 기본 소유자로 만듭니다. CSP 직접 파트너 또는 간접 공급자는 AOBO를 사용하여 구독에 대한 간접 재판매인 액세스를 제공합니다.|자동(파트너 작업 필요 없음)|
|Azure Lighthouse|파트너가 [Marketplace에 새 관리형 서비스 제품](https://docs.microsoft.com/azure/lighthouse/concepts/managed-services-offers)을 만듭니다. 이 제품은 CSP 구독에서 허용되고 파트너는 CSP 구독에 대한 액세스 권한을 얻습니다.|자동(파트너 작업 필요 없음)|
|Azure Lighthouse|파트너가 Azure 구독에서 [ARM 템플릿](https://docs.microsoft.com/azure/lighthouse/how-to/onboard-customer)을 배포합니다.|파트너는 MPN ID를 파트너 테넌트의 사용자 또는 서비스 사용자에 연결해야 합니다. 자세한 내용은 [파트너 ID 연결](https://docs.microsoft.com/en-us/azure/billing/billing-partner-admin-link-started)을 참조하세요.|
|디렉터리 또는 게스트 사용자|파트너는 고객 디렉터리에 새 사용자 또는 서비스 사용자를 만들고 사용자에게 CSP 구독에 대한 액세스 권한을 부여합니다. 파트너는 고객 디렉터리에 새 사용자 또는 서비스 사용자를 만듭니다. 파트너는 사용자를 그룹에 추가하고 해당 그룹에 CSP 구독에 대한 액세스 권한을 제공합니다.|파트너는 MPN ID를 고객 테넌트의 사용자 또는 서비스 사용자에 연결해야 합니다. 자세한 내용은 [파트너 ID 연결](https://docs.microsoft.com/en-us/azure/billing/billing-partner-admin-link-started)을 참조하세요.|

## <a name="confirm-that-you-have-admin-access"></a>관리자 액세스 권한이 있는지 확인

고객이 보유한 서비스와 획득한 크레딧을 관리하려면 관리자 액세스 권한이 필요합니다. 획득한 크레딧에 대한 자세한 내용은 [파트너 획득 크레딧](partner-earned-credit.md)을 읽어 보세요. 관리자 액세스 권한이 있는지 확인하는 두 가지 방법이 있습니다.

- 일별 사용량 파일 검토 - 일일 사용량 파일 내의 단가 및 유효 단가를 검토하고 할인이 적용되는지 확인하여 관리자 액세스 권한이 있는지 확인할 수 있습니다. 할인을 받고 있다면 현재 관리자입니다.

- Azure 모니터 경고 만들기 - CSP 구독에서 RBAC 액세스가 제거될 때 알림을 받도록 Azure Monitor 활동 로그 [경고](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log)를 만들 수 있습니다.

### <a name="create-an-azure-monitor-alert"></a>Azure 모니터 경고 만들기

1. 경고를 만듭니다.

![azure 경고](images/azure/azurealert1.png)

2. 경고를 발생시킬 작업 유형을 선택합니다. 예를 들어 이메일을 원하는 것으로 지정하는 경우 역할 할당 삭제가 발생하면 알려주는 이메일을 받게 됩니다.

![경고 구성](images/azure/azureconfigurealert2.png)

### <a name="aobo-removal"></a>AOBO 제거

고객은 Azure Portal에서 **액세스 제어**로 이동하여 구독에 대한 액세스를 관리할 수 있습니다. 고객이 **역할 할당** 탭에서 **액세스 제거**를 선택합니다. 이 경우 다음과 같은 조치를 취할 수 있습니다.

- 고객에게 연락하여 관리자 액세스를 복구할 수 있는지 확인합니다.
- [RBAC(역할 기반 액세스 제어)](https://docs.microsoft.com/azure/role-based-access-control/overview)를 통해 제공되는 액세스 권한을 사용합니다.
- [Azure Lighthouse](https://azure.microsoft.com/services/azure-lighthouse/)를 통해 제공되는 액세스 권한을 사용합니다.

역할 기반 액세스는 관리자 액세스와 다릅니다. 역할은 수행할 수 있는 작업과 수행할 수 없는 작업의 범위를 정확하게 구분합니다. 관리자 액세스는 좀 더 광범위합니다.

PEC를 얻을 수 있는 역할에 대해 알아보려면 [파트너 획득 크레딧에 대한 역할 및 권한](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE3QuW2)을 읽어 보세요.

**자세한 내용**

- [파트너 획득 크레딧 - 개요](partner-earned-credit.md)

- [관리형 서비스에 대한 파트너 획득 크레딧](partner-earned-credit-explanation.md)