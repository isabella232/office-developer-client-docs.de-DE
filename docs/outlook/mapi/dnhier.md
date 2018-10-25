---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: 'Letzte Änderung: 05. Juli 2012'
ms.openlocfilehash: 06f30b4856fc10127aec99975652e28a5e8dda30
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389085"
---
# <a name="dnhier"></a>DNHIER

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informationen zum Herunterladen einer Hierarchie vom Server während des [Zustands „Downloadhierarchie](download-hierarchy-state.md), der Teil einer vollständigen Hierarchiesynchronisierung ist. Bei diesem Downloadvorgang wird Microsoft Exchange Incremental Change Synchronization (ICS) verwendet. Weitere Informationen zu ICS finden Sie unter [ICS-Auswertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct DNHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    PXIHC pxihc; 
    UINT cEntNew; 
   UINT cEntMod; 
    UINT cEntDel; 
};
```

## <a name="members"></a>Elemente

_ulFlags_
  
>  [in] Flags, um das entsprechende Verhalten während des Downloads zu ermitteln. 
    
   - DNH_OK
    
   - [in] Download war erfolgreich. Der Client legt dies nach dem Herunterladen von Informationen vom Server fest.
    
_pstmReserved_
  
> [out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_pxihc_
  
>  [out] Verweis auf die **IExchangeImportHierarchyChanges**-Hierarchieschnittstelle, die das Herunterladen von inkrementelle Hierarchieänderungen unterstützt. Weitere Informationen zu **IExchangeImportHierarchyChanges** finden Sie unter [ICS-Auswertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_cEntNew_
  
> [out] Die Anzahl von Ordnern, die dem lokalen Speicher hinzugefügt wurden. Outlook füllt diesen Wert während des Herunterladens bei Verwendung von ICS aus.
    
_cEntMod_
  
> [out] Die Anzahl von Ordnern, die dem lokalen Speicher geändert werden sollen. Outlook füllt diesen Wert während des Herunterladens bei Verwendung von ICS aus.
    
_cEntDel_
  
> [out] Die Anzahl von Ordnern, die im lokalen Speicher gelöscht werden sollen. Outlook füllt diesen Wert während des Herunterladens bei Verwendung von ICS aus.
    
## <a name="see-also"></a>Siehe auch

- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md) 
- [MAPI-Konstanten](mapi-constants.md)

