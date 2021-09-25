---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: 'Letzte Änderung: 05. Juli 2012'
ms.openlocfilehash: edf83bd47785f273679a79cce8156dfabda39809
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588126"
---
# <a name="dntble"></a>DNTBLE

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informationen zum Herunterladen der Inhalte eines Ordners vom Server während des [Download-Tabellenzustands](download-table-state.md). Bei diesem Downloadvorgang wird Microsoft Exchange Incremental Change Synchronization (ICS) verwendet. Weitere Informationen zu ICS finden Sie unter [ICS-Auswertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a>Elemente

 _cEntNew_
  
> [out] Die Anzahl von Elementen, die dem lokalen Informationsspeichers hinzugefügt wurden. Outlook füllt diesen Wert während des Herunterladens bei Verwendung von ICS aus.
    
 _cEntMod_
  
> [out] Die Anzahl von Elementen, die im lokalen Informationsspeichers geändert wurden. Outlook füllt diesen Wert während des Herunterladens bei Verwendung von ICS aus.
    
 _cEntRead_
  
> [out] Die Anzahl von Elementen, die im lokalen Informationsspeichers als gelesen oder ungelesen markiert wurden. Outlook füllt diesen Wert während des Herunterladens bei Verwendung von ICS aus.
    
 _cEntDel_
  
> [out] Die Anzahl von Elementen, die im lokalen Informationsspeichers gelöscht wurden. Outlook füllt diesen Wert während des Herunterladens bei Verwendung von ICS aus.
    
## <a name="see-also"></a>Siehe auch



[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[DNTBL](dntbl.md)

