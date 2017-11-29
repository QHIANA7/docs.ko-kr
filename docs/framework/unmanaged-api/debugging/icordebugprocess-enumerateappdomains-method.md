---
title: "ICorDebugProcess::EnumerateAppDomains 메서드"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugProcess.EnumerateAppDomains
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugProcess::EnumerateAppDomains
helpviewer_keywords:
- ICorDebugProcess::EnumerateAppDomains method [.NET Framework debugging]
- EnumerateAppDomains method [.NET Framework debugging]
ms.assetid: d508981f-e2b2-445b-a649-69951c22702d
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 5233dd80750afb82a2e2a8e9675867f6decfa8f4
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugprocessenumerateappdomains-method"></a><span data-ttu-id="49179-102">ICorDebugProcess::EnumerateAppDomains 메서드</span><span class="sxs-lookup"><span data-stu-id="49179-102">ICorDebugProcess::EnumerateAppDomains Method</span></span>
<span data-ttu-id="49179-103">이 프로세스의 모든 응용 프로그램 도메인을 열거합니다.</span><span class="sxs-lookup"><span data-stu-id="49179-103">Enumerates all the application domains in this process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="49179-104">구문</span><span class="sxs-lookup"><span data-stu-id="49179-104">Syntax</span></span>  
  
```  
HRESULT EnumerateAppDomains(  
    [out] ICorDebugAppDomainEnum **ppAppDomains);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="49179-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="49179-105">Parameters</span></span>  
 `ppAppDomains`  
 <span data-ttu-id="49179-106">[out] 주소에 대 한 포인터는 [ICorDebugAppDomainEnum](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomainenum-interface.md) 이 프로세스의 응용 프로그램 도메인에 대 한 열거자입니다.</span><span class="sxs-lookup"><span data-stu-id="49179-106">[out] A pointer to the address of an [ICorDebugAppDomainEnum](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomainenum-interface.md) that is an enumerator for the application domains in this process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="49179-107">설명</span><span class="sxs-lookup"><span data-stu-id="49179-107">Remarks</span></span>  
 <span data-ttu-id="49179-108">이 메서드를 사용 하 여 하기 전에 수는 [icordebugmanagedcallback:: Createprocess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-createprocess-method.md) 콜백 합니다.</span><span class="sxs-lookup"><span data-stu-id="49179-108">This method can be used before the [ICorDebugManagedCallback::CreateProcess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-createprocess-method.md) callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="49179-109">요구 사항</span><span class="sxs-lookup"><span data-stu-id="49179-109">Requirements</span></span>  
 <span data-ttu-id="49179-110">**플랫폼:** 참조 [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="49179-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="49179-111">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="49179-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="49179-112">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="49179-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="49179-113">**.NET framework 버전:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="49179-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>