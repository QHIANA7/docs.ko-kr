---
title: "인덱싱된 속성(F#)"
description: "F # 인덱싱된 속성을 속성 정렬 된 데이터에 대 한 배열 유사 액세스를 제공 하는 방법을 알아봅니다."
keywords: "visual f#, f#, 함수형 프로그래밍"
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: f1266b8b-e2e3-4f49-9332-65c6d34dc0f3
ms.openlocfilehash: 78a09a70621e82f073346471e68ec826359641d6
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/18/2017
---
# <a name="indexed-properties"></a>인덱싱된 속성

*인덱싱된 속성* 속성에 대 한 배열 유사 액세스를 제공 하는 데이터를 정렬 됩니다.


## <a name="syntax"></a>구문

```fsharp
// Indexed property that has both get and set defined.
member self-identifier.PropertyName
    with get(index-variable) =
        get-function-body
    and set index-variablesvalue-variables =
        set-function-body

// Indexed property that has get only.
member self-identifier.PropertyName(index-variable) =
    get-function-body

// Alternative syntax for indexed property with get only
member self-identifier.PropertyName
    with get(index-variables) =
        get-function-body

// Indexed property that has set only.
member self-identifier.PropertyName
    with set index-variablesvalue-variables = 
        set-function-body
```

## <a name="remarks"></a>설명
이전 구문에는 세 가지 형식 모두에 포함 된 인덱싱된 속성을 정의 하는 방법을 보여 줍니다는 `get` 및 `set` 메서드를가 `get` 메서드만 수도 있고 한 `set` 메서드만 합니다. 만 get 및 set만 표시 된 구문에 대 한 표시 된 구문은 모두 결합 하 고 get과 set 갖고 있는 속성을 만들 수도 있습니다. 이 마지막 형식을 get에 서로 다른 접근성 한정자 및 특성을 배치 하 고 방법을 설정할 수 있습니다.

경우는 *PropertyName* 은 `Item`, 컴파일러는 인덱싱된 기본 속성으로 속성을 처리 합니다. A *인덱싱된 기본 속성* 개체 인스턴스에서 배열 유사 구문을 사용 하 여 액세스할 수 있는 속성입니다. 예를 들어 경우 `obj` 구문을이 속성을 정의 하는 형식의 개체인 `obj.[index]` 속성에 액세스 하는 데 사용 됩니다.

인덱싱된 속성은 속성 및 괄호로 인덱스의 이름을 제공 하기 위해 기본값이 아닌에 액세스 하기 위한 구문입니다. 예를 들어 속성 `Ordinal`, 작성 `obj.Ordinal(index)` 에 액세스할 수 있습니다.

형식을 사용 하는에 관계 없이 항상 사용 해야 변환된에 대 한 형식을 `set` 인덱싱된 속성에는 메서드. 커리 된 함수에 대 한 정보를 참조 하십시오. [함수](../functions/index.md)합니다.

## <a name="example"></a>예제

다음 코드 예제에서는 정 및 기본 및 get 및 set 메서드는 기본이 아닌 인덱싱된 속성의 사용을 보여 줍니다.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3301.fs)]

## <a name="output"></a>출력

```
ONE two three four five six seven eight nine ten
ONE first two second three third four fourth five fifth six 6th
seven seventh eight eighth nine ninth ten tenth
```

## <a name="indexed-properties-with-multiple-index-variables"></a>여러 인덱스 변수를 사용 하 여 인덱싱된 속성
인덱싱된 속성에는 인덱스 변수는 여러 개 있을 수 있습니다. 이 경우 변수는 속성을 사용 하면 쉼표로 구분 됩니다. 이러한 속성의 set 메서드에는 첫 번째는 키가 포함 된 튜플이 및 중 두 번째 설정 되는 값은 두 커리 된 인수가 있어야 합니다.

다음 코드는 여러 개의 인덱스 변수로 인덱싱된 속성의 사용법을 보여줍니다.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3302.fs)]
    
## <a name="see-also"></a>참고 항목
[멤버](index.md)
