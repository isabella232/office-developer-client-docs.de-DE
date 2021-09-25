---
title: FBadRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FBadRestriction
api_type:
- HeaderDef
ms.assetid: 6ad3638c-d088-4a89-9b0d-f5b672162203
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b91c33e237af2dc5da3d24961192fff88e64223f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604999"
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

 _Lpres_
  
> [in] Eine [SRestriction-Struktur,](srestriction.md) die die zu überprüfende Einschränkung definiert. 
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Die angegebene Einschränkung oder eine oder mehrere ihrer Untereinschränkungen ist ungültig. 
    
FALSE 
  
> Die angegebene Einschränkung und alle zugehörigen Untereinschränkungen sind gültig.
    
## <a name="remarks"></a>HinwBemerkungeneise

Nachdem eine Einschränkung überprüft wurde, kann sie in Aufrufen der [IMAPITable::Restrict-Methode](imapitable-restrict.md) übergeben werden, um die Tabelle auf bestimmte Zeilen zu beschränken, an die [IMAPITable::FindRow-Methode](imapitable-findrow.md) zum Suchen einer Tabellenzeile und an Methoden der [IMAPIContainer-Schnittstelle,](imapicontainerimapiprop.md) um eine Einschränkung für ein Containerobjekt auszuführen. 
  

