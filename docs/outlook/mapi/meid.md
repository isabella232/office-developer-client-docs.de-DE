---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Zuletzt geändert: 03 Juli, 2012'
ms.openlocfilehash: a9aea0db700de9c82aa2a41a443ebf03da8ce9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430308"
---
# <a name="meid"></a>MEID

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bezeichner für ein Outlook-Element. Sie enthält eine Eintrags-ID und andere relevante Informationen.
  
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
  
> 4-Byte-Eintrags-ID für das Outlook-Element. Weitere Informationen zu MAPI-Eintrags Bezeichnern **[](entryid.md)** finden Sie Untereintrags-ID. 
    
 _muid_
  
> GUID, die den Informationsspeicher Anbieter identifiziert. Weitere Informationen finden Sie unter mapidefs. h für die Typdefinition von **MAPIUID**. 
    
 _Platzhalter_
  
> Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
 _ltidFld_
  
> Langfristige ID des Ordners.
    
 _ltidMsg_
  
> Langfristige ID des Outlook-Elements.
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[LTID](ltid.md)
  
[SYNCHRONISIERUNGS](sync.md)
  
[UPMSG](upmsg.md)

