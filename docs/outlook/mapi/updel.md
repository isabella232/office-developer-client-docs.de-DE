---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fd3b18f54fdc8e8e4762f5676c5be49b6b934749
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619589"
---
# <a name="updel"></a>UPDEL

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informationen zu Elementen, die in einem lokalen Speicher gelöscht wurden. Diese Informationen werden während des [Upload-Löschstatus](upload-delete-status-state.md)verwendet.
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a>Elemente

 _vererz_
  
>  [out] Vektor von [UPDELE-Einträgen.](updele.md) 
    
 _cEnt_
  
> [out] Anzahl der Einträge in *der Veröffentlichungsversion.* 
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[MAPI-Konstanten](mapi-constants.md)

