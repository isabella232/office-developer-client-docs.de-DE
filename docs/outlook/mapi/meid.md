---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Zuletzt geändert: 03 Juli 2012'
ms.openlocfilehash: 24cc4b00f02c61395565fb7ddeb6a5b5a62afdc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591940"
---
# <a name="meid"></a>MEID

 
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Bezeichner für ein Outlook-Element. Sie enthält eine Eintrags-ID und weitere relevante Informationen.
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct MEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltidFld; 
    LTID ltidMsg; 
};
```

## <a name="members"></a>Elemente

 _abFlags_
  
> 4-Byte-Eintrags-ID für das Outlook-Element. Weitere Informationen zu MAPI-Eintragsbezeichner finden Sie unter **[ENTRYID](entryid.md)**. 
    
 _muid_
  
> GUID, den Speicheranbieter identifiziert. Finden Sie unter mapidefs.h für die Definition des **MAPIUID**Typs. 
    
 _Platzhalter_
  
> Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
 _ltidFld_
  
> Langfristige ID des Ordners.
    
 _ltidMsg_
  
> Langfristige ID des Outlook-Elements.
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[LTID](ltid.md)
  
[SYNC](sync.md)
  
[UPMSG](upmsg.md)

