---
title: MAPI Idle Engine
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
# <a name="mapi-idle-engine"></a>MAPI Idle Engine

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI bietet mehrere Funktionen, die gemeinsam als Leerlaufmodul bezeichnet werden. Mit diesen Funktionen können Clients, Adressbuchanbieter und Nachrichtenspeicheranbieter verschiedene Aufgaben in langsamen Zeiten in der Sitzung oder als Reaktion auf eine langsame Zeit ausführen. Clients und Dienstanbieter können z. B. langsame Vorgänge zurückdingen oder Dateien schließen, die für einen längeren Zeitraum nicht verwendet wurden. Transportanbieter verwenden in der Regel nicht das Leerlaufmodul, da die **IXPLogon::Idle-Methode** ihren Platz einnimmt. Weitere Informationen finden Sie unter [IXPLogon::Idle](ixplogon-idle.md).
  
Um das Leerlaufmodul zu verwenden, erstellen Clients und Dienstanbieter eine Rückruffunktion, die die Aufgaben enthält, die auftreten sollten, wenn sich das MAPI-Subsystem im Leerlauf befindet. Wenn MAPI Leerlaufzeit erkennt, wird diese Rückruffunktion aufgerufen. Die Rückruffunktion folgt dem **FNIDLE-Prototyp,** der wie folgt definiert ist: 
  
 `BOOL (STDAPICALLTYPE FNIDLE) (LPVOID lpvContext)`
  
Weitere Informationen finden Sie unter [FNIDLE](fnidle.md).
  
Die Funktionen des Leerlaufmoduls sind:
  
[ChangeIdleRoutine](changeidleroutine.md)
  
[DeregisterIdleRoutine](deregisteridleroutine.md)
  
[EnableIdleRoutine](enableidleroutine.md)
  
[FtgRegisterIdleRoutine](ftgregisteridleroutine.md)
  
[MAPIDeInitIdle](mapideinitidle.md)
  
[MAPIInitIdle](mapiinitidle.md)
  
Um eine Rückruffunktion zu registrieren, rufen Clients und Dienstanbieter die **FtgRegisterIdleRoutine-Funktion** auf. Die Eingabeparameter umfassen eine optionale Priorität, einen Speicherblock, der an Ihre Rückruffunktion als Eingabe übergeben wird, einen Zeitraum, der in irgendeiner Weise verwendet werden muss, und eine Reihe von Optionskennzeichen. 
  
Clients und Dienstanbieter können eine Priorität im  _priIdle-Parameter_ angeben, der steuert, wie die Leerlauffunktion ausgeführt wird, oder Null angeben, wenn die Priorität kein Problem ist. Da negative Zahlen höhere Prioritäten als positive Zahlen oder Null darstellen, sollten Komprimierungs- und Suchvorgängen negative Zahlen zugewiesen werden. Vorgängen, die einmal auftreten, sollten positive Zahlen zugewiesen werden. 
  
Zum Aufheben der Registrierung einer aktiven Rückruffunktion rufen Clients und Dienstanbieter die **DeregisterIdleRoutine-Funktion** auf. Da **DeregisterIdleRoutine** asynchron funktioniert, kann die Rückruffunktion jederzeit während des Registrierungsaufrufs und möglicherweise auch nach der **DeregisterIdleRoutine** aufgerufen werden. 
  
Um einige oder alle Merkmale einer Rückruffunktion zu ändern, rufen Clients und Dienstanbieter die **ChangeIdleRoutine-Funktion** auf. **ChangeIdleRoutine** nimmt Änderungen an der Einstellung des flags-Parameters  _"ircIdle"_ vor. **ChangeIdleRoutine** kann die Funktion selbst, ihre Priorität, Die Zeiteinstellung und den Eingabeparameter ändern. 
  
MAPI definiert leerlauf wie das Betriebssystem, wenn das Betriebssystem über eine Definition verfügt. In Win32 erstellt MAPI einen Thread mit Der Priorität der Leerlaufklasse, um Aufgaben im Leerlauf zu planen. Dieser Thread verfolgt die Uhrzeit und postet eine Nachricht an den Thread, der die Leerlaufaufgabe ausführen soll, wenn der Zeitpunkt für die Ausführung eintrifft. Win32 plant Threads, nicht Prozesse. Wenn Vorgänge mit einer Höheren Priorität als die Leerlaufpriorität auf der Arbeitsstation ausgeführt werden, sollte die Leerlaufaufgabe erst nach Abschluss der Vorgänge für die Ausführung geplant werden. 
  
Alle Leerlaufaufgaben werden im Thread ausgeführt, der **MAPIInitIdle aufgerufen hat.** MAPI verfügt über einen separaten Thread für die Planung, aber wenn eine Leerlaufaufgabe berechtigt wird, wird eine Nachricht zurück an den Initialisierungsthread gesendet, und die Leerlaufaufgabe wird dort ausgeführt. Die Auswirkungen auf unterschiedliche Typen von Clients sind wie folgt:
  
|**Threadmodell**|**Implikationen**|
|:-----|:-----|
|Singlethreading  <br/> |Kein Problem. Leerlauffunktionen werden im Hauptthread Ihres Clients ausgeführt und über die Nachrichtenschleife serialisiert.  <br/> |
|Freethreading  <br/> |Leerlauffunktionen müssen threadsicher sein, aber Ihr Client verfügt bereits über die erforderliche Infrastruktur. Ihr Client benötigt möglicherweise das MAPI-Leerlaufmodul überhaupt nicht.  <br/> |
|Apartmentthreading  <br/> |Die Idle-Funktion muss für denselben Thread ausgeführt werden, der sie registriert hat, wenn sie MAPI, OLE oder andere COM-Schnittstellen verwenden möchte. Die unkomplizierteste Möglichkeit besteht in der Registrierung einer Leerlauffunktion bei MAPI, die eine Nachricht an den richtigen Thread postet und die "echte" Leerlauffunktion direkt aus der Nachrichtenschleife dieses Threads zurücksennen.  <br/> |
   

