---
title: "ICorProfilerCallback::ExceptionUnwindFinallyLeave 메서드"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback.ExceptionUnwindFinallyLeave
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback::ExceptionUnwindFinallyLeave
helpviewer_keywords:
- ICorProfilerCallback::ExceptionUnwindFinallyLeave method [.NET Framework profiling]
- ExceptionUnwindFinallyLeave method [.NET Framework profiling]
ms.assetid: 2350351e-f253-4c0c-a191-f952bc5700e6
topic_type: apiref
caps.latest.revision: "12"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 969bc0723929dffd16b3119a9c9b74499f35b0e0
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/22/2017
---
# <a name="icorprofilercallbackexceptionunwindfinallyleave-method"></a>ICorProfilerCallback::ExceptionUnwindFinallyLeave 메서드
예외의 해제 단계 처리 없어진 프로파일러에 알립니다는 `finally` 절.  
  
## <a name="syntax"></a>구문  
  
```  
HRESULT ExceptionUnwindFinallyLeave();  
```  
  
## <a name="remarks"></a>설명  
 프로파일러 스택 가비지 수집을 허용 하는 상태가 아닐 수 있습니다 때문에이 호출 하는 동안 차단 하지 않아야 하 고 따라서 선점형 가비지 수집을 사용할 수 없습니다. 이때 프로파일러가 차단 및 가비지 수집을 시도 하는 경우 런타임에서이 콜백이 반환 될 때까지 차단 됩니다.  
  
 또한이 호출 하는 동안 프로파일러 호출 해서는 안 관리 코드에 또는 관리 되는 메모리 할당에서.  
  
## <a name="requirements"></a>요구 사항  
 **플랫폼:** 참조 [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)합니다.  
  
 **헤더:** CorProf.idl, CorProf.h  
  
 **라이브러리:** CorGuids.lib  
  
 **.NET framework 버전:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>참고 항목  
 [ICorProfilerCallback 인터페이스](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [ExceptionUnwindFinallyEnter 메서드](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionunwindfinallyenter-method.md)
