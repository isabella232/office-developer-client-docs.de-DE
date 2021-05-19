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
ms.openlocfilehash: 9bd61739b14d0ec382a9d582689c1049fe89429b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424882"
---
# <a name="updele"></a>UPDELE

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erweiterte Informationen für Elemente, die in einem lokalen Speicher gelöscht wurden. Diese Informationen werden während des [Statusstatus zum Hochladen des Löschstatus verwendet.](upload-delete-status-state.md)
  
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
  
> [out]/[in] Flags, um das entsprechende Verhalten beim Hochladen zu bestimmen.
    
  - UPD_ASSOC
    
    - [out] Element ist zugeordnet.
    
  - UPD_MOV
    
    - [out] Element wurde verschoben.
    
  - UPD_OK 
    
    - [in] Hochladen war erfolgreich. Der Client legt dies nach dem Hochladen von Informationen auf den Server fest.
    
  - UPD_MOVED
    
    - [in] Element wurde erfolgreich verschoben.
    
  - UPD_UPDATE
    
    - [in] Markieren Sie das Quellelement als geändert.
    
  - UPD_COMMIT
    
    - [in] Commituploadstatus jetzt (Eintrag 0).
    
_skey_
  
> [out] Quellschlüssel des Elements.
    
_dwReserved_
  
> [out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
_binChg_
  
> [out] Ändern Sie den Schlüssel des Zielelements, wenn das Element verschoben wurde.
    
_binPcl_
  
> [out] Ändern der Liste des Zielelements, wenn das Element verschoben wurde.
    
_skeyDst_
  
> [out] Quellschlüssel des Zielelements, wenn das Element verschoben wurde.
    
_pupmov_
  
> [out] Zielordnerinformationen, wenn das Element verschoben wurde.
    
## <a name="see-also"></a>Siehe auch

- [Informationen über die Replikations-API](about-the-replication-api.md) 
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)
- [SKEY](skey.md)
- [UPDEL](updel.md)
- [UPMOV](upmov.md)

