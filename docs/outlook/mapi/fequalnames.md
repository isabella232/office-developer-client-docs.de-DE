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
ms.openlocfilehash: 8f71b30bd02af8f768da86218456feadda8ea1b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414802"
---
# <a name="fequalnames"></a>FEqualNames

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestimmt, ob zwei MAPI-benannte Eigenschaften identisch sind. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a>Parameter

 _lpName1_
  
> in Zeiger auf eine [MAPINAMEID](mapinameid.md) -Struktur, die die erste benannte Eigenschaft beschreibt. 
    
 _lpName2_
  
> in Zeiger auf eine **MAPINAMEID** -Struktur, die die zweite benannte Eigenschaft beschreibt. 
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Die beiden Eigenschaftennamen sind gleich. 
    
FALSE 
  
> Die beiden Eigenschaftennamen sind ungleich.
    
## <a name="remarks"></a>Bemerkungen

Die **FEqualNames** -Funktion ist nützlich, da die **MAPINAMEID** -Struktur eine [GUID](guid.md) enthält und den Eigenschaftennamen selbst auf mehrere Weise darstellen kann. Dies führt dazu, dass die beiden Strukturen nicht mit einfachen binären Methoden verglichen werden können. 
  
Bei dem Testvorgang wird die Groß-/Kleinschreibung für die Eigenschaftennamen Zeichenfolgen beachtet. 
  

