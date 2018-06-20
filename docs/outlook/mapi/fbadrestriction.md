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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 43e0d8d28836b3114ab2029bc1f241197c569ffc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791663"
---
# <a name="fbadrestriction"></a>FBadRestriction

  
  
**Betrifft**: Outlook 
  
Überprüft eine Einschränkung verwendet, um einer Tabellenansicht einzuschränken. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a>Parameter

 _lpres_
  
> [in] Eine [SRestriction](srestriction.md) -Struktur definieren die Einschränkung überprüft werden soll. 
    
## <a name="return-value"></a>R�ckgabewert

TRUE 
  
> Die angegebene Einschränkung oder eine oder mehrere der seine Subrestrictions ist ungültig. 
    
FALSE 
  
> Die angegebene Beschränkung und alle seine Subrestrictions sind gültig.
    
## <a name="remarks"></a>Hinweise

Nach der Überprüfung einer Einschränkung, kann sie in der Tabelle auf bestimmte Zeilen, an die [IMAPITable](imapitable-findrow.md) -Methode, um eine Tabellenzeile zu suchen und die Methoden des der [IMAPIContainer](imapicontainerimapiprop.md) einschränken Aufrufen an die [Methode IMAPITable:: Restrict](imapitable-restrict.md) -Methode übergeben werden Schnittstelle für eine Beschränkung für ein Container-Objekt ausführen. 
  

