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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b45b80f09efbd4f05aabc2c868d5bd8eb5fa4cce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418521"
---
# <a name="ftgregisteridleroutine"></a>FtgRegisterIdleRoutine

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt dem MAPI-System eine funktionsbasierte Leerlaufroutine für [FNIDLE](fnidle.md) hinzu. 
  
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
  
> [in] Ein Zeiger auf einen Speicherblock, den das Leerlaufmodul als Parameter an die Leerlaufroutine übergeben soll, wenn es es aufruft. 
    
_priIdle_
  
> [in] Die anfängliche Priorität für die Leerlaufroutine. Mögliche Prioritäten für implementierungsdefinierte Routinen sind größer oder kleiner als Null, aber nicht Null. Die Nullpriorität ist für ein Benutzerereignis wie z. B. einen Mausklick oder eine WM_PAINT reserviert. Prioritäten, die größer als Null sind, stellen Hintergrundaufgaben dar, die eine höhere Priorität als Benutzerereignisse haben und als Teil der standardmäßigen Nachrichtenumpumpschleife Windows werden. Prioritäten kleiner als Null stellen Leerlaufaufgaben dar, die nur während der Leerlaufzeit der Nachrichtenumpumpung ausgeführt werden. Beispiele für Prioritäten sind: 1 für die Vordergrundübermittlung, 2 für das Einfügen von Power-Edit-Zeichen und 3 für das Herunterladen neuer Nachrichten.
    
_csecIdle_
  
> [in] Der anfängliche Zeitwert in Hundertstel sekunden, der bei der Angabe von Routineparametern im Leerlauf verwendet werden soll. Die Bedeutung des Anfänglichen Zeitwerts variiert, je nachdem, was im  _iroIdle-Parameter übergeben_ wird. Die Bedeutung kann eine der folgenden sein: 
    
  - Der Minimale Zeitraum der Untätigkeit des Benutzers, der verstreichen muss, bevor das MAPI-Leerlaufmodul die Leerlaufroutine zum ersten Mal aufruft, wenn das FIROWAIT-Flag in  _iroIdle_ festgelegt ist. Nach dieser Zeit kann das Leerlaufmodul die Leerlaufroutine so oft wie nötig aufrufen. 
    
  - Das Mindestintervall zwischen Aufrufen der Leerlaufroutine, wenn das FIROINTERVAL-Flag in _iroIdle festgelegt ist._ 
    
_iroIdle_
  
> [in] Die Bitmaske der Flags, mit der erste Optionen für die Leerlaufroutine festgelegt werden. Die folgenden Kennzeichen können festgelegt werden:
    
  FIRONOADJUSTMENT
    
  > Verwenden Sie dieses Flag, um anzugeben, dass der Leerlaufroutinentimer nicht für den Ruhezustand oder die Fortsetzung angepasst werden soll. Das Standardverhalten ohne dieses Flag ist, dass die Ruhezeit beim Berechnen der verstrichenen Zeit ausgeschlossen wird. Wenn FIRONOADJUSTMENT übergeben wird, wird die Ruhezeit bei der Berechnung der verstrichenen Zeit einbezogen.
      
  FIRODISABLED
    
  > Die Leerlaufroutine sollte bei der Registrierung deaktiviert werden. Die Standardaktion besteht in der Aktivierung der Leerlaufroutine, wenn **FtgRegisterIdleRoutine** sie registriert. 
      
  FIROINTERVAL 
    
  > Die durch den  _csecIdle-Parameter_ angegebene Zeit ist das Mindestintervall zwischen aufeinander folgenden Aufrufen der Leerlaufroutine. 
      
  FIROONCEONLY 
    
  > Veraltet. Nicht verwenden.  
      
  FIROPERBLOCK 
    
  > Veraltet. Nicht verwenden.  
      
  FIROWAIT 
    
  > Die durch den  _csecIdle-Parameter_ angegebene Zeit ist der minimale Zeitraum der Untätigkeit des Benutzers, der verstreichen muss, bevor das #A0 die Leerlaufroutine zum ersten Mal aufruft. Nach dieser Zeit kann das Leerlaufmodul die Leerlaufroutine so oft wie nötig aufrufen. 
    
## <a name="return-value"></a>Rückgabewert

Die **FtgRegisterIdleRoutine-Funktion** gibt ein Funktionstag zurück, das die Leerlaufroutine identifiziert, die dem MAPI-System hinzugefügt wurde. Wenn **FtgRegisterIdleRoutine** die Leerlaufroutine für die Clientanwendung oder den Dienstanbieter nicht registrieren kann, z. B. aufgrund von Speicherproblemen, gibt es NULL zurück. 
  
## <a name="remarks"></a>Hinweise

Die folgenden Funktionen befassen sich mit dem MAPI-Leerlaufmodul und mit Leerlaufroutinen, die auf dem Prototyp der [FNIDLE-Funktion](fnidle.md) basieren. 
  
|**Routinefunktion im Leerlauf**|**Nutzung**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Ändert die Merkmale einer registrierten Leerlaufroutine.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Entfernt eine registrierte Leerlaufroutine aus dem MAPI-System.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deaktiviert oder aktiviert eine registrierte Leerlaufroutine, ohne sie aus dem MAPI-System zu entfernen.  <br/> |
|**FtgRegisterIdleRoutine** <br/> |Fügt dem MAPI-System eine Leerlaufroutine mit oder ohne Aktivierung hinzu.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Beendet das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialisiert das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine** und **EnableIdleRoutine** nehmen als Eingabeparameter das von **FtgRegisterIdleRoutine** zurückgegebene Funktionstag an. 
  
Wenn alle Vordergrundaufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlaufmodul die Leerlaufroutine mit der höchsten Priorität auf, die ausgeführt werden kann. Es gibt keine Garantie für das Aufrufen der Reihenfolge zwischen Leerlaufroutinen mit derselben Priorität. 
  
Im Folgenden sehen Sie ein Beispiel für die Verwendung des FIRONOADJUSTMENT-Flag im _iroIdle-Parameter._ 
  
1. Registrieren Sie eine Leerlaufroutine mit einer Verzögerung von 5 Minuten.
    
2. Ruhezustand/Ruhezustand des Computers nach 1 Minute (4 Minuten im Timer).
    
3. Setzen Sie den Computer 10 Minuten später fort.
    
Das Standardverhalten ohne FIRONOADJUSTMENT ist, dass Sie noch 4 Minuten warten müssen, bis Ihre Routine ausgeführt wird. Das heißt, Der Timer wurde angepasst, um zu ermöglichen, wie lange der Computer geschlafen hat. Wenn Sie FIRONOADJUSTMENT jedoch bestehen, wird Ihre Leerlaufroutine sofort ausgeführt, da mehr als 5 Minuten Echtzeit verstrichen sind.
  

