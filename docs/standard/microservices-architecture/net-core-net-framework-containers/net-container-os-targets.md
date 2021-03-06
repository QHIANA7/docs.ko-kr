---
title: ".NET 컨테이너와 대상에 어느 운영 체제"
description: "컨테이너 화 된.NET 응용 프로그램에 대 한.NET Microservices 아키텍처 | .NET 컨테이너와 대상에 어느 운영 체제"
keywords: "Docker, 마이크로 서비스, ASP.NET, 컨테이너"
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/18/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.openlocfilehash: 828ccb5e7a76f9419e80793b6cb3a6ba24f358cf
ms.sourcegitcommit: c2e216692ef7576a213ae16af2377cd98d1a67fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/22/2017
---
# <a name="what-os-to-target-with-net-containers"></a>.NET 컨테이너와 대상에 어느 운영 체제

Docker 및.NET Core와.NET Framework의 차이점을 지 원하는 운영 체제의 다양성을 고려할 때, 특정 OS 및 사용 하는 프레임 워크에 따라 특정 버전 대상 해야 있습니다. 

Windows, Windows Server Core 또는 Windows Nano Server를 사용할 수 있습니다. 이러한 Windows 버전 필요할 수 있는.NET Framework 또는.NET Core에서 각각 다른 특성 (Windows Server Core와 Nano Server에서 Kestrel와 같은 자체 호스트 된 웹 서버에서에서 IIS)를 제공 합니다. 

Linux 용 여러 배포판은 사용할 수 있으며 (예: Debian).NET Docker 이미지를 공식 지원 합니다.

그림 3-1에서 사용 되는.NET framework에 따라 가능한 운영 체제 버전을 볼 수 있습니다.

![](./media/image1.png)

**그림 3-1입니다.** .NET framework의 버전에 따라 대상으로 운영 체제

또한 다른 Linux 배포판을 사용 하려면 또는 Microsoft에서 제공 하지 않는 버전 이미지를 원하는 경우에서 사용자 고유의 Docker 이미지를 만들 수 있습니다. 예를 들어 기존.NET Framework 및 Docke에 대 한 not 하므로 일반적인 시나리오는 Windows Server Core에서 실행 되는 ASP.NET Core와 이미지를 만들 수 있습니다.

Dockerfile 파일을 이미지 이름을 추가 하면 운영 체제 및 버전을 사용 하면 다음 예와 같이 태그에 따라 선택할 수 있습니다.

-   microsoft /**dotnet:2.0.0-런타임-제시**

        .NET Core 2.0 runtime-only on Linux

-   microsoft /**dotnet:2.0.0-런타임-nanoserver-1709** 

        .NET Core 2.0 runtime-only on Windows Nano Server (Windows Server 2016 Fall Creators Update version 1709)

-   microsoft /**aspnetcore:2.0**
    
        .NET Core 2.0 multi-architecture: Supports Linux and Windows Nano Server depending on the Docker host.
        The aspnetcore image has a few optimizations for ASP.NET Core. 





>[!div class="step-by-step"]
[이전] (컨테이너-프레임 워크-선택-factors.md) [다음] (공식-net-docker-images.md)
