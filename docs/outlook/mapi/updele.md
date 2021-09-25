---
title: UPDELE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c38aa8be-ae77-0c40-9843-42e07b80db6b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 43b7f65987948b600420ee288dd8b7e0bcea5325
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609243"
---
# <a name="updele"></a>UPDELE

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erweiterte Informationen für Elemente, die in einem lokalen Speicher gelöscht wurden. Diese Informationen werden während des [Upload-Löschstatus](upload-delete-status-state.md)verwendet.
  
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
  
> [out]/[in] Flags, um das entsprechende Verhalten während des Uploads zu bestimmen.
    
  - UPD_ASSOC
    
    - [out] Element ist zugeordnet.
    
  - UPD_MOV
    
    - [out] Element wurde verschoben.
    
  - UPD_OK 
    
    - [in] Hochladen erfolgreich war. Der Client legt dies nach dem Hochladen von Informationen auf den Server fest.
    
  - UPD_MOVED
    
    - [in] Element wurde erfolgreich verschoben.
    
  - UPD_UPDATE
    
    - [in] Markieren Sie das Quellelement als geändert.
    
  - UPD_COMMIT
    
    - [in] Uploadstatus jetzt übernehmen (Eintrag 0).
    
_skey_
  
> [out] Quellschlüssel des Elements.
    
_wetterReserved_
  
> [out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
_binChg_
  
> [out] Ändern Sie den Schlüssel des Zielelements, wenn das Element verschoben wurde.
    
_binPcl_
  
> [out] Ändern sie die Liste des Zielelements, wenn das Element verschoben wurde.
    
_skeyDst_
  
> [out] Quellschlüssel des Zielelements, wenn das Element verschoben wurde.
    
_wissmov_
  
> [out] Zielordnerinformationen, wenn das Element verschoben wurde.
    
## <a name="see-also"></a>Siehe auch

- [Informationen über die Replikations-API](about-the-replication-api.md) 
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)
- [SKEY](skey.md)
- [UPDEL](updel.md)
- [UPMOV](upmov.md)

