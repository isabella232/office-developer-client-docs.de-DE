---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: 0196291f739d66bdab7369d0eccb53f273398792
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630915"
---
# <a name="feid"></a>FEID

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bezeichner für einen Ordner. Es enthält einen Eintragsbezeichner und andere relevante Informationen.
  
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
  
> 4-Byte-Eintragsbezeichner für den Ordner. Weitere Informationen zu MAPI-Eintragsbezeichnern finden Sie unter **[ENTRYID.](entryid.md)** 
    
 _muid_
  
> GUID, die den Store-Anbieter identifiziert. Die Typdefinition von **MAPIUID** finden Sie unter mapidefs.h. 
    
 _Platzhalter_
  
> Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
 _ltid_
  
> Langfristige ID des Ordners.
    
## <a name="see-also"></a>Siehe auch



[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[LTID](ltid.md)
  
[UPFLD](upfld.md)
  
[SYNC](sync.md)

