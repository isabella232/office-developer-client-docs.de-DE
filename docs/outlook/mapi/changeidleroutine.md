---
title: ChangeIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ChangeIdleRoutine
api_type:
- HeaderDef
ms.assetid: 0a24fe3b-a1ef-4748-b3b3-3bf747473c9d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cfec9356a866c79b687497c3af007c046a20a75e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334433"
---
# <a name="changeidleroutine"></a>ChangeIdleRoutine

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ändert einige oder alle Merkmale einer [FNIDLE](fnidle.md) -basierten Leerlauf Routine. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
VOID ChangeIdleRoutine(
  FTG ftg,
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle,
  USHORT ircIdle
);
```

## <a name="parameters"></a>Parameter

_FTG_
  
> in Funktionstag, das die Leerlauf Routine identifiziert. 
    
_pfnIdle_
  
> in Zeiger auf die Leerlauf Routine. 
    
_pvIdleParam_
  
> in Zeiger auf einen neuen Speicherblock, den die aufrufende Implementierung für die Leerlauf Routine reserviert. 
    
_priIdle_
  
> in Wert, der eine neue Priorität für die Leerlauf Routine darstellt. Mögliche Prioritäten für Implementierungs definierte Routinen sind größer oder kleiner als 0 (null), jedoch nicht NULL. Der Wert 0 (null) ist für ein Benutzerereignis wie ein Mausklick oder eine WM_PAINT-Nachricht reserviert. Werte, die größer als NULL sind, stellen Prioritäten für Hintergrundaufgaben dar, die eine höhere Priorität als Benutzerereignisse haben und als Teil der standardmäßigen Windows-Nachrichten Pumpen Schleife gesendet werden. Werte, die kleiner als 0 (null) sind, stellen Prioritäten für Leerlauf Vorgänge dar, die nur während der Nachrichten Pumpen Leerlaufzeit ausgeführt werden. Beispiele für Prioritäten sind: 1 für die Vordergrund Übermittlung, 1 für das Einfügen von Power-Edit-Zeichen und 3 zum Herunterladen neuer Nachrichten.
    
_csecIdle_
  
> in Eine neue Zeit in Hundertstel Sekunden, die auf die Leerlauf Routine angewendet werden soll. Die Bedeutung des anfänglichen Time-Werts variiert je nachdem, was im _iroIdle_ -Parameter übergeben wird. Es kann Folgendes sein: 
    
  - Der minimale Zeitraum der Benutzer Untätigkeit, die verstreichen muss, bevor das MAPI-Leerlauf Modul die Leerlauf Routine zum ersten Mal aufruft, wenn das FIROWAIT-Flag in _iroIdle_festgelegt ist. Nach diesem Zeitpunkt kann das Leerlauf Modul die Leerlauf Routine so oft aufrufen, wie es erforderlich ist. 
    
  - Das minimale Intervall zwischen Aufrufen der Leerlauf Routine, wenn das FIROINTERVAL-Flag in _iroIdle_festgelegt ist. 
    
_iroIdle_
  
> in Bitmaske von Flags, die neue Optionen für das Aufrufen der Leerlauf Routine angeben. Es muss genau eines der folgenden Flags festgelegt werden:
    
  - FIROINTERVAL: die vom _csecIdle_ -Parameter angegebene Zeit ist das Mindestintervall zwischen aufeinanderfolgenden Aufrufen der Leerlauf Routine. 
      
  - FIROONCEONLY: veraltet. Nicht verwenden. 
      
  - FIROPERBLOCK: veraltet. Nicht verwenden. 
      
  - FIROWAIT: die vom _csecIdle_ -Parameter angegebene Zeit ist die Mindestdauer der Benutzer Untätigkeit, die verstreichen muss, bevor das MAPI-Leerlauf Modul die Leerlauf Routine zum ersten Mal aufruft. Nach diesem Zeitpunkt kann das Leerlauf Modul die Leerlauf Routine so oft aufrufen, wie es erforderlich ist. 
    
_ircIdle_
  
> in Bitmaske der Flags, die zum Anzeigen der Änderungen an der Leerlauf Routine verwendet werden. Die folgenden Flags können in einer beliebigen Kombination festgelegt werden:
    
  - FIRCCSEC: eine Änderung der Zeit, die der Leerlauf Routine zugeordnet ist, also einer Änderung, die durch den im _csecIdle_ -Parameter übergebenen Wert angegeben wird. 
      
  - FIRCIRO: eine Änderung der Optionen für die Leerlauf Routine, also eine Änderung, die durch den im _iroIdle_ -Parameter übergebenen Wert angegeben wird. 
      
  - FIRCPFN: eine Änderung am Zeiger für die Leerlauf Routine, das heißt eine Änderung, die durch den im _pfnIdle_ -Parameter übergebenen Wert angegeben wird. 
      
  - FIRCPRI: eine Änderung der Priorität der Leerlauf Routine, also einer Änderung, die durch den im _priIdle_ -Parameter übergebenen Wert angegeben wird. 
      
  - FIRCPV: eine Änderung des Speicherblocks der Leerlauf Routine, also einer Änderung, die durch den im _pvIdleParam_ -Parameter übergebenen Wert angegeben wird. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Bemerkungen

Die folgenden Funktionen befassen sich mit dem MAPI-Leerlauf Modul und mit Leerlauf Routinen, die auf dem [FNIDLE](fnidle.md) -Funktionsprototyp basieren: 
  
|**Leerlauf Routine Funktion**|**Verwendung**|
|:-----|:-----|
|**ChangeIdleRoutine** <br/> |Ändert die Eigenschaften einer registrierten Leerlauf Routine.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Entfernt eine registrierte Leerlauf Routine aus dem MAPI-System.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deaktiviert oder aktiviert eine registrierte Leerlauf Routine, ohne Sie aus dem MAPI-System zu entfernen.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Fügt eine Leerlauf Routine zum MAPI-System hinzu, mit oder ohne Sie zu aktivieren.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Fährt das MAPI-Leerlauf Modul für die aufrufende Anwendung herunter.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialisiert das MAPI-Leerlauf Modul für die aufrufende Anwendung.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**und **EnableIdleRoutine** nehmen als Eingabeparameter das von **FtgRegisterIdleRoutine**zurückgegebene funktionstag an. 
  
Wenn alle Vordergrund Aufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlauf Modul die Leerlauf Routine mit der höchsten Priorität auf, die zur Ausführung bereit ist. Es gibt keine Garantie für die Anruf Reihenfolge unter Leerlauf Routinen mit derselben Priorität. 
  

