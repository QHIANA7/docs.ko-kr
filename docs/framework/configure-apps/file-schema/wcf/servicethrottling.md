---
title: '&lt;serviceThrottling&gt;'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: a337d064-1e64-4209-b4a9-db7fdb7e3eaf
caps.latest.revision: "22"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: a059684967af26c72aca48a3fa6bb10c2f26b0c5
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/22/2017
---
# <a name="ltservicethrottlinggt"></a>&lt;serviceThrottling&gt;
WCF(Windows Communication Foundation) 서비스의 스로틀 메커니즘을 지정합니다.  
  
 \<시스템입니다. ServiceModel >  
\<동작 >  
\<serviceBehaviors >  
\<동작 >  
\<serviceThrottling >  
  
## <a name="syntax"></a>구문  
  
```xml  
<serviceThrottling maxConcurrentCalls="Integer"  
    maxConcurrentInstances="Integer"  
    maxConcurrentSessions="Integer" />  
```  
  
## <a name="attributes-and-elements"></a>특성 및 요소  
 다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.  
  
### <a name="attributes"></a>특성  
  
|특성|설명|  
|---------------|-----------------|  
|maxConcurrentCalls|<xref:System.ServiceModel.ServiceHost>에서 현재 처리되는 메시지 수를 제한하는 양의 정수입니다. 제한을 초과하는 호출은 큐에 대기합니다. 이 값을 0으로 설정하는 것은 Int32.MaxValue로 설정하는 것과 같습니다. 기본값은 16 * 프로세서 수입니다.|  
|maxConcurrentInstances|<xref:System.ServiceModel.InstanceContext>에서 한 번에 실행하는 <xref:System.ServiceModel.ServiceHost> 개체 수를 제한하는 양의 정수입니다. 추가 인스턴스 생성 요청은 큐에 대기했다가 인스턴스 수가 한도 아래로 내려가면 완료됩니다. 기본값은 maxConcurrentSessions와 MaxConcurrentCalls의 합계입니다.|  
|maxConcurrentSessions|<xref:System.ServiceModel.ServiceHost> 개체에서 수락할 수 있는 세션 수를 제한하는 양의 정수입니다.<br /><br /> 서비스는 제한을 초과하는 연결을 수락하지만 제한 아래의 채널만 활성화되며 해당 채널에서 메시지를 읽습니다. 이 값을 0으로 설정하는 것은 Int32.MaxValue로 설정하는 것과 같습니다. 기본값은 100 * 프로세서 수입니다.|  
  
### <a name="child-elements"></a>자식 요소  
 없음  
  
### <a name="parent-elements"></a>부모 요소  
  
|요소|설명|  
|-------------|-----------------|  
|[\<동작 >](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|동작 요소를 지정합니다.|  
  
## <a name="remarks"></a>설명  
 스로틀은 리소스가 과도하게 사용되는 것을 방지하기 위해 동시 호출, 인스턴스 또는 세션 수를 제한합니다.  
  
 특성 값에 도달할 때마다 추적이 기록되며 첫 번째 추적이 경고로 기록됩니다.  
  
## <a name="example"></a>예  
 다음 구성 예제에서는 서비스가 최대 동시 호출 수를 2로 제한하고 최대 동시 인스턴스 수를 10으로 제한하도록 지정합니다. 이 예제를 실행 하는의 자세한 예제를 보려면 [제한](../../../../../docs/framework/wcf/samples/throttling.md)합니다.  
  
```xml  
<behaviors>   
  <serviceBehaviors>   
    <behavior name="CalculatorServiceBehavior">   
      <serviceDebug includeExceptionDetailInFaults="False" />   
      <serviceMetadata httpGetEnabled="True"/>   
      <!-- Specify throttling behavior -->  
      <serviceThrottling maxConcurrentCalls="2"   
           maxConcurrentInstances="10"/>   
    </behavior>  
  </serviceBehaviors>  
</behaviors>  
```  
  
## <a name="see-also"></a>참고 항목  
 <xref:System.ServiceModel.Description.ServiceThrottlingBehavior>  
 <xref:System.ServiceModel.Configuration.ServiceThrottlingElement>  
 [ServiceThrottlingBehavior를 사용하여 WCF 서비스 성능 제어](../../../../../docs/framework/wcf/feature-details/using-servicethrottlingbehavior-to-control-wcf-service-performance.md)
