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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 62231a900dbe01ebe1e848355226c0589072cd42
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316800"
---
# <a name="deregisteridleroutine"></a>DeregisterIdleRoutine

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Entfernt eine [FNIDLE](fnidle.md) -basierte Leerlauf Routine aus dem MAPI-System. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a>Parameter

 _FTG_
  
> in Funktionstag, das die zu entfernende Leerlauf Routine identifiziert.
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Bemerkungen

Jede Aufgabe in einer Clientanwendung oder einem Dienstanbieter kann jede Leerlauf Routine, für die Sie einen gültigen _FTG_ -Parameter aufweist, aufheben. Insbesondere eine Leerlauf Routine kann sich selbst aufheben. 
  
Die folgenden Funktionen befassen sich mit dem MAPI-Leerlauf Modul und mit Leerlauf Routinen, die auf dem [FNIDLE](fnidle.md) -Funktionsprototyp basieren: 
  
|**Leerlauf Routine Funktion**|**Verwendung**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Ändert die Eigenschaften einer registrierten Leerlauf Routine.  <br/> |
|**DeregisterIdleRoutine** <br/> |Entfernt eine registrierte Leerlauf Routine aus dem MAPI-System.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deaktiviert oder aktiviert eine registrierte Leerlauf Routine, ohne Sie aus dem MAPI-System zu entfernen.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Fügt eine Leerlauf Routine zum MAPI-System hinzu, mit oder ohne Sie zu aktivieren.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Fährt das MAPI-Leerlauf Modul für die aufrufende Anwendung herunter.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialisiert das MAPI-Leerlauf Modul für die aufrufende Anwendung.  <br/> |
   
 **ChangeIdleRoutine**, **DeregisterIdleRoutine**und **EnableIdleRoutine** nehmen als Eingabeparameter das von **FtgRegisterIdleRoutine**zurückgegebene funktionstag an. 
  
Wenn alle Vordergrund Aufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlauf Modul die Leerlauf Routine mit der höchsten Priorität auf, die zur Ausführung bereit ist. Es gibt keine Garantie für die Anruf Reihenfolge unter Leerlauf Routinen mit derselben Priorität. 
  
Nachdem die Leerlauf Routine deregistriert wurde, wird Sie vom Leerlauf Modul nicht erneut aufgerufen. Jede Implementierung, die **DeregisterIdleRoutine** aufruft, muss alle Speicherblöcke freigeben, an die Sie Zeiger für das Leerlauf Modul übergeben hat, die im ursprünglichen Aufruf der **FtgRegisterIdleRoutine** -Funktion verwendet werden sollen. 
  

