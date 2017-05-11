---
title: ".NET Framework 클래스 라이브러리 개요 | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-standard"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - ".NET Framework 클래스 라이브러리, 정보"
  - ".NET Framework, 클래스 라이브러리"
  - "기본 형식, 클래스 라이브러리"
  - "기본 제공 형식"
  - "클래스 라이브러리[.NET Framework]"
  - "클래스 개체 값 형식"
  - "클래스[.NET Framework], 라이브러리 개요"
  - "CLS"
  - "공용 언어 사양"
  - "데이터 형식[.NET Framework]"
  - "데이터 형식[.NET Framework], C#"
  - "데이터 형식[.NET Framework], C++"
  - "데이터 형식[.NET Framework], JScript"
  - "데이터 형식[.NET Framework], Visual Basic"
  - "부동 소수점 값 형식"
  - "정수 값 형식"
  - "JScript, 데이터 형식"
  - "라이브러리, .NET Framework 클래스 라이브러리"
  - "논리 값 형식"
  - "멤버[.NET Framework], 형식"
  - "네임스페이스[.NET Framework]"
  - "네임스페이스[.NET Framework], 네임스페이스 정보"
  - "명명 규칙[.NET Framework]"
  - "System 네임스페이스"
  - "형식 시스템[.NET Framework]"
  - "형식, .NET Framework"
  - "사용자 정의 형식"
  - "값 형식"
  - "Visual Basic, 데이터 형식"
  - "Visual C#, 데이터 형식"
  - "Visual C++, 데이터 형식"
ms.assetid: 7e4c5921-955d-4b06-8709-101873acf157
caps.latest.revision: 19
author: "rpetrusha"
ms.author: "ronpet"
manager: "wpickett"
caps.handback.revision: 19
---
# .NET Framework 클래스 라이브러리 개요
[!INCLUDE[dnprdnshort](../../includes/dnprdnshort-md.md)]에는 개발 과정을 지원 및 최적화하고 시스템 기능에 대한 액세스를 제공하는 클래스, 인터페이스 및 값 형식이 포함되어 있습니다.  언어 간의 원활한 상호 운용성을 위해 대부분의 .NET Framework 형식은 CLS\(공용 언어 사양\) 규격을 따르므로 CLS 규격 컴파일러를 사용하는 모든 프로그래밍 언어에서 사용될 수 있습니다.  
  
 .NET Framework 형식은 .NET 응용 프로그램, 구성 요소 및 컨트롤 빌드의 기초가 됩니다.  [!INCLUDE[dnprdnshort](../../includes/dnprdnshort-md.md)]에는 다음과 같은 기능을 수행하는 형식이 포함되어 있습니다.  
  
-   기본 데이터 형식 및 예외를 나타냅니다.  
  
-   데이터 구조를 캡슐화합니다.  
  
-   I\/O를 수행합니다.  
  
-   로드된 형식에 대한 정보에 액세스합니다.  
  
-   .NET Framework 보안 검사를 호출합니다.  
  
-   데이터 액세스, 리치 클라이언트 쪽 GUI, 서버에서 제어 가능한 클라이언트 쪽 GUI를 제공합니다.  
  
 [!INCLUDE[dnprdnshort](../../includes/dnprdnshort-md.md)]에서는 강력한 인터페이스 집합뿐만 아니라 추상 및 구체\(비추상\) 클래스도 제공합니다.  구체 클래스를 있는 그대로 사용할 수도 있고 여러 가지 경우에 구체 클래스에서 직접 클래스를 파생시켜 사용할 수도 있습니다.  인터페이스의 기능을 사용하려면 해당 인터페이스를 구현하는 클래스를 만들거나 해당 인터페이스를 구현하는 .NET Framework 클래스 중 하나에서 클래스를 파생시킵니다.  
  
