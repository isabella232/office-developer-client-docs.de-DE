---
title: FtgRegisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FtgRegisterIdleRoutine
api_type:
- COM
ms.assetid: 8d9557ba-7919-42c6-9e2f-f10214437d53
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0ba14e2cb0b7c41460a54f31e80099ddfb27cfb7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621024"
---
# <a name="ftgregisteridleroutine"></a>FtgRegisterIdleRoutine

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt dem MAPI-System eine [FNIDLE-funktionsbasierte](fnidle.md) Leerlaufroutine hinzu. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
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
  
> [in] Ein Zeiger auf die Leerlaufroutine. 
    
_pvIdleParam_
  
> [in] Ein Zeiger auf einen Speicherblock, den das Leerlaufmodul als Parameter an die Leerlaufroutine übergeben soll, wenn es ihn aufruft. 
    
_priIdle_
  
> [in] Die anfängliche Priorität für die Leerlaufroutine. Mögliche Prioritäten für implementierungsdefinierte Routinen sind größer oder kleiner als Null, aber nicht Null. Die Nullpriorität ist für ein Benutzerereignis reserviert, z. B. ein Mausklick oder eine WM_PAINT Nachricht. Prioritäten größer als Null stellen Hintergrundaufgaben dar, die eine höhere Priorität als Benutzerereignisse haben und als Teil der Standardschleife Windows Nachricht verteilt werden. Prioritäten, die kleiner als Null sind, stellen Leerlaufaufgaben dar, die nur während der Leerlaufzeit der Nachricht ausgeführt werden. Beispiele für Prioritäten sind: 1 für die Vordergrundübermittlung, 2 für die Einfügung von Power-Edit-Zeichen und 3 zum Herunterladen neuer Nachrichten.
    
_csecIdle_
  
> [in] Der Anfangszeitwert in Hundertstel einer Sekunde, der zum Angeben von Routineparametern im Leerlauf verwendet werden soll. Die Bedeutung des anfänglichen Zeitwerts variiert, je nachdem, was im  _iroIdle-Parameter_ übergeben wird. Die Bedeutung kann eine der folgenden Sein: 
    
  - Der minimale Zeitraum der Benutzerinaktivität, der verstrichen sein muss, bevor das MAPI-Leerlaufmodul zum ersten Mal die Leerlaufroutine aufruft, wenn das FIROWAIT-Flag in  _iroIdle_ festgelegt ist. Nach Ablauf dieser Zeit kann das Leerlaufmodul die Leerlaufroutine so oft wie nötig aufrufen. 
    
  - Das minimale Intervall zwischen Aufrufen der Leerlaufroutine, wenn das FIROINTERVAL-Flag in  _iroIdle_ festgelegt ist. 
    
_iroIdle_
  
> [in] Die Bitmaske von Flags, die zum Festlegen der anfänglichen Optionen für die Leerlaufroutine verwendet werden. Die folgenden Flags können festgelegt werden:
    
  FIRONOADJUSTMENT
    
  > Verwenden Sie dieses Kennzeichen, um anzugeben, dass der Leerlaufroutinen-Timer nicht für den Ruhezustand oder die Fortsetzung angepasst werden soll. Das Standardverhalten ohne dieses Kennzeichen ist, dass die Ruhezustandszeit bei der Berechnung der verstrichenen Zeit ausgeschlossen wird. Wenn FIRONOADJUSTMENT übergeben wird, wird die Ruhezustandszeit bei der Berechnung der verstrichenen Zeit einbezogen.
      
  FIRODISABLED
    
  > Die Leerlaufroutine sollte bei der Registrierung deaktiviert werden. Die Standardaktion besteht darin, die Leerlaufroutine zu aktivieren, wenn **FtgRegisterIdleRoutine** sie registriert. 
      
  FIROINTERVAL 
    
  > Die durch den  _csecIdle-Parameter_ angegebene Zeit ist das minimale Intervall zwischen aufeinander folgenden Aufrufen der Leerlaufroutine. 
      
  FIROONCEONLY 
    
  > Veraltet. Nicht verwenden.  
      
  FIROPERBLOCK 
    
  > Veraltet. Nicht verwenden.  
      
  FIROWAIT 
    
  > Die durch den  _csecIdle-Parameter_ angegebene Zeit ist der minimale Zeitraum der Benutzerinaktivität, der verstrichen sein muss, bevor das MAPI-Leerlaufmodul die Leerlaufroutine zum ersten Mal aufruft. Nach Ablauf dieser Zeit kann das Leerlaufmodul die Leerlaufroutine so oft wie nötig aufrufen. 
    
## <a name="return-value"></a>Rückgabewert

Die **FtgRegisterIdleRoutine-Funktion** gibt ein Funktionstag zurück, das die Leerlaufroutine identifiziert, die dem MAPI-System hinzugefügt wurde. Wenn **FtgRegisterIdleRoutine** die Leerlaufroutine für die Clientanwendung oder den Dienstanbieter nicht registrieren kann, z. B. aufgrund von Speicherproblemen, wird NULL zurückgegeben. 
  
## <a name="remarks"></a>Bemerkungen

Die folgenden Funktionen befassen sich mit dem MAPI-Leerlaufmodul und mit Leerlaufroutinen, die auf dem [FNIDLE-Funktionsprototyp](fnidle.md) basieren. 
  
|**Routinefunktion "Leerlauf"**|**Nutzung**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Ändert die Merkmale einer registrierten Leerlaufroutine.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Entfernt eine registrierte Leerlaufroutine aus dem MAPI-System.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deaktiviert oder aktiviert eine registrierte Leerlaufroutine erneut, ohne sie aus dem MAPI-System zu entfernen.  <br/> |
|**FtgRegisterIdleRoutine** <br/> |Fügt eine Leerlaufroutine zum MAPI-System hinzu, mit oder ohne sie zu aktivieren.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Beendet das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialisiert das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine** und **EnableIdleRoutine** verwenden als Eingabeparameter das von **FtgRegisterIdleRoutine** zurückgegebene Funktionstag. 
  
Wenn alle Vordergrundaufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlaufmodul die Leerlaufroutine mit der höchsten Priorität auf, die zur Ausführung bereit ist. Es gibt keine Garantie für die Anrufreihenfolge zwischen Leerlaufroutinen mit derselben Priorität. 
  
Es folgt ein Beispiel für die Verwendung des FIRONOADJUSTMENT-Flags im _iroIdle-Parameter._ 
  
1. Registrieren Sie eine Leerlaufroutine mit einer Verzögerung von 5 Minuten.
    
2. Ruhezustand/Ruhezustand des Computers nach 1 Minute (4 Minuten auf dem Timer).
    
3. Setzen Sie den Computer 10 Minuten später fort.
    
Das Standardverhalten ohne FIRONOADJUSTMENT besteht darin, dass Sie noch 4 Minuten warten müssen, bis Ihre Routine ausgeführt wird. Das heißt, Der Timer wurde so angepasst, dass er angibt, wie lange der Computer eingelummert hat. Wenn Sie jedoch FIRONOADJUSTMENT übergeben, wird die Leerlaufroutine sofort ausgeführt, da mehr als 5 Minuten Echtzeit vergangen sind.
  

