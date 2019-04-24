---
title: SYNCCONT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b4307a3-5a8c-89bf-1113-2549556a7fe7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: afba7fa718a35d33966d45289461313e349ef2e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349574"
---
# <a name="synccont"></a>SYNCCONT

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informationen zum Synchronisieren des Inhalts bestimmter Ordner in einem lokalen Speicher mit dem Server während des [Synchronisierungs Inhaltsstatus](synchronize-contents-state.md). Dazu gehört das Hochladen oder eine vollständige Synchronisierung mit einem Upload und dann einem Download.
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct SYNCCONT 
{ 
   ULONG   ulFlags; 
   UINT   iEnt; 
   UINT   cEnt; 
   LPVOID    pvReserved; 
   LPSPropTagArray   ptagaReserved; 
   LPSSortOrderSet   psosReserved; 
};
```

## <a name="members"></a>Elemente

_ulFlags_
  
> in Flags zum Bestimmen des geeigneten Verhaltens während der Synchronisierung.
    
  - UPC_OK
    
  - in Die hoch-oder vollständige Synchronisierung war erfolgreich. Der Client legt dies fest, nachdem Informationen mit dem Server synchronisiert wurden.
    
_iEnt_
  
> Out Index, um die Synchronisierung der Inhalte in der Anzahl der durch _cEnt_angegebenen Ordner nachzuverfolgen.
    
_Prozent_
  
> Out Die Anzahl der zu replizierenden Ordner.
    
_pvReserved_
  
> Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_ptagaReserved_
  
> Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_psosReserved_
  
> Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
## <a name="see-also"></a>Siehe auch

- [Informationen über die Replikations-API](about-the-replication-api.md)
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)

