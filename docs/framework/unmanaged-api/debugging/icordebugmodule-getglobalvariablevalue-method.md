---
title: "ICorDebugModule::GetGlobalVariableValue 메서드"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugModule.GetGlobalVariableValue
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugModule::GetGlobalVariableValue
helpviewer_keywords:
- ICorDebugModule::GetGlobalVariableValue method [.NET Framework debugging]
- GetGlobalVariableValue method [.NET Framework debugging]
ms.assetid: bbc0881c-6a59-41a0-b5ee-2f3d1b71684c
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 00fb56353652e2fdeac7d7b42c030d9105cc9aca
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugmodulegetglobalvariablevalue-method"></a><span data-ttu-id="a8235-102">ICorDebugModule::GetGlobalVariableValue 메서드</span><span class="sxs-lookup"><span data-stu-id="a8235-102">ICorDebugModule::GetGlobalVariableValue Method</span></span>
<span data-ttu-id="a8235-103">지정 된 전역 변수의 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a8235-103">Gets the value of the specified global variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a8235-104">구문</span><span class="sxs-lookup"><span data-stu-id="a8235-104">Syntax</span></span>  
  
```  
HRESULT GetGlobalVariableValue(  
    [in]  mdFieldDef      fieldDef,  
    [out] ICorDebugValue  **ppValue  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a8235-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a8235-105">Parameters</span></span>  
 `fieldDef`  
 <span data-ttu-id="a8235-106">[in] `mdFieldDef` 전역 변수를 설명 하는 메타 데이터를 참조 하는 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="a8235-106">[in] An `mdFieldDef` token that references the metadata describing the global variable.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="a8235-107">[out] 지정 된 전역 변수의 값을 나타내는 ICorDebugValue 개체의 주소에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="a8235-107">[out] A pointer to the address of an ICorDebugValue object that represents the value of the specified global variable.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a8235-108">요구 사항</span><span class="sxs-lookup"><span data-stu-id="a8235-108">Requirements</span></span>  
 <span data-ttu-id="a8235-109">**플랫폼:** 참조 [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="a8235-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a8235-110">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a8235-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a8235-111">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a8235-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a8235-112">**.NET framework 버전:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a8235-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>