---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: 'Letzte �nderung: Donnerstag, 5. Juli 2012'
ms.openlocfilehash: fbf064201bf8d2733c3eea1e1a24f77b146a23c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564570"
---
# <a name="dnhier"></a>DNHIER

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Informationen für das Herunterladen einer Hierarchie vom Server während der [Hierarchie Zustand herunterladen](download-hierarchy-state.md), die Teil einer vollständigen hierarchiesynchronisierung ist. Dieser Download Prozess verwendet Microsoft Exchange inkrementelle Änderung Synchronisierung (ICS). Weitere Informationen zu ICS finden Sie unter [ICS Bewertungskriterien](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
  
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
  
>  [in] Kennzeichen, die um das entsprechende Verhalten während des Downloads zu bestimmen. 
    
   - DNH_OK
    
   - [in] Download war erfolgreich. Der Client legt dies nach dem Herunterladen von Informationen vom Server.
    
_pstmReserved_
  
> [out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_pxihc_
  
>  [out] Zeiger auf die **IExchangeImportHierarchyChanges** Hierarchie-Schnittstelle unterstützt, die Hierarchie inkrementelle Änderungen herunterladen. Weitere Informationen zu **IExchangeImportHierarchyChanges**finden Sie unter [ICS Bewertungskriterien](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
    
_cEntNew_
  
> [out] Anzahl der Ordner auf dem lokalen Speicher hinzugefügt. Outlook wird dieser Wert während des Herunterladens, bei Verwendung von ICS aufgefüllt.
    
_cEntMod_
  
> [out] Anzahl der Ordner auf dem lokalen Speicher geändert werden. Outlook wird dieser Wert während des Herunterladens, bei Verwendung von ICS aufgefüllt.
    
_cEntDel_
  
> [out] Anzahl der Ordner auf dem lokalen Speicher gelöscht werden soll. Outlook wird dieser Wert während des Herunterladens, bei Verwendung von ICS aufgefüllt.
    
## <a name="see-also"></a>Siehe auch

- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md) 
- [MAPI-Konstanten](mapi-constants.md)

