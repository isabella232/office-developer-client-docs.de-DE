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
ms.openlocfilehash: bb2d347d218a7c33a2184bf1fcf181a11fa7d8fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791677"
---
# <a name="feid"></a>FEID

 
  
**Betrifft**: Outlook 
  
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

