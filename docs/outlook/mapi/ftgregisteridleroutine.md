---
title: FtgRegisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtgRegisterIdleRoutine
api_type:
- COM
ms.assetid: 8d9557ba-7919-42c6-9e2f-f10214437d53
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b45b80f09efbd4f05aabc2c868d5bd8eb5fa4cce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327993"
---
# <a name="ftgregisteridleroutine"></a>FtgRegisterIdleRoutine

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt dem MAPI-System eine [FNIDLE](fnidle.md) -funktionsbasierte Leerlauf Routine hinzu. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a>Parameter

_pfnIdle_
  
> in Ein Zeiger auf die Leerlauf Routine. 
    
_pvIdleParam_
  
> in Ein Zeiger auf einen Speicherblock, der vom Leerlauf Modul als Parameter an die Leerlauf Routine übergeben werden soll, wenn diese aufgerufen wird. 
    
_priIdle_
  
> in Die anfängliche Priorität für die Leerlauf Routine. Mögliche Prioritäten für Implementierungs definierte Routinen sind größer oder kleiner als 0 (null), jedoch nicht NULL. Die NULL-Priorität ist für ein Benutzerereignis wie einen Mausklick oder eine WM_PAINT-Nachricht reserviert. Prioritäten, die größer als NULL sind, stellen Hintergrundvorgänge dar, die eine höhere Priorität als Benutzerereignisse haben und als Teil der standardmäßigen Windows-Nachrichten Pumpen Schleife gesendet werden. Prioritäten unter Null stellen Leerlauf Vorgänge dar, die nur während der Nachrichten Pumpen-Leerlaufzeit ausgeführt werden. Es folgen Beispiele für Prioritäten: 1 für die Vordergrund Übermittlung, 2 für das Einfügen von Power-Edit-Zeichen und 3 zum Herunterladen neuer Nachrichten.
    
_csecIdle_
  
> in Der anfängliche Zeitwert in Hundertstel Sekunden, der bei der Angabe von Leerlauf Routine Parametern verwendet werden soll. Die Bedeutung des anfänglichen Time-Werts variiert je nachdem, was im _iroIdle_ -Parameter übergeben wird. Die Bedeutung kann eine der folgenden sein: 
    
  - Der minimale Zeitraum der Benutzer Untätigkeit, die verstreichen muss, bevor das MAPI-Leerlauf Modul die Leerlauf Routine zum ersten Mal aufruft, wenn das FIROWAIT-Flag in _iroIdle_festgelegt ist. Nach diesem Zeitpunkt kann das Leerlauf Modul die Leerlauf Routine so oft aufrufen, wie es erforderlich ist. 
    
  - Das minimale Intervall zwischen Aufrufen der Leerlauf Routine, wenn das FIROINTERVAL-Flag in _iroIdle_festgelegt ist. 
    
_iroIdle_
  
> in Die Bitmaske der Flags, die zum Festlegen der anfänglichen Optionen für die Leerlauf Routine verwendet werden. Die folgenden Flags können festgelegt werden:
    
  FIRONOADJUSTMENT
    
  > Verwenden Sie dieses Flag, um anzugeben, dass der Zeitgeber für die Leerlauf Routine nicht für den Standbymodus oder den Lebenslauf angepasst werden soll. Das Standardverhalten ohne dieses Flag besteht darin, dass die Sleep-Zeit beim Berechnen der verstrichenen Zeit ausgeschlossen wird. Wenn FIRONOADJUSTMENT übergeben wird, wird die Zeit beim Berechnen der verstrichenen Zeit berücksichtigt.
      
  FIRODISABLED
    
  > Die Leerlauf Routine sollte bei der Registrierung deaktiviert werden. Die Standardaktion besteht darin, die Leerlauf Routine zu aktivieren, wenn Sie von **FtgRegisterIdleRoutine** registriert wird. 
      
  FIROINTERVAL 
    
  > Die vom _csecIdle_ -Parameter angegebene Zeit ist das Mindestintervall zwischen aufeinanderfolgenden Aufrufen der Leerlauf Routine. 
      
  FIROONCEONLY 
    
  > Veraltet. Nicht verwenden. 
      
  FIROPERBLOCK 
    
  > Veraltet. Nicht verwenden. 
      
  FIROWAIT 
    
  > Die vom _csecIdle_ -Parameter angegebene Zeit ist die Mindestdauer der Benutzer Untätigkeit, die verstreichen muss, bevor das MAPI-Leerlauf Modul die Leerlauf Routine zum ersten Mal aufruft. Nach diesem Zeitpunkt kann das Leerlauf Modul die Leerlauf Routine so oft aufrufen, wie es erforderlich ist. 
    
## <a name="return-value"></a>Rückgabewert

Die **FtgRegisterIdleRoutine** -Funktion gibt ein function-Tag zurück, das die Leerlauf Routine identifiziert, die dem MAPI-System hinzugefügt wurde. Wenn **FtgRegisterIdleRoutine** die Leerlauf Routine für die Clientanwendung oder den Dienstanbieter, beispielsweise aufgrund von Speicherproblemen, nicht registrieren kann, wird NULL zurückgegeben. 
  
## <a name="remarks"></a>Bemerkungen

Die folgenden Funktionen befassen sich mit dem MAPI-Leerlauf Modul und mit Leerlauf Routinen, die auf dem [FNIDLE](fnidle.md) -Funktionsprototyp basieren. 
  
|**Leerlauf Routine Funktion**|**Verwendung**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Ändert die Eigenschaften einer registrierten Leerlauf Routine.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Entfernt eine registrierte Leerlauf Routine aus dem MAPI-System.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deaktiviert oder aktiviert eine registrierte Leerlauf Routine, ohne Sie aus dem MAPI-System zu entfernen.  <br/> |
|**FtgRegisterIdleRoutine** <br/> |Fügt eine Leerlauf Routine zum MAPI-System hinzu, mit oder ohne Sie zu aktivieren.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Fährt das MAPI-Leerlauf Modul für die aufrufende Anwendung herunter.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialisiert das MAPI-Leerlauf Modul für die aufrufende Anwendung.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**und **EnableIdleRoutine** nehmen als Eingabeparameter das von **FtgRegisterIdleRoutine**zurückgegebene funktionstag an. 
  
Wenn alle Vordergrund Aufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlauf Modul die Leerlauf Routine mit der höchsten Priorität auf, die zur Ausführung bereit ist. Es gibt keine Garantie für die Anruf Reihenfolge unter Leerlauf Routinen mit derselben Priorität. 
  
Es folgt ein Beispiel für die Verwendung des FIRONOADJUSTMENT-Flags im _iroIdle_ -Parameter. 
  
1. Registrieren Sie eine Leerlauf Routine mit einer Verzögerung von 5 Minuten.
    
2. Hibernate/Sleep the Computer after 1 Minute (4 Minuten Links auf dem Timer).
    
3. Setzen Sie den Computer 10 Minuten später fort.
    
Das Standardverhalten ohne FIRONOADJUSTMENT ist, dass Sie noch 4 Minuten warten müssen, bis Ihre Routine ausgeführt wird. Das heißt, der Timer wurde angepasst, um zu ermöglichen, wie lange der Computer eingeschlafen ist. Wenn Sie jedoch FIRONOADJUSTMENT, wird die Leerlauf Routine sofort ausgeführt, da mehr als 5 Minuten in Echtzeit vergangen sind.
  

