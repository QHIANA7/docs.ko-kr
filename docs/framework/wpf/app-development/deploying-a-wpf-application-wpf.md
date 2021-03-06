---
title: "WPF 응용 프로그램 배포(WPF)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- WPF applications [WPF], deployment
- deployment [WPF], applications
ms.assetid: 12cadca0-b32c-4064-9a56-e6a306dcc76d
caps.latest.revision: "27"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 7cf0c5383728648d46427ce8fe2f5a97a736ab00
ms.sourcegitcommit: c0dd436f6f8f44dc80dc43b07f6841a00b74b23f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/19/2018
---
# <a name="deploying-a-wpf-application-wpf"></a>WPF 응용 프로그램 배포(WPF)
[!INCLUDE[TLA#tla_wpf](../../../../includes/tlasharptla-wpf-md.md)] 응용 프로그램을 만들었으면 배포해야 합니다. [!INCLUDE[TLA#tla_mswin](../../../../includes/tlasharptla-mswin-md.md)] 및 [!INCLUDE[TLA2#tla_winfx](../../../../includes/tla2sharptla-winfx-md.md)]에서는 여러 가지 배포 기술을 제공합니다. [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] 응용 프로그램을 배포하는 데 사용되는 배포 기술은 응용 프로그램 종류에 따라 달라집니다. 이 항목에서는 각 배포 기술과 해당 기술이 각 [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] 응용 프로그램 종류의 배포 요구 사항과 함께 사용되는 방법에 대해 간략하게 설명합니다.  
  
   
<a name="Deployment_Technologies"></a>   
## <a name="deployment-technologies"></a>배포 기술  
 [!INCLUDE[TLA#tla_mswin](../../../../includes/tlasharptla-mswin-md.md)] 및 [!INCLUDE[TLA2#tla_winfx](../../../../includes/tla2sharptla-winfx-md.md)]에서는 다음을 포함하여 여러 가지 배포 기술을 제공합니다.  
  
-   XCopy 배포.  
  
-   [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)] 배포.  
  
-   [!INCLUDE[TLA#tla_clickonce](../../../../includes/tlasharptla-clickonce-md.md)] 배포.  
  
<a name="XCopy_Deployment"></a>   
### <a name="xcopy-deployment"></a>XCopy 배포  
 XCopy 배포는 XCopy 명령줄 프로그램을 사용하여 한 위치에서 다른 위치로 파일을 복사하는 방법을 나타냅니다. XCopy 배포는 다음과 같은 경우에 적합합니다.  
  
-   응용 프로그램이 독립적이며, 실행하기 위해 클라이언트를 업데이트할 필요가 없습니다.  
  
-   빌드 위치(로컬 디스크, [!INCLUDE[TLA2#tla_unc](../../../../includes/tla2sharptla-unc-md.md)] 파일 공유 등)에서 게시 위치(웹 사이트, [!INCLUDE[TLA2#tla_unc](../../../../includes/tla2sharptla-unc-md.md)] 파일 공유 등)로 이동하는 경우처럼 한 위치에서 다른 위치로 응용 프로그램 파일을 이동해야 합니다.  
  
-   응용 프로그램에 셸 통합(시작 메뉴 바로 가기, 데스크톱 아이콘 등)이 필요하지 않습니다.  
  
 XCopy는 간단한 배포 시나리오에 적합하지만 좀더 복잡한 배포 기능이 필요한 경우 제한됩니다. 특히 XCopy를 사용하면 강력한 방식으로 배포를 관리하기 위한 스크립트를 작성, 실행 및 유지 관리하는 오버헤드가 자주 발생합니다. 또한 XCopy는 버전 관리, 제거 또는 롤백을 지원하지 않습니다.  
  
<a name="Windows_Installer"></a>   
### <a name="windows-installer"></a>Windows Installer  
 [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)]를 사용하면 클라이언트에 쉽게 배포하고 실행할 수 있는 자체 포함 실행 파일로 응용 프로그램을 패키지할 수 있습니다. 또한 [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)]는 [!INCLUDE[TLA#tla_mswin](../../../../includes/tlasharptla-mswin-md.md)]와 함께 설치되며 데스크톱, 시작 메뉴 및 프로그램 제어판과의 통합을 가능하게 합니다.  
  
 [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)]에서는 응용 프로그램의 설치 및 제거가 간단하지만 설치된 응용 프로그램이 버전 관리 관점에서 최신 버전으로 유지되도록 보장하는 기능은 제공하지 않습니다.  
  
 [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)]에 대한 자세한 내용은 [Windows Installer 배포](http://msdn.microsoft.com/library/121be21b-b916-43e2-8f10-8b080516d2a0)를 참조하세요.  
  
<a name="ClickOnce_Deployment"></a>   
### <a name="clickonce-deployment"></a>ClickOnce 배포  
 [!INCLUDE[TLA2#tla_clickonce](../../../../includes/tla2sharptla-clickonce-md.md)]에서는 비 웹 응용 프로그램에 대해 웹 스타일 응용 프로그램 배포를 사용할 수 있습니다. 응용 프로그램이 웹 또는 파일 서버에서 게시되고 배포됩니다. [!INCLUDE[TLA2#tla_clickonce](../../../../includes/tla2sharptla-clickonce-md.md)]는 [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)] 설치 응용 프로그램처럼 전체 범위의 클라이언트 기능을 지원하지는 않지만 다음을 포함하는 하위 기능은 지원합니다.  
  
-   시작 메뉴 및 프로그램 제어판과의 통합.  
  
-   버전 관리, 롤백 및 제거.  
  
-   항상 배포 위치에서 응용 프로그램을 시작하는 온라인 설치 모드.  
  
-   새 버전이 릴리스되는 경우 자동 업데이트.  
  
-   파일 확장명 등록.  
  
 [!INCLUDE[TLA2#tla_clickonce](../../../../includes/tla2sharptla-clickonce-md.md)]에 대한 자세한 내용은 [ClickOnce 보안 및 배포](/visualstudio/deployment/clickonce-security-and-deployment)를 참조하세요.  
  
<a name="Deploying_WPF_Applications"></a>   
## <a name="deploying-wpf-applications"></a>WPF 응용 프로그램 배포  
 [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] 응용 프로그램에 대한 배포 옵션은 응용 프로그램 종류에 따라 달라집니다. 배포 측면에서 [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)]는 세 가지 중요한 응용 프로그램 종류를 제공합니다.  
  
-   독립 실행형 응용 프로그램.  
  
-   마크업 전용 [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] 응용 프로그램.  
  
-   [!INCLUDE[TLA#tla_xbap#plural](../../../../includes/tlasharptla-xbapsharpplural-md.md)].  
  
<a name="Deploying_Standalone_Applications"></a>   
### <a name="deploying-standalone-applications"></a>독립 실행형 응용 프로그램 배포  
 독립 실행형 응용 프로그램은 [!INCLUDE[TLA#tla_clickonce](../../../../includes/tlasharptla-clickonce-md.md)] 또는 [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)]를 사용하여 배포됩니다. 두 방법 모두 독립 실행형 응용 프로그램을 실행하려면 완전 신뢰가 필요합니다. 완전 신뢰는 [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)]를 사용하여 배포되는 독립 실행형 응용 프로그램에 자동으로 부여됩니다. [!INCLUDE[TLA2#tla_clickonce](../../../../includes/tla2sharptla-clickonce-md.md)]를 사용하여 배포되는 독립 실행형 응용 프로그램에는 완전 신뢰가 자동으로 부여되지 않습니다. 대신 [!INCLUDE[TLA2#tla_clickonce](../../../../includes/tla2sharptla-clickonce-md.md)]는 사용자가 동의해야 독립 실행형 응용 프로그램이 설치되는 보안 경고 대화 상자를 표시합니다. 동의하면 독립 실행형 응용 프로그램이 설치되고 완전 신뢰가 부여됩니다. 동의하지 않으면 독립 실행형 응용 프로그램이 설치되지 않습니다.  
  
<a name="Deploying_Markup_Only_XAML_Applications"></a>   
### <a name="deploying-markup-only-xaml-applications"></a>마크업 전용 XAML 응용 프로그램 배포  
 마크업 전용 [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] 페이지는 일반적으로 [!INCLUDE[TLA2#tla_html](../../../../includes/tla2sharptla-html-md.md)] 페이지 같은 웹 서버에 게시되며 [!INCLUDE[TLA2#tla_iegeneric](../../../../includes/tla2sharptla-iegeneric-md.md)]를 사용하여 볼 수 있습니다. 마크업 전용 [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] 페이지는 인터넷 영역 권한 설정에 정의된 제한 사항이 있는 부분 신뢰 보안 샌드박스 내에서 실행됩니다. 또한 [!INCLUDE[TLA2#tla_html](../../../../includes/tla2sharptla-html-md.md)] 기반 웹 응용 프로그램과 동일한 보안 샌드박스를 제공합니다.  
  
 [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] 응용 프로그램의 보안에 대한 자세한 내용은 [보안](../../../../docs/framework/wpf/security-wpf.md)을 참조하세요.  
  
 마크업 전용 [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] 페이지는 XCopy나 [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)]를 사용하여 로컬 파일 시스템에 설치할 수 있습니다. 이러한 페이지는 [!INCLUDE[TLA2#tla_iegeneric](../../../../includes/tla2sharptla-iegeneric-md.md)] 또는 [!INCLUDE[TLA2#tla_mswin](../../../../includes/tla2sharptla-mswin-md.md)] 탐색기를 사용하여 볼 수 있습니다.  
  
 XAML에 대한 자세한 내용은 [XAML 개요(WPF)](../../../../docs/framework/wpf/advanced/xaml-overview-wpf.md)를 참조하세요.  
  
<a name="Deploying_XAML_Browser_Applications"></a>   
### <a name="deploying-xaml-browser-applications"></a>XAML 브라우저 응용 프로그램 배포  
 [!INCLUDE[TLA2#tla_xbap#plural](../../../../includes/tla2sharptla-xbapsharpplural-md.md)]는 배포하려면 다음과 같은 파일 세 개가 필요한 컴파일된 응용 프로그램입니다.  
  
-   *ApplicationName*.exe: 실행 가능한 어셈블리 응용 프로그램 파일입니다.  
  
-   *ApplicationName*.xbap: 배포 매니페스트입니다.  
  
-   *ApplicationName*.exe.manifest: 응용 프로그램 매니페스트입니다.  
  
> [!NOTE]
>  배포 및 응용 프로그램 매니페스트에 대한 자세한 내용은 [WPF 응용 프로그램 만들기](../../../../docs/framework/wpf/app-development/building-a-wpf-application-wpf.md)를 참조하세요.  
  
 이러한 파일은 [!INCLUDE[TLA2#tla_xbap](../../../../includes/tla2sharptla-xbap-md.md)]가 빌드될 때 생성됩니다. 자세한 내용은 [방법: 새 WPF 브라우저 응용 프로그램 프로젝트 만들기](http://msdn.microsoft.com/library/72ef4d90-e163-42a1-8df0-ea7ccfd1901f)를 참조하세요. 마크업 전용 [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] 페이지처럼 [!INCLUDE[TLA2#tla_xbap#plural](../../../../includes/tla2sharptla-xbapsharpplural-md.md)]는 일반적으로 웹 서버에 게시되며 [!INCLUDE[TLA2#tla_iegeneric](../../../../includes/tla2sharptla-iegeneric-md.md)]를 사용하여 볼 수 있습니다.  
  
 [!INCLUDE[TLA2#tla_xbap#plural](../../../../includes/tla2sharptla-xbapsharpplural-md.md)]는 배포 기술 중 하나를 사용하여 클라이언트에 배포할 수 있습니다. 그러나 다음과 같은 기능을 제공하는 [!INCLUDE[TLA#tla_clickonce](../../../../includes/tlasharptla-clickonce-md.md)]가 권장됩니다.  
  
1.  새 버전이 게시될 때 자동 업데이트.  
  
2.  완전 신뢰로 실행되는 [!INCLUDE[TLA2#tla_xbap](../../../../includes/tla2sharptla-xbap-md.md)]에 대한 권한 상승.  
  
 기본적으로 ClickOnce는 .deploy 확장명을 사용하여 응용 프로그램 파일을 게시합니다. 그러면 문제가 될 수 있지만 사용하지 않도록 설정할 수 있습니다. 자세한 내용은 [ClickOnce 배포 시 서버 및 클라이언트 구성 문제](/visualstudio/deployment/server-and-client-configuration-issues-in-clickonce-deployments)를 참조하세요.  
  
 [!INCLUDE[TLA#tla_xbap#plural](../../../../includes/tlasharptla-xbapsharpplural-md.md)] 배포에 대한 자세한 내용은 [WPF XAML 브라우저 응용 프로그램 개요](../../../../docs/framework/wpf/app-development/wpf-xaml-browser-applications-overview.md)를 참조하세요.  
  
<a name="Installing__NET_Framework_3_0"></a>   
## <a name="installing-the-net-framework"></a>.NET Framework 설치  
 [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] 응용 프로그램을 실행하려면 [!INCLUDE[TLA#tla_winfx](../../../../includes/tlasharptla-winfx-md.md)]를 클라이언트에 설치해야 합니다. [!INCLUDE[TLA2#tla_ie](../../../../includes/tla2sharptla-ie-md.md)]는 [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] 브라우저에서 호스팅되는 응용 프로그램이 표시될 때 클라이언트에 [!INCLUDE[TLA2#tla_winfx](../../../../includes/tla2sharptla-winfx-md.md)]가 설치되어 있는지 자동으로 검색합니다. [!INCLUDE[TLA2#tla_winfx](../../../../includes/tla2sharptla-winfx-md.md)]가 설치되지 않은 경우 설치하라는 메시지가 [!INCLUDE[TLA2#tla_ie](../../../../includes/tla2sharptla-ie-md.md)]에 표시됩니다.  
  
 [!INCLUDE[TLA2#tla_winfx](../../../../includes/tla2sharptla-winfx-md.md)]가 설치되어 있는지 여부를 검색하기 위해 [!INCLUDE[TLA2#tla_ie](../../../../includes/tla2sharptla-ie-md.md)]에는 .xaml, .xps, .xbap 및 .application 확장명을 사용하는 콘텐츠 파일에 대한 대체(fallback) [!INCLUDE[TLA#tla_mime](../../../../includes/tlasharptla-mime-md.md)] 처리기로 등록되는 부트스트래퍼 응용 프로그램이 있습니다. 이러한 파일 형식으로 이동한 경우 [!INCLUDE[TLA2#tla_winfx](../../../../includes/tla2sharptla-winfx-md.md)]가 클라이언트에 설치되어 있지 않으면 부트스트래퍼 응용 프로그램에서 설치 권한을 요청합니다. 권한을 제공하지 않을 경우 [!INCLUDE[TLA2#tla_winfx](../../../../includes/tla2sharptla-winfx-md.md)]와 응용 프로그램이 모두 설치되지 않습니다.  
  
 권한이 부여되면 [!INCLUDE[TLA2#tla_ie](../../../../includes/tla2sharptla-ie-md.md)]에서 [!INCLUDE[TLA#tla_bits](../../../../includes/tlasharptla-bits-md.md)]를 사용하여 [!INCLUDE[TLA2#tla_winfx](../../../../includes/tla2sharptla-winfx-md.md)]를 다운로드하고 설치합니다. [!INCLUDE[TLA2#tla_winfx](../../../../includes/tla2sharptla-winfx-md.md)]를 설치하고 나면 처음에 요청한 파일이 새 브라우저 창에서 열립니다.  
  
 [!INCLUDE[TLA2#tla_winfx](../../../../includes/tla2sharptla-winfx-md.md)] 자동 검색은 [!INCLUDE[TLA2#tla_ie7](../../../../includes/tla2sharptla-ie7-md.md)] 이상이 설치된 [!INCLUDE[TLA#tla_longhorn](../../../../includes/tlasharptla-longhorn-md.md)], [!INCLUDE[TLA#tla_winxpsp2](../../../../includes/tlasharptla-winxpsp2-md.md)] 및 [!INCLUDE[TLA#tla_winnetsvrfamsp1](../../../../includes/tlasharptla-winnetsvrfamsp1-md.md)] 클라이언트에서 사용할 수 있습니다.  
  
 자세한 내용은 [.NET Framework 및 응용 프로그램 배포](../../../../docs/framework/deployment/index.md)를 참조하세요.  
  
## <a name="see-also"></a>참고 항목  
 [WPF 응용 프로그램 빌드](../../../../docs/framework/wpf/app-development/building-a-wpf-application-wpf.md)  
 [보안](../../../../docs/framework/wpf/security-wpf.md)
