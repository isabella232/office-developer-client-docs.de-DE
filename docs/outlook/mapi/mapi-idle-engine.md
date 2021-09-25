---
title: MAPI Idle Engine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 755d096a-2a61-44d2-a765-5d464a857756
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c009efbd869b820c52aa2069e4420d473fecc3ee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561222"
---
# <a name="mapi-idle-engine"></a>MAPI Idle Engine

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI stellt mehrere Funktionen bereit, die gemeinsam als Leerlaufmodul bezeichnet werden. Mit diesen Funktionen können Clients, Adressbuchanbieter und Nachrichtenspeicheranbieter verschiedene Aufgaben in langsamen Zeiten in der Sitzung oder als Reaktion auf eine langsame Zeit ausführen. Beispielsweise können Clients und Dienstanbieter langsame Vorgänge zurückstellen oder Dateien schließen, die über einen längeren Zeitraum nicht verwendet wurden. Transportanbieter verwenden das Leerlaufmodul in der Regel nicht, da die **IXPLogon::Idle-Methode** ihren Platz einnimmt. Weitere Informationen finden Sie unter [IXPLogon::Idle](ixplogon-idle.md).
  
Um das Leerlaufmodul zu verwenden, erstellen Clients und Dienstanbieter eine Rückruffunktion, die die Aufgaben enthält, die ausgeführt werden sollen, wenn sich das MAPI-Subsystem im Leerlauf befindet. Wenn die MAPI Leerlaufzeit erkennt, wird diese Rückruffunktion aufgerufen. Die Rückruffunktion folgt dem **FNIDLE-Prototyp,** der wie folgt definiert ist: 
  
 `BOOL (STDAPICALLTYPE FNIDLE) (LPVOID lpvContext)`
  
Weitere Informationen finden Sie unter [FNIDLE](fnidle.md).
  
Die Funktionen, die das Leerlaufmodul bilden, sind:
  
[ChangeIdleRoutine](changeidleroutine.md)
  
[DeregisterIdleRoutine](deregisteridleroutine.md)
  
[EnableIdleRoutine](enableidleroutine.md)
  
[FtgRegisterIdleRoutine](ftgregisteridleroutine.md)
  
[MAPIDeInitIdle](mapideinitidle.md)
  
[MAPIInitIdle](mapiinitidle.md)
  
Um eine Rückruffunktion zu registrieren, rufen Clients und Dienstanbieter die **FtgRegisterIdleRoutine-Funktion auf.** Die Eingabeparameter umfassen eine optionale Priorität, einen Speicherblock, der als Eingabe an Ihre Rückruffunktion übergeben wird, eine zeitaufwendigere Verwendung in jeder geeigneten Weise und eine Reihe von Optionsflags. 
  
Clients und Dienstanbieter können eine Priorität im  _priIdle-Parameter_ angeben, der steuert, wie die Leerlauffunktion ausgeführt wird, oder Null angeben, wenn die Priorität kein Problem darstellt. Da negative Zahlen höhere Prioritäten als positive Zahlen oder Null darstellen, sollten Komprimierungs- und Suchvorgänge negativen Zahlen zugewiesen werden. Aufgaben, die einmal auftreten, sollten positive Zahlen zugewiesen werden. 
  
Zum Aufheben der Registrierung einer aktiven Rückruffunktion rufen Clients und Dienstanbieter die **DeregisterIdleRoutine-Funktion** auf. Da **DeregisterIdleRoutine** asynchron ausgeführt wird, kann die Rückruffunktion jederzeit während des Registrierungsaufrufs und möglicherweise auch nach der Rückgabe von **DeregisterIdleRoutine** aufgerufen werden. 
  
Um einige oder alle Merkmale einer Rückruffunktion zu ändern, rufen Clients und Dienstanbieter die **ChangeIdleRoutine-Funktion** auf. **ChangeIdleRoutine** nimmt Änderungen entsprechend der Festlegung des Flags-Parameters  _ircIdle_ vor. **ChangeIdleRoutine** kann die Funktion selbst, ihre Priorität, die Zeiteinstellung und den Eingabeparameter ändern. 
  
Die MAPI definiert den Leerlauf genauso wie das Betriebssystem, wenn das Betriebssystem über eine Definition verfügt. In Win32 erstellt MAPI einen Thread mit Leerlaufklassenpriorität, um Leerlaufaufgaben zu planen. Dieser Thread verfolgt die Zeit und sendet eine Nachricht an den Thread, der die Leerlaufaufgabe ausführt, wenn die Zeit für die Ausführung eingeht. Win32 plant Threads, keine Prozesse. Wenn Vorgänge, deren Priorität höher als die Leerlaufpriorität ist, auf der Arbeitsstation ausgeführt werden, sollte der Leerlaufvorgang erst nach Abschluss der Aufgaben ausgeführt werden. 
  
Alle Leerlaufaufgaben werden in dem Thread ausgeführt, der **MAPIInitIdle** aufgerufen hat. Die MAPI verfügt über einen separaten Thread für die Planung, aber wenn ein Leerlaufvorgang berechtigt wird, wird eine Nachricht zurück an den Initialisierungsthread gesendet, und die Leerlaufaufgabe wird dort ausgeführt. Die Auswirkungen auf verschiedene Arten von Clients sind wie folgt.
  
|**Threadingmodell**|**Auswirkung**|
|:-----|:-----|
|Singlethread  <br/> |Kein Problem. Leerlauffunktionen werden im Hauptthread Des Clients ausgeführt und über die Nachrichtenschleife serialisiert.  <br/> |
|Freethreading  <br/> |Leerlauffunktionen müssen threadsicher sein, ihr Client verfügt jedoch bereits über die erforderliche Infrastruktur. Ihr Client benötigt möglicherweise überhaupt nicht das MAPI-Leerlaufmodul.  <br/> |
|Apartmentthread  <br/> |Die Leerlauffunktion muss in demselben Thread ausgeführt werden, der sie registriert hat, wenn sie MAPI, OLE oder andere COM-Schnittstellen verwenden möchte. Die einfachste Möglichkeit besteht darin, eine Leerlauffunktion mit MAPI zu registrieren, die eine Nachricht an den richtigen Thread sendet und die "echte" Leerlauffunktion direkt aus der Nachrichtenschleife dieses Threads weiterleitet.  <br/> |
   

