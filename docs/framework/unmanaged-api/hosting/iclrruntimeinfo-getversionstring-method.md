---
title: "ICLRRuntimeInfo::GetVersionString 메서드"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRRuntimeInfo.GetVersionString
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRRuntimeInfo::GetVersionString
helpviewer_keywords:
- ICLRRuntimeInfo::GetVersionString method [.NET Framework hosting]
- GetVersionString method, ICLRRuntimeInfo interface [.NET Framework hosting]
ms.assetid: 98b097ef-2276-4dd9-8551-b03c972e8179
topic_type: apiref
caps.latest.revision: "16"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 170b144c642463f6030e033cb5f5aaaf9755d4e2
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/21/2017
---
# <a name="iclrruntimeinfogetversionstring-method"></a><span data-ttu-id="e7c45-102">ICLRRuntimeInfo::GetVersionString 메서드</span><span class="sxs-lookup"><span data-stu-id="e7c45-102">ICLRRuntimeInfo::GetVersionString Method</span></span>
<span data-ttu-id="e7c45-103">와 연결 된 공용 언어 런타임 (CLR) 버전 정보를 가져옵니다는 주어진 [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c45-103">Gets common language runtime (CLR) version information associated with a given [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface.</span></span>  
  
 <span data-ttu-id="e7c45-104">이 메서드는 다음과 같은 기능을 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c45-104">This method supersedes the following functions:</span></span>  
  
-   [<span data-ttu-id="e7c45-105">GetRequestedRuntimeInfo</span><span class="sxs-lookup"><span data-stu-id="e7c45-105">GetRequestedRuntimeInfo</span></span>](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeinfo-function.md)  
  
-   [<span data-ttu-id="e7c45-106">GetRequestedRuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="e7c45-106">GetRequestedRuntimeVersion</span></span>](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeversion-function.md)  
  
## <a name="syntax"></a><span data-ttu-id="e7c45-107">구문</span><span class="sxs-lookup"><span data-stu-id="e7c45-107">Syntax</span></span>  
  
```  
HRESULT GetVersionString(  
    [out, size_is(*pcchBuffer)] LPWSTR pwzBuffer,  
    [in, out]  DWORD *pcchBuffer);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e7c45-108">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e7c45-108">Parameters</span></span>  
 `pwzBuffer`  
 <span data-ttu-id="e7c45-109">[out] .NET Framework 컴파일 버전 형식에서 "v*A*. *B*[. *X*] "입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c45-109">[out] The .NET Framework compilation version in the format "v*A*.*B*[.*X*]".</span></span> <span data-ttu-id="e7c45-110">*A*, *B*, 및 *X* 는 주 버전, 부 버전 및 빌드 번호에 해당 하는 10 진수입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c45-110">*A*, *B*, and *X* are decimal numbers that correspond to the major version, the minor version, and the build number.</span></span> <span data-ttu-id="e7c45-111">*X* 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c45-111">*X* is optional.</span></span> <span data-ttu-id="e7c45-112">경우 *X* 은 없으며, 기간은 없습니다 후행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c45-112">If *X* is not present, there is no trailing period.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e7c45-113">이 매개 변수 C:\Windows\Microsoft.NET\Framework 아래 표시 된 대로.NET Framework 버전에 대 한 디렉터리 이름을 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c45-113">This parameter must match the directory name for the .NET Framework version, as it appears under C:\Windows\Microsoft.NET\Framework.</span></span>  
  
 <span data-ttu-id="e7c45-114">예제 값은 "v1.0.3705", "v1.1.4322", "v2.0.50727" 및 "v4.0 합니다. *x*"여기서 *x* 설치 된 빌드 번호에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="e7c45-114">Example values are "v1.0.3705", "v1.1.4322", "v2.0.50727", and "v4.0.*x*", where *x* depends on the build number installed.</span></span> <span data-ttu-id="e7c45-115">"V" 접두사는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c45-115">Note that the "v" prefix is mandatory.</span></span>  
  
 `pchBuffer`  
 <span data-ttu-id="e7c45-116">[out에서] 크기를 지정 `pwzBuffer` 버퍼 오버런을 방지 하기.</span><span class="sxs-lookup"><span data-stu-id="e7c45-116">[in, out] Specifies the size of `pwzBuffer` to avoid buffer overruns.</span></span> <span data-ttu-id="e7c45-117">경우 `pwzBuffer` 은 `null`, `pchBuffer` 필요한 크기의 반환 `pwzBuffer` 사전 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c45-117">If `pwzBuffer` is `null`, `pchBuffer` returns the required size of `pwzBuffer` to allow preallocation.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e7c45-118">반환 값</span><span class="sxs-lookup"><span data-stu-id="e7c45-118">Return Value</span></span>  
 <span data-ttu-id="e7c45-119">이 메서드는 다음과 같은 특정 HRESULT뿐만 아니라 메서드 오류를 나타내는 HRESULT 오류도 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c45-119">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="e7c45-120">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e7c45-120">HRESULT</span></span>|<span data-ttu-id="e7c45-121">설명</span><span class="sxs-lookup"><span data-stu-id="e7c45-121">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="e7c45-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="e7c45-122">S_OK</span></span>|<span data-ttu-id="e7c45-123">메서드가 완료되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c45-123">The method completed successfully.</span></span>|  
|<span data-ttu-id="e7c45-124">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="e7c45-124">E_POINTER</span></span>|<span data-ttu-id="e7c45-125">`pwzBuffer` 또는 `pchBuffer`이 null입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c45-125">`pwzBuffer` or `pchBuffer` is null.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e7c45-126">요구 사항</span><span class="sxs-lookup"><span data-stu-id="e7c45-126">Requirements</span></span>  
 <span data-ttu-id="e7c45-127">**플랫폼:** 참조 [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c45-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e7c45-128">**헤더:** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="e7c45-128">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="e7c45-129">**라이브러리:** MSCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="e7c45-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e7c45-130">**.NET framework 버전:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e7c45-130">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e7c45-131">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e7c45-131">See Also</span></span>  
 [<span data-ttu-id="e7c45-132">ICLRRuntimeInfo 인터페이스</span><span class="sxs-lookup"><span data-stu-id="e7c45-132">ICLRRuntimeInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)  
 [<span data-ttu-id="e7c45-133">호스팅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="e7c45-133">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)  
 [<span data-ttu-id="e7c45-134">4 및 4.5.NET Framework에 추가 된 CLR 호스팅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="e7c45-134">CLR Hosting Interfaces Added in the .NET Framework 4 and 4.5</span></span>](../../../../docs/framework/unmanaged-api/hosting/clr-hosting-interfaces-added-in-the-net-framework-4-and-4-5.md)  
 [<span data-ttu-id="e7c45-135">호스팅</span><span class="sxs-lookup"><span data-stu-id="e7c45-135">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)