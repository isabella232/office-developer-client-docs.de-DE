---
title: MAPI-Leerlauf Modul
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 755d096a-2a61-44d2-a765-5d464a857756
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d8d591c02bb621c16a1d1b46272b19573ea79785
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428452"
---
# <a name="mapi-idle-engine"></a>MAPI-Leerlauf Modul

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI bietet mehrere Funktionen, die gemeinsam als Leerlauf Modul bezeichnet werden. Diese Funktionen ermöglichen es Clients, Adressbuch Anbietern und Nachrichtenspeicher Anbietern, verschiedene Aufgaben in langsamen Zeiten in der Sitzung oder als Antwort auf eine langsame Zeit auszuführen. So können Clients und Dienstanbieter beispielsweise langsame Vorgänge zurückstellen oder Dateien, die für einen längeren Zeitraum nicht verwendet wurden, beenden. Transport Anbieter verwenden normalerweise das Leerlauf Modul nicht, da die **IXPLogon:: idle** -Methode ihren Platz einnimmt. Weitere Informationen finden Sie unter [IXPLogon:: idle](ixplogon-idle.md).
  
Um das Leerlauf Modul zu verwenden, erstellen Clients und Dienstanbieter eine Rückruffunktion, die die Aufgaben enthält, die auftreten sollten, wenn das MAPI-Subsystem inaktiv ist. Wenn MAPI die Leerlaufzeit erkennt, wird diese Rückruffunktion aufgerufen. Die Callback-Funktion folgt dem **FNIDLE** -Prototyp, wie folgt definiert: 
  
 `BOOL (STDAPICALLTYPE FNIDLE) (LPVOID lpvContext)`
  
Weitere Informationen finden Sie unter [FNIDLE](fnidle.md).
  
Die Funktionen, aus denen das Leerlauf Modul besteht, sind:
  
[ChangeIdleRoutine](changeidleroutine.md)
  
[DeregisterIdleRoutine](deregisteridleroutine.md)
  
[EnableIdleRoutine](enableidleroutine.md)
  
[FtgRegisterIdleRoutine](ftgregisteridleroutine.md)
  
[MAPIDeInitIdle](mapideinitidle.md)
  
[MAPIInitIdle](mapiinitidle.md)
  
Um eine Rückruffunktion zu registrieren, rufen Clients und Dienstanbieter die **FtgRegisterIdleRoutine** -Funktion auf. Zu den Eingabeparametern gehört eine optionale Priorität, ein Speicherblock, der als Eingabe an die Rückruffunktion übergeben wird, eine Zeitdauer, die in beliebiger Weise verwendet werden soll, und eine Reihe von Options-Flags. 
  
Clients und Dienstanbieter können eine Priorität im _priIdle_ -Parameter angeben, der steuert, wie die Leerlauf Funktion ausgeführt wird, oder NULL angeben, wenn die Priorität kein Problem darstellt. Da negative Zahlen höhere Prioritäten als positive Zahlen oder NULL darstellen, sollten Komprimierung und Suchvorgänge negative Zahlen erhalten. Für Vorgänge, die einmal auftreten, sollten positive Zahlen zugewiesen werden. 
  
Zum Aufheben der Registrierung einer aktiven Rückruffunktion rufen Clients und Dienstanbieter die **DeregisterIdleRoutine** -Funktion auf. Da **DeregisterIdleRoutine** asynchron arbeitet, ist es möglich, dass die Rückruffunktion jederzeit während des Deregistrierungs Aufrufs und möglicherweise auch nach dem zurückGeben von **DeregisterIdleRoutine** aufgerufen wird. 
  
Um einige oder alle Merkmale einer Rückruffunktion zu ändern, rufen Clients und Dienstanbieter die **ChangeIdleRoutine** -Funktion auf. **ChangeIdleRoutine** ändert entsprechend der Festlegung des flags-Parameters _ircIdle_ ; **ChangeIdleRoutine** kann die Funktion selbst, die Priorität, die Uhrzeiteinstellung und den Eingabeparameter ändern. 
  
MAPI definiert Leerlauf mit dem Betriebssystem, wenn das Betriebssystem eine Definition aufweist. Auf Win32 erstellt MAPI einen Thread mit Leerlaufpriorität, um Leerlauf Vorgänge zu planen. Dieser Thread verfolgt die Zeit und sendet eine Nachricht an den Thread, der die Leerlauf Aufgabe ausführt, wenn der Zeitpunkt für die Ausführung ankommt. Win32 plant Threads, nicht Prozesse. Wenn auf der Arbeitsstation Aufgaben mit einer höheren Priorität als der Leerlaufpriorität ausgeführt werden, sollte die Leerlauf Aufgabe erst ausgeführt werden, wenn die Aufgaben abgeschlossen sind. 
  
Alle Leerlaufaufgaben werden im Thread ausgeführt, der **MAPIInitIdle**aufgerufen hat. MAPI hat einen separaten Thread für die Planung, aber wenn eine Leerlauf Aufgabe berechtigt wird, sendet Sie eine Nachricht zurück in den Initialisierungsthread und die Leerlauf Aufgabe wird dort ausgeführt. Die Auswirkungen auf unterschiedliche Clienttypen lauten wie folgt:
  
|**Threadingmodell**|**Implikation**|
|:-----|:-----|
|Single Threaded  <br/> |Kein Problem. Leerlauf Funktionen werden im Hauptthread des Clients ausgeführt und werden über die Nachrichtenschleife serialisiert.  <br/> |
|Free-Threaded  <br/> |Leerlauf Funktionen müssen threadsicher sein, aber Ihr Client verfügt bereits über die erforderliche Infrastruktur. Möglicherweise benötigt Ihr Client nicht das MAPI-Leerlauf Modul.  <br/> |
|Apartment-Threaded  <br/> |Die Leerlauf Funktion muss im selben Thread ausgeführt werden, der Sie registriert hat, wenn Sie MAPI, OLE oder andere COM-Schnittstellen verwenden möchte. Die einfachste Möglichkeit besteht darin, eine Leerlauf Funktion mit MAPI zu registrieren, die eine Nachricht an den richtigen Thread sendet und die "Real"-Leerlauf Funktion direkt aus der Nachrichtenschleife dieses Threads ausgibt.  <br/> |
   

