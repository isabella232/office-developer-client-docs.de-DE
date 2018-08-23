---
title: DeregisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DeregisterIdleRoutine
api_type:
- COM
ms.assetid: a8ada6fe-9963-4c25-b4b4-db77f9517368
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 78d499dabe60a8051c6a2a77abad4b7d6f2ed159
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591954"
---
# <a name="deregisteridleroutine"></a>DeregisterIdleRoutine

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Entfernt eine [FNIDLE](fnidle.md) basierend im Leerlauf Routine aus dem MAPI-System. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a>Parameter

 _ftg_
  
> [in] Funktion-Tag zur Identifizierung der im Leerlauf Routine entfernt werden soll.
    
## <a name="return-value"></a>Rückgabewert

None.
  
## <a name="remarks"></a>HinwBemerkungeneise

Jede Aufgabe in einer Clientanwendung oder Dienstanbieter kann eine beliebige im Leerlauf Routine Aufheben der Registrierung für den sie einen gültigen _Ftg_ Parameter verfügt. Insbesondere kann eine im Leerlauf Routine selbst Aufheben der Registrierung. 
  
Die folgenden Funktionen Umgang mit der MAPI-Modul im Leerlauf und im Leerlauf Routinen basierend auf den [FNIDLE](fnidle.md) Funktionsprototyp: 
  
|**Im Leerlauf routinemäßige-Funktion**|**Nutzung**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Ändert die Eigenschaften einer registrierten im Leerlauf Routine.  <br/> |
|**DeregisterIdleRoutine** <br/> |Entfernt eine registrierte im Leerlauf Routine aus dem MAPI-System.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Aktiviert oder deaktiviert erneut eine registrierte im Leerlauf Routine ohne aus der MAPI-System entfernt.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Das MAPI-System, mit oder ohne Aktivieren hinzugefügt eine im Leerlauf Routine.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Das im Leerlauf MAPI-Modul für die aufrufende Anwendung geschlossen wird.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialisiert das im Leerlauf MAPI-Modul für die aufrufende Anwendung.  <br/> |
   
 **ChangeIdleRoutine**, **DeregisterIdleRoutine**und **EnableIdleRoutine** werden als Eingabeparameter das Function-Tag von **FtgRegisterIdleRoutine**zurückgegeben. 
  
Wenn alle Vordergrund Aufgaben für die Plattform Leerlauf, ruft das MAPI-im Leerlauf-Modul die höchste Priorität im Leerlauf Routine, die zur Ausführung bereit ist. Es gibt keine Garantie für den Aufruf Reihenfolge zwischen im Leerlauf Routinen, der die gleiche Priorität. 
  
Nachdem die im Leerlauf Routine aufgehoben wird, wird das Modul im Leerlauf nicht erneut aufgerufen. Jede Implementierung, die **DeregisterIdleRoutine** aufruft, muss alle Speicherblöcke freigeben an die dieser Zeiger in seiner ursprünglichen Aufruf der Funktion **FtgRegisterIdleRoutine** verwenden, die im Leerlauf Engine übergeben. 
  

