---
title: "ICorProfilerObjectEnum::Skip 메서드"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerObjectEnum.Skip
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerObjectEnum::Skip
helpviewer_keywords:
- ICorProfilerObjectEnum::Skip method [.NET Framework profiling]
- Skip method, ICorProfilerObjectEnum interface [.NET Framework profiling]
ms.assetid: f8e498f8-f93a-4b82-bd22-55bdbf5e8d45
topic_type: apiref
caps.latest.revision: "11"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 84960af6e128f3a6aa9e3b45187e282ac7228e0f
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/18/2017
---
# <a name="icorprofilerobjectenumskip-method"></a><span data-ttu-id="58056-102">ICorProfilerObjectEnum::Skip 메서드</span><span class="sxs-lookup"><span data-stu-id="58056-102">ICorProfilerObjectEnum::Skip Method</span></span>
<span data-ttu-id="58056-103">지정 된 개수의 요소를 건너뛰도록 현재 위치에서이 열거자의 커서를 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="58056-103">Advances the cursor of this enumerator from its current position so that the specified number of elements are skipped.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="58056-104">구문</span><span class="sxs-lookup"><span data-stu-id="58056-104">Syntax</span></span>  
  
```  
HRESULT Skip (  
    [in] ULONG   celt  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="58056-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="58056-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="58056-106">[in] 건너뛸 요소의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="58056-106">[in] The number of elements to be skipped.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="58056-107">설명</span><span class="sxs-lookup"><span data-stu-id="58056-107">Remarks</span></span>  
 <span data-ttu-id="58056-108">이 열거자의이 커서의 새 위치는: (현재 위치) + `celt` 합니다.</span><span class="sxs-lookup"><span data-stu-id="58056-108">The new position of this enumerator's cursor is: (current position) + `celt` .</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="58056-109">요구 사항</span><span class="sxs-lookup"><span data-stu-id="58056-109">Requirements</span></span>  
 <span data-ttu-id="58056-110">**플랫폼:** 참조 [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="58056-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="58056-111">**헤더:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="58056-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="58056-112">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="58056-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="58056-113">**.NET framework 버전:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="58056-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="58056-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="58056-114">See Also</span></span>  
 [<span data-ttu-id="58056-115">ICorProfilerObjectEnum 인터페이스</span><span class="sxs-lookup"><span data-stu-id="58056-115">ICorProfilerObjectEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerobjectenum-interface.md)