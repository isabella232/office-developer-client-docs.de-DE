---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: 'Letzte Änderung: 05. Juli 2012'
ms.openlocfilehash: 7ec4de850efd7f92c065beb821a26a11aad1c440
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588140"
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
  
>  [out] Verweis auf die **IExchangeImportHierarchyChanges**-Hierarchieschnittstelle, die das Herunterladen von inkrementellen Hierarchieänderungen unterstützt. Weitere Informationen zu **IExchangeImportHierarchyChanges** finden Sie unter [ICS-Auswertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_cEntNew_
  
> [out] Die Anzahl von Ordnern, die dem lokalen Speicher hinzugefügt wurden. Outlook füllt diesen Wert während des Herunterladens bei Verwendung von ICS aus.
    
_cEntMod_
  
> [out] Die Anzahl von Ordnern, die dem lokalen Speicher geändert werden sollen. Outlook füllt diesen Wert während des Herunterladens bei Verwendung von ICS aus.
    
_cEntDel_
  
> [out] Die Anzahl von Ordnern, die im lokalen Speicher gelöscht werden sollen. Outlook füllt diesen Wert während des Herunterladens bei Verwendung von ICS aus.
    
## <a name="see-also"></a>Siehe auch

- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md) 
- [MAPI-Konstanten](mapi-constants.md)

