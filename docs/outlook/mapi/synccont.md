---
title: SYNCCONT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b4307a3-5a8c-89bf-1113-2549556a7fe7
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 82923895353cf600c4d0b78b9a6e16fc7d57e466
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795681"
---
# <a name="synccont"></a>SYNCCONT

**Betrifft**: Outlook 
  
Informationen für den Inhalt der angegebenen Ordner in einem lokalen Speicher mit dem Server synchronisieren, während der [Inhalt Zustand synchronisieren](synchronize-contents-state.md). Dieser Schritt umfasst das soeben hochladen oder eine vollständige Synchronisierung im Zusammenhang mit Upload und klicken Sie dann auf Download.
  
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

## <a name="members"></a>Members

_ulFlags_
  
> [in] Kennzeichen, die um das entsprechende Verhalten während der Synchronisierung zu bestimmen.
    
  - UPC_OK
    
  - [in] Hochladen oder vollständige Synchronisierung war erfolgreich. Der Client legt dies nach Informationen mit dem Server synchronisieren.
    
_iEnt_
  
> [out] Index zum Nachverfolgen der Inhalt in die Anzahl von _cEnt_angegebenen Ordner zu synchronisieren.
    
_cEnt_
  
> [out] Anzahl der Ordner repliziert werden.
    
_pvReserved_
  
> Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_ptagaReserved_
  
> Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_psosReserved_
  
> Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
## <a name="see-also"></a>Siehe auch

- [Über die API-Replikation](about-the-replication-api.md)
- [Informationen zu den Replikationsstatus Computer](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)

