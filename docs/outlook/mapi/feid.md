---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Zuletzt geändert: 02 Juli 2012'
ms.openlocfilehash: 3e534f91863e2a1300e03d112d1f532f486eedd9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588307"
---
# <a name="feid"></a>FEID

 
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Bezeichner für einen Ordner. Sie enthält eine Eintrags-ID und weitere relevante Informationen.
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a>Elemente

 _abFlags_
  
> 4-Byte-Eintrags-ID für den Ordner. Weitere Informationen zu MAPI-Eintragsbezeichner finden Sie unter **[ENTRYID](entryid.md)**. 
    
 _muid_
  
> GUID, den Speicheranbieter identifiziert. Finden Sie unter mapidefs.h für die Definition des **MAPIUID**Typs. 
    
 _Platzhalter_
  
> Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
 _ltid_
  
> Langfristige ID des Ordners.
    
## <a name="see-also"></a>Siehe auch



[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[LTID](ltid.md)
  
[UPFLD](upfld.md)
  
[SYNC](sync.md)

