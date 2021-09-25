---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: 81bc97456d0b8ed3cce7071afdd445583a6f0a1d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571423"
---
# <a name="meid"></a>MEID

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bezeichner für ein Outlook Element. Es enthält einen Eintragsbezeichner und andere relevante Informationen.
  
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
  
> 4-Byte-Eintragsbezeichner für das Outlook Element. Weitere Informationen zu MAPI-Eintragsbezeichnern finden Sie unter **[ENTRYID.](entryid.md)** 
    
 _muid_
  
> GUID, die den Store-Anbieter identifiziert. Die Typdefinition von **MAPIUID** finden Sie unter mapidefs.h. 
    
 _Platzhalter_
  
> Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
 _ltidFld_
  
> Langfristige ID des Ordners.
    
 _ltidMsg_
  
> Langfristige ID des Outlook Elements.
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[LTID](ltid.md)
  
[SYNC](sync.md)
  
[UPMSG](upmsg.md)

