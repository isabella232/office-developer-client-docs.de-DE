---
title: FEqualNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FEqualNames
api_type:
- COM
ms.assetid: 4dd58b0b-dc39-4782-a9ec-05e353c90927
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 51052bd3ee46e880f84cbc0fd5ace69f2ae68f21
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604992"
---
# <a name="fequalnames"></a>FEqualNames

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestimmt, ob zwei benannte MAPI-Eigenschaften identisch sind. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a>Parameter

 _lpName1_
  
> [in] Zeiger auf eine [MAPINAMEID-Struktur,](mapinameid.md) die die erste benannte Eigenschaft beschreibt. 
    
 _lpName2_
  
> [in] Zeiger auf eine **MAPINAMEID-Struktur,** die die zweite benannte Eigenschaft beschreibt. 
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Die beiden Eigenschaftennamen sind gleich. 
    
FALSE 
  
> Die beiden Eigenschaftennamen sind ungleich.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **FEqualNames-Funktion** ist nützlich, da die **MAPINAMEID-Struktur** eine [GUID](guid.md) enthält und den Eigenschaftsnamen selbst auf mehrere Weise darstellen kann. Dies bedeutet, dass die beiden Strukturen nicht mit einfachen binären Methoden verglichen werden können. 
  
Beim Testvorgang wird die Groß-/Kleinschreibung für die Eigenschaftennamenzeichenfolgen beachtet. 
  

