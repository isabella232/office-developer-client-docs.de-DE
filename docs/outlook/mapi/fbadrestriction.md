---
title: FBadRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadRestriction
api_type:
- HeaderDef
ms.assetid: 6ad3638c-d088-4a89-9b0d-f5b672162203
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: eb3e0d5a96121f63166da2025743b7ef89f4ecf6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432240"
---
# <a name="fbadrestriction"></a>FBadRestriction

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft eine Einschränkung, die zum Einschränken einer Tabellenansicht verwendet wird. 
  
|||
|:-----|:-----|
|Headerdatei:  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a>Parameter

 _lpres_
  
> in Eine [SRestriction](srestriction.md) -Struktur, die die zu überprüfende Einschränkung definiert. 
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Die angegebene Einschränkung oder mindestens eine der unter Einschränkungen ist ungültig. 
    
FALSE 
  
> Die angegebene Einschränkung und alle zugehörigen unter Einschränkungen sind gültig.
    
## <a name="remarks"></a>Bemerkungen

Sobald eine Einschränkung validiert wurde, kann Sie in Aufrufen der [IMAPITable:: Restrict](imapitable-restrict.md) -Methode übergeben werden, um die Tabelle auf bestimmte Zeilen einzuschränken, auf die [IMAPITable:: FindRow](imapitable-findrow.md) -Methode, um eine Tabellenzeile und die Methoden des [IMAPIContainer](imapicontainerimapiprop.md) zu finden. Schnittstelle zum Durchführen einer Einschränkung für ein Container-Objekt. 
  

