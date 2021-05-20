---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b401f54df020fb6553cbdcc5b85206ee422a8429
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438113"
---
# <a name="uptbl"></a>UPTBL

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informationen zum Hochladen des Inhalts eines Ordners während des [Status der Uploadtabelle](upload-table-state.md).
  
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
  
> [in] Flags, um das entsprechende Verhalten während des Uploads zu bestimmen.
    
  - UPT_OK
    
    - [in] Hochladen war erfolgreich. Der Client legt dies nach dem Hochladen des Ordnerinhalts auf den Server fest.
    
_pstmReserved_
  
> [out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_pszName_
  
> [out] Der Name des Ordners.
    
_feid_
  
> [out] Eintrags-ID des Ordners.
    
_uintReserved_
  
> [out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_rgte_
  
> [out] Struktur zum Speichern der folgenden Informationen für normale (oder nicht ausgeblendete) Elemente und zugeordnete (oder ausgeblendete) Elemente im Ordner:  _rgte[0]_ ist für normale Elemente und  _rgte[1]_ für zugeordnete Elemente. 
    
   - Die Anzahl der neuen oder geänderten Elemente
   - Die Anzahl der gelesenen Elemente 
   - Die Anzahl der gelöschten Elemente
    
 _iEnt_
  
> [out] Index zum Nachverfolgen des Hochladens der von _cEnt angegebenen Anzahl von Änderungen._
    
_cEnt_
  
> [out] Anzahl der Änderungen am Ordner.
    
_pupmovHead_
  
> [out] Kette von [UPMOV-Strukturen.](upmov.md) 
    
_pReserved_
  
> [out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
## <a name="see-also"></a>Siehe auch

- [Informationen über die Replikations-API](about-the-replication-api.md)
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)
- [UPTBLE](uptble.md)

