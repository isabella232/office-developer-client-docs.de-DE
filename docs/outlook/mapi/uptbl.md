---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 70d23bebfda10339ffb05f573c8c309a44f09d7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795837"
---
# <a name="uptbl"></a>UPTBL

**Betrifft**: Outlook 
  
Informationen zum Hochladen der Inhalt eines Ordners während der [Tabelle Zustand hochladen](upload-table-state.md).
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct UPTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    LPSTR pszName; 
    FEID feid; 
    UINT uintReserved; 
    UPTBLE rgte[2]; 
    UINT iEnt; 
    UINT cEnt; 
    PUPMOV pupmovHead; 
    void* pReserved; 
};
```

## <a name="members"></a>Elemente

_ulFlags_
  
> [in] Kennzeichen, die um das entsprechende Verhalten beim Hochladen zu bestimmen.
    
  - UPT_OK
    
    - [in] Der Upload war erfolgreich. Der Client legt dies nach dem Hochladen der Inhalt des Ordners auf dem Server.
    
_pstmReserved_
  
> [out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_pszName_
  
> [out] Name des Ordners.
    
_feid_
  
> [out] Die EntryID des Ordners.
    
_uintReserved_
  
> [out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_rgte_
  
> [out] Struktur für die folgenden Informationen für normalen (oder nicht ausgeblendeten) und zugeordneten (oder ausgeblendet) Elemente im Ordner: _Rgte [0]_ für normale Elemente und _Rgte [1]_ für verknüpfte Objekte. 
    
   - die Anzahl der neuen oder geänderten Elemente
   - die Anzahl der Elemente lesen 
   - die Anzahl der gelöschten Elemente
    
 _iEnt_
  
> [out] Index zum Nachverfolgen die Anzahl von Änderungen durch _cEnt_angegebenen hochladen.
    
_cEnt_
  
> [out] Anzahl der Änderungen in den Ordner.
    
_pupmovHead_
  
> [out] Kette von [UPMOV](upmov.md) Strukturen. 
    
_Beibehalten_
  
> [out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
## <a name="see-also"></a>Siehe auch

- [Informationen über die Replikations-API](about-the-replication-api.md)
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)
- [UPTBLE](uptble.md)

