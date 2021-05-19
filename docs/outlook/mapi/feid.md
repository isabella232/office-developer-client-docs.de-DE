---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Letzte Änderung: 02. Juli 2012'
ms.openlocfilehash: 88716719857cfd623d30a3684fc997ea8019455e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409811"
---
# <a name="feid"></a>FEID

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bezeichner für einen Ordner. Sie enthält eine Eintrags-ID und andere relevante Informationen.
  
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
  
> 4-Byte-Eintrags-ID für den Ordner. Weitere Informationen zu MAPI-Eintragsbezeichnern finden Sie unter **[ENTRYID](entryid.md)**. 
    
 _muid_
  
> GUID, die den Speicheranbieter identifiziert. Die Typdefinition von **MAPIUID** finden Sie unter mapidefs.h. 
    
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