## 명명 규칙  
 .NET Framework 형식에서는 계층 구조를 의미하는 스키마의 이름을 지정하는데 점 구문를 사용합니다.  이 방법을 사용하면 관련 형식을 네임스페이스로 그룹화하여 보다 쉽게 검색하고 참조할 수 있습니다.  전체 이름에서 첫 번째 부분\(가장 오른쪽 점의 오른쪽 부분\)은 해당 네임스페이스의 이름이고,  마지막 부분은 형식 이름입니다.  예를 들어, **System.Collections.ArrayList**는 **System.Collections** 네임스페이스에 속하는 **ArrayList** 형식을 나타냅니다.  **System.Collections**의 형식은 개체의 컬렉션을 조작하는 데 사용할 수 있습니다.  
  
 이 이름 지정 체계를 사용하면 [!INCLUDE[dnprdnshort](../../includes/dnprdnshort-md.md)]를 확장하는 라이브러리 개발자가 손쉽게 계층 구조의 그룹 형식을 만들고 일관되고 이해하기 쉬운 이름을 그룹에 지정할 수 있습니다.  또한 형식을 전체 이름, 즉 네임스페이스와 형식 이름별로 명확하게 식별할 수 있으므로 형식 이름 간의 충돌을 방지할 수 있습니다.  라이브러리 개발자는 다음과 같은 규칙을 사용하여 네임스페이스의 이름을 만듭니다.  
  
 *CompanyName*.*TechnologyName*  
  
 예를 들어, Microsoft.Word라는 네임스페이스는 이 형식을 사용한 것입니다.  
  
 명명 패턴을 사용하여 관련 형식을 네임스페이스로 그룹화하면 효과적으로 클래스 라이브러리를 빌드하고 문서화할 수 있습니다.  하지만 이 명명 스키마는 표시 여부, 멤버 액세스, 상속성, 보안 또는 바인딩에는 영향을 주지 않습니다.  하나의 네임스페이스가 여러 어셈블리에 분할될 수 있으며 하나의 어셈블리에 여러 네임스페이스의 형식이 포함될 수 있습니다.  어셈블리는 공용 언어 런타임에서 버전 관리, 배포, 보안, 로딩 및 표시 여부에 대한 형식적 구조를 제공합니다.  
  
 네임스페이스 및 형식 이름에 대한 자세한 내용은 [공용 형식 시스템](../../docs/standard/base-types/common-type-system.md)을 참조 하십시오.  
  
## System 네임스페이스  
 <xref:System> 네임스페이스는 [!INCLUDE[dnprdnshort](../../includes/dnprdnshort-md.md)]의 기본 형식에 대한 루트 네임스페이스입니다.  이 네임스페이스에는 모든 응용 프로그램에서 사용하는 <xref:System.Object>\(상속 계층 구조의 루트\), <xref:System.Byte>, <xref:System.Char>, <xref:System.Array>, <xref:System.Int32>, <xref:System.String> 등의 기본 데이터 형식을 나타내는 클래스가 포함됩니다.  이 형식의 대부분은 프로그래밍 언어에서 사용하는 기본 데이터 형식에 해당합니다.  .NET Framework 형식을 사용하여 코드를 작성할 때 .NET Framework의 기본 데이터 형식이 필요하면 사용 중인 프로그래밍 언어의 해당 키워드를 사용할 수 있습니다.  
  
 다음 표에서는 [!INCLUDE[dnprdnshort](../../includes/dnprdnshort-md.md)]에서 제공하는 기본 형식 목록을 보여 주며 각 형식에 대해 간단히 설명한 다음 Visual Basic, C\#, C\+\+ 및 JScript의 해당 형식을 나타냅니다.  
  
