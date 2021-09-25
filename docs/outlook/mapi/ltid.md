---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ec1902d05c6b5a8403fce4d872129b11159fd7ee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592165"
---
# <a name="ltid"></a>LTID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Generische Long Term ID eines Objekts in einem Outlook Speicher.
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a>Elemente

 _guid_
  
- [out] Die GUID des Servers, der das Objekt erstellt hat.
    
 _globcnt_
  
- [out] Eine eindeutige 6-Byte-Nummer, die das Objekt innerhalb des Outlook Speichers identifiziert.
    
 _wLevel_
  
- [out] Die Hierarchieebene der Eintrags-ID für einen Exchange öffentlichen Favoritenordner.
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[FEID](feid.md)

