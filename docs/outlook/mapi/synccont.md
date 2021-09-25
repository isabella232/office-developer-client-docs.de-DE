---
title: SYNCCONT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 7b4307a3-5a8c-89bf-1113-2549556a7fe7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 212e55485d449601cd93eca4e63a79fe4a3e0b3f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624076"
---
# <a name="synccont"></a>SYNCCONT

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informationen zum Synchronisieren des Inhalts der angegebenen Ordner in einem lokalen Speicher mit dem Server während des [Synchronisierungsinhaltsstatus.](synchronize-contents-state.md) Dies umfasst nur das Hochladen oder eine vollständige Synchronisierung mit einem Upload und dann einem Download.
  
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
  
> [in] Flags, um das entsprechende Verhalten während der Synchronisierung zu bestimmen.
    
  - UPC_OK
    
  - [in] Hochladen oder vollständige Synchronisierung erfolgreich war. Der Client legt dies nach der Synchronisierung von Informationen mit dem Server fest.
    
_iEnt_
  
> [out] Index to track synchronizing the contents in the number of folders specified by  _cEnt_.
    
_cEnt_
  
> [out] Die Anzahl der zu replizierenden Ordner.
    
_pvReserved_
  
> Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_ptagaReserved_
  
> Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_psosReserved_
  
> Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
## <a name="see-also"></a>Siehe auch

- [Informationen über die Replikations-API](about-the-replication-api.md)
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)

