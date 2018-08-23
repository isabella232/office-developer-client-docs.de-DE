---
title: UPDELE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c38aa8be-ae77-0c40-9843-42e07b80db6b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2361d225c07d60fab40465b27ad393ca10f6d8eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566586"
---
# <a name="updele"></a>UPDELE

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Erweiterte Informationen für Elemente, die in einem lokalen Speicher gelöscht wurden. Diese Informationen werden während der [Upload löschen Status Zustand](upload-delete-status-state.md)verwendet.
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct UPDELE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
    DWORD   dwReserved; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeyDst; 
    PUPMOV pupmov; 
};
```

## <a name="members"></a>Elemente

_ulFlags_
  
> [Out] / [in] Flags, die entsprechende Verhalten beim Hochladen zu bestimmen.
    
  - UPD_ASSOC
    
    - [out] Element ist verknüpft.
    
  - UPD_MOV
    
    - [out] Element wurde verschoben.
    
  - UPD_OK 
    
    - [in] Der Upload war erfolgreich. Der Client legt dies nach dem Hochladen von Informationen zum Server.
    
  - UPD_MOVED
    
    - [in] Element wurde erfolgreich verschoben.
    
  - UPD_UPDATE
    
    - [in] Mark Quellelement als geändert.
    
  - UPD_COMMIT
    
    - [in] Commit jetzt Upload-Status (Eintrag 0).
    
_SKEY_
  
> [out] Quellschlüssel des Elements.
    
_dwReserved_
  
> [out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
_binChg_
  
> [out] Ändern Sie Schlüssel des Zielelement, wenn Element verschoben wurde.
    
_binPcl_
  
> [out] Ändern Sie Liste der Zielelement, wenn das Element verschoben wurde.
    
_skeyDst_
  
> [out] Schlüssel Source Ziel-Elements, wenn das Element wurde verschoben.
    
_pupmov_
  
> [out] Ordnerinformationen Ziel, wenn das Element wurde verschoben.
    
## <a name="see-also"></a>Siehe auch

- [Informationen über die Replikations-API](about-the-replication-api.md) 
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)
- [SKEY](skey.md)
- [UPDEL](updel.md)
- [UPMOV](upmov.md)

