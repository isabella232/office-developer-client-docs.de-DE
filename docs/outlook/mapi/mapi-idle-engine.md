---
title: Im Leerlauf MAPI-Modul
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 755d096a-2a61-44d2-a765-5d464a857756
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c535da245be09f930a70c5fae2a892f33087ebf9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793007"
---
# <a name="mapi-idle-engine"></a>Im Leerlauf MAPI-Modul

  
  
**Betrifft**: Outlook 
  
MAPI bietet verschiedene Funktionen, die allgemein als im Leerlauf Engine bezeichnet werden. Diese Funktionen ermöglichen Clients, adressbuchanbietern implementierte und Message-Anbieter für verschiedene Aufgaben langsame Zeiten in der Sitzung oder als Reaktion auf einen Zeitpunkt langsam. Beispielsweise können Clients und Dienstanbieter langsame Vorgänge zurückgestellt oder schließen Sie Dateien, die für einen längeren Zeitraum nicht verwendete befunden hat. Transportanbieter in der Regel verwenden das Modul im Leerlauf Sie nicht, da die **IXPLogon::Idle** -Methode die stattfindet. Weitere Informationen finden Sie unter [IXPLogon::Idle](ixplogon-idle.md).
  
Erstellen Sie für die Verwendung des Moduls im Leerlauf Clients und -Dienstanbieter eine Rückruffunktion, die die Aufgaben, die ausgeführt werden soll enthält, wenn das MAPI-Subsystem im Leerlauf befindet. Wenn MAPI Leerlaufzeit erkennt, wird diese Callback-Funktion aufgerufen. Die Callback-Funktion: **FNIDLE** Prototyp wie folgt definiert 
  
 `BOOL (STDAPICALLTYPE FNIDLE) (LPVOID lpvContext)`
  
Weitere Informationen finden Sie unter [FNIDLE](fnidle.md).
  
Die Funktionen, die das Modul im Leerlauf bilden sind:
  
[ChangeIdleRoutine](changeidleroutine.md)
  
[DeregisterIdleRoutine](deregisteridleroutine.md)
  
[EnableIdleRoutine](enableidleroutine.md)
  
[FtgRegisterIdleRoutine](ftgregisteridleroutine.md)
  
[MAPIDeInitIdle](mapideinitidle.md)
  
[MAPIInitIdle](mapiinitidle.md)
  
Um eine Callback-Funktion zu registrieren, rufen Sie Clients und -Dienstanbieter die **FtgRegisterIdleRoutine** -Funktion. Die Eingabeparametern umfassen eine optionale Priorität, einen Block von Arbeitsspeicher, die an die Rückruffunktion übergeben wird, als Eingabe, eine bestimmte Zeitspanne keinerlei gegebenenfalls verwendet werden, und eine Reihe von Option Kennzeichen. 
  
Clients und Dienstanbieter können Geben Sie eine Priorität in der _PriIdle_ -Parameter, der steuert, wie die im Leerlauf-Funktion ausgeführt wird oder 0 (null) angeben, wenn die Priorität kein Belang ist. Da negative Zahlen einer höheren Priorität als positive Zahlen oder NULL darstellen, sollte Komprimierung und Suche Vorgänge negative Zahlen zugewiesen werden. Aufgaben, bei denen auf einmalige positive Zahlen zugewiesen werden soll. 
  
Rufen zum Aufheben der Registrierung für einer aktive Callback-Funktion, Clients und -Dienstanbieter die **DeregisterIdleRoutine** -Funktion. Da **DeregisterIdleRoutine** asynchron ausgeführt wird, ist es möglich, dass der Callback-Funktion können Sie jederzeit während des Anrufs Registrierung aufheben aufgerufen werden und möglicherweise sogar, nachdem **DeregisterIdleRoutine** zurückgegeben hat. 
  
Um einige oder alle der Merkmale der Callback-Funktion zu ändern, rufen Sie Clients und -Dienstanbieter die **ChangeIdleRoutine** -Funktion. **ChangeIdleRoutine** wird, ändert sich entsprechend der Flags-Parameter _IrcIdle_ wie festgelegt wird. **ChangeIdleRoutine** können die Funktion selbst, dessen Priorität, die Einstellung und input-Parameter ändern. 
  
MAPI im Leerlauf definiert die gleiche wie das Betriebssystem, wenn das Betriebssystem eine Definition hat. Unter Win32 erstellt MAPI einen Thread mit Priorität Leerlauf--Klasse im Leerlauf Aufgaben zu planen. Dieser Thread verfolgt die Uhrzeit und sendet eine Nachricht an den Thread, der der Leerlauf-Task ausgeführt werden soll, wenn die Zeit für die Ausführung eingeht. Win32 plant Threads, nicht verarbeitet. Wenn Aufgaben, bei die eine höhere Priorität als im Leerlauf Priorität haben auf der Arbeitsstation auftreten werden, sollte der im Leerlauf Vorgang nicht für die Ausführung geplant erhalten möchten, bis die Aufgaben abgeschlossen haben. 
  
Führen Sie alle Aufgaben im Leerlauf auf der Thread, **MAPIInitIdle**aufgerufen. MAPI verfügt über einen separaten Thread für die Planung, aber sobald ein Vorgang im Leerlauf berechtigt ist, sendet eine Meldung über den Initialisierung Thread und der Leerlauf-Task es ausgeführt wird. Die Konsequenzen für die verschiedenen Typen von Clients sind zulässig.
  
|**Threading-Modell**|**Implikation**|
|:-----|:-----|
|Single Threading-  <br/> |Kein Problem. Im Leerlauf Funktionen auf Ihrem Client Hauptthread ausführen und Schleife Nachricht serialisiert werden.  <br/> |
|Freethreadanbieter  <br/> |Im Leerlauf Funktionen muss threadsicheren, aber der Empfänger die notwendige Infrastruktur bereits verfügt. Das MAPI-Modul im Leerlauf möglicherweise nicht in allen Ihrer Client erforderlich.  <br/> |
|Des Apartmentthreading Thread-  <br/> |Im Leerlauf-Funktion hat, auf dem gleichen Thread auszuführen, die sie registriert, wenn sie MAPI oder OLE-COM-Schnittstellen verwenden möchte. Am einfachsten ist eine Funktion im Leerlauf MAPI, die eine Nachricht an den richtigen Thread bereitstellt registriert werden und die Funktion "real" im Leerlauf direkt aus diesem Thread Nachrichtenschleife versenden.  <br/> |
   

