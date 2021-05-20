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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430406"
---
# <a name="synccont"></a>SYNCCONT

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informationen zum Synchronisieren des Inhalts der angegebenen Ordner in einem lokalen Speicher mit dem Server während des [Synchronisierungsinhaltsstatus](synchronize-contents-state.md). Dies umfasst lediglich das Hochladen oder eine vollständige Synchronisierung, die einen Upload und dann einen Download umfasst.
  
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
    
  - [in] Hochladen oder vollständige Synchronisierung war erfolgreich. Der Client legt dies nach der Synchronisierung von Informationen mit dem Server fest.
    
_iEnt_
  
> [out] Index, um die Synchronisierung der Inhalte in der anzahl der von _cEnt angegebenen Ordner nachverfolgt zu werden._
    
_cEnt_
  
> [out] Anzahl der zu replizierenden Ordner.
    
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

