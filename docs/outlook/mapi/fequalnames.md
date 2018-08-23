---
title: FEqualNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FEqualNames
api_type:
- COM
ms.assetid: 4dd58b0b-dc39-4782-a9ec-05e353c90927
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 09c6540f2a224b7dc89a62c34cfb0c867cef4632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570849"
---
# <a name="fequalnames"></a>FEqualNames

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Bestimmt, ob zwei MAPI benannte Eigenschaften sind identisch. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a>Parameter

 _lpName1_
  
> [in] Zeiger auf eine [MAPINAMEID](mapinameid.md) -Struktur, die die erste benannte Eigenschaft beschreibt. 
    
 _lpName2_
  
> [in] Zeiger auf eine **MAPINAMEID** -Struktur, die zweite benannte Eigenschaft beschreibt. 
    
## <a name="return-value"></a>R�ckgabewert

TRUE 
  
> Die zwei Eigenschaftennamen sind gleich. 
    
FALSE 
  
> Die zwei Eigenschaftennamen sind nicht gleich.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **FEqualNames** -Funktion ist nützlich, da die **MAPINAMEID** Struktur eine [GUID enthält](guid.md) und der Name der Eigenschaft selbst in mehr als eine Möglichkeit darstellen kann. Dies bedeutet, dass die zwei Strukturen nicht durch einfache binäre Methoden verglichen werden können. 
  
Testvorgang beachtet werden für die Eigenschaft Namenszeichenfolgen. 
  

