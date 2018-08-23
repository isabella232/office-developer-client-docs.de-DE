---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: 'Letzte �nderung: Donnerstag, 5. Juli 2012'
ms.openlocfilehash: d92e8d7b3fb14051ffceb829f3df3f6fa12e6e23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565858"
---
# <a name="dntble"></a>DNTBLE

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Informationen für den Inhalt eines Ordners auf dem Server während der [Tabelle Downloadstatus](download-table-state.md)herunterladen. Dieser Download Prozess verwendet Microsoft Exchange inkrementelle Änderung Synchronisierung (ICS). Weitere Informationen zu ICS finden Sie unter [ICS Bewertungskriterien](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
  
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
  
> [out] Anzahl der Elemente im lokalen Speicher hinzugefügt. Outlook wird dieser Wert während des Herunterladens, bei Verwendung von ICS aufgefüllt.
    
 _cEntMod_
  
> [out] Anzahl der Elemente, die auf dem lokalen Speicher geändert. Outlook wird dieser Wert während des Herunterladens, bei Verwendung von ICS aufgefüllt.
    
 _cEntRead_
  
> [out] Anzahl der Elemente lesen oder auf dem lokalen Speicher als ungelesen markiert. Outlook wird dieser Wert während des Herunterladens, bei Verwendung von ICS aufgefüllt.
    
 _cEntDel_
  
> [out] Anzahl der Elemente, die auf dem lokalen Speicher gelöscht. Outlook wird dieser Wert während des Herunterladens, bei Verwendung von ICS aufgefüllt.
    
## <a name="see-also"></a>Siehe auch



[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[DNTBL](dntbl.md)

