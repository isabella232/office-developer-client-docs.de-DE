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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0d8d1b8509f699b20f6e436d8af2c1d0d97cf4ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791671"
---
# <a name="fequalnames"></a>FEqualNames

  
  
**Betrifft**: Outlook 
  
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
    
## <a name="remarks"></a>Hinweise

Die **FEqualNames** -Funktion ist nützlich, da die **MAPINAMEID** Struktur eine [GUID enthält](guid.md) und der Name der Eigenschaft selbst in mehr als eine Möglichkeit darstellen kann. Dies bedeutet, dass die zwei Strukturen nicht durch einfache binäre Methoden verglichen werden können. 
  
Testvorgang beachtet werden für die Eigenschaft Namenszeichenfolgen. 
  