|범주|클래스 이름|설명|Visual Basic 데이터 형식|C\# 데이터 형식|C\+\+ 데이터 형식|JScript 데이터 형식|  
|--------|------------|--------|-------------------------|----------------|------------------|--------------------|  
|정수|<xref:System.Byte>|8비트 부호 없는 정수입니다.|**Byte**|**byte**|**unsigned char**|**Byte**|  
||<xref:System.SByte>|8비트 부호 있는 정수입니다.<br /><br /> CLS 규격을 따르지 않음|**SByte**|**sbyte**|**char**<br /><br /> 또는<br /><br /> **signed** **char**|**SByte**|  
||<xref:System.Int16>|16비트 부호 있는 정수입니다.|**Short**|**short**|**short**|**short**|  
||<xref:System.Int32>|32비트 부호 있는 정수입니다.|**정수**|**int**|**int**<br /><br /> 또는<br /><br /> **long**|**int**|  
||<xref:System.Int64>|64비트 부호 있는 정수입니다.|**Long**|**long**|**\_\_int64**|**long**|  
||<xref:System.UInt16>|16비트 부호 없는 정수입니다.<br /><br /> CLS 규격을 따르지 않음|**UShort**|**ushort**|**unsigned short**|**UInt16**|  
||<xref:System.UInt32>|32비트 부호 없는 정수입니다.<br /><br /> CLS 규격을 따르지 않음|**UInteger**|**uint**|**unsigned int**<br /><br /> 또는<br /><br /> **unsigned long**|**UInt32**|  
||<xref:System.UInt64>|64비트 부호 없는 정수입니다.<br /><br /> CLS 규격을 따르지 않음|**ULong**|**ulong**|**unsigned \_\_int64**|**UInt64**|  
|부동 소수점|<xref:System.Single>|단정밀도\(32비트\) 부동 소수점 숫자|**Single**|**float**|**float**|**float**|  
||<xref:System.Double>|배정밀도\(64비트\) 부동 소수점 숫자|**Double**|**double**|**double**|**double**|  
|논리|<xref:System.Boolean>|부울 값\(true 또는 false\)|**Boolean**|**bool**|**bool**|**bool**|  
|기타|<xref:System.Char>|유니코드\(16비트\) 문자|**Char**|**char**|**wchar\_t**|**char**|  
||<xref:System.Decimal>|10진수\(128비트\) 값|**10진수**|**decimal**|**10진수**|**10진수**|  
||<xref:System.IntPtr>|내부 플랫폼에 따라 크기가 결정되는 부호 있는 정수\(32비트 플랫폼에서는 32비트 값이고 64비트 플랫폼에서는 64비트 값임\)|**IntPtr**<br /><br /> 기본 제공 형식이 아님|**IntPtr**<br /><br /> 기본 제공 형식이 아님|**IntPtr**<br /><br /> 기본 제공 형식이 아님|**IntPtr**|  
||<xref:System.UIntPtr>|내부 플랫폼에 따라 크기가 결정되는 부호 없는 정수\(32비트 플랫폼에서는 32비트 값이고 64비트 플랫폼에서는 64비트 값임\)<br /><br /> CLS 규격을 따르지 않음|**UIntPtr**<br /><br /> 기본 제공 형식이 아님|**UIntPtr**<br /><br /> 기본 제공 형식이 아님|**UIntPtr**<br /><br /> 기본 제공 형식이 아님|**UIntPtr**|  
|클래스 개체|<xref:System.Object>|개체 계층 구조의 루트|**Object**|**object**|**Object\***|**Object**|  
||<xref:System.String>|유니코드 문자로 구성된 변경할 수 없는 고정 길이의 문자열|**String**|**string**|**String\***|**String**|  
  
 <xref:System> 네임스페이스에는 기본 데이터 형식 외에도 예외를 처리하는 클래스에서 응용 프로그램 도메인 및 가비지 수집기 등의 핵심 런타임 개념을 다루는 클래스에 이르는 100개 이상의 클래스가 들어 있습니다.  또한 <xref:System> 네임스페이스에는 2차 네임스페이스도 많이 들어 있습니다.  
  
 네임스페이스에 대한 자세한 내용은 [.NET Framework 클래스 라이브러리](http://go.microsoft.com/fwlink/?LinkID=227195)를 참조하십시오.  이 참조 문서에서는 각 네임스페이스에 대한 간단한 개요와 각 형식 및 해당 멤버에 대한 형식 설명을 볼 수 있습니다.  
  
## 참고 항목  
 [공용 형식 시스템](../../docs/standard/base-types/common-type-system.md)   
 [.NET Framework 클래스 라이브러리](http://go.microsoft.com/fwlink/?LinkID=227195)   
 [개요](../../docs/framework/get-started/overview.md)