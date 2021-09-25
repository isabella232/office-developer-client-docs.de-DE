---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: dd6bc09798a75f7f9b7cae7a11eef39a5cd3feae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609222"
---
# <a name="uptble"></a>UPTBLE

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erweiterte Informationen zum Hochladen des Inhalts eines Ordners während des [Uploadtabellenstatus.](upload-table-state.md)
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct UPTBLE 
{ 
    UINTiEntMod; 
    UINTcEntMod; 
    UINTiEntRead; 
    UINTcEntRead; 
    UINTiEntDel; 
    UINTcEntDel; 
};
```

## <a name="members"></a>Elemente

 _iEntMod_
  
>  [out] Index zum Nachverfolgen des Hochladens der  _cEntMod-Anzahl_ neuer oder geänderter Elemente. 
    
 _cEntMod_
  
>  [out] Die Anzahl der neuen oder geänderten Elemente im Ordner. 
    
 _iEntRead_
  
>  [out] Index zum Nachverfolgen des Uploads der Anzahl von _cEntRead-Leseelementen._ 
    
 _cEntRead_
  
>  [out] Anzahl der gelesenen Elemente im Ordner. 
    
 _iEntDel_
  
>  [out] Index zum Nachverfolgen des Uploads der Anzahl der _gelöschten cEntDel-Elemente._ 
    
 _cEntDel_
  
>  [out] Die Anzahl der gelöschten Elemente im Ordner. 
    
## <a name="see-also"></a>Siehe auch

- [Informationen über die Replikations-API](about-the-replication-api.md) 
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [UPTBL](uptbl.md)

