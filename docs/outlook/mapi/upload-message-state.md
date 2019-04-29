---
title: Nachrichtenstatus hochladen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 61cda23557a501a2651385d192f1dc7432ef1cb5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433801"
---
# <a name="upload-message-state"></a>Nachrichtenstatus hochladen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Upload-Nachrichtenstatus des Replikationsstatus Computers passiert. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Status-ID:  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |
|Zugehörige Datenstruktur:  <br/> |**[UPMSG](upmsg.md)** <br/> |
|Aus folgendem Zustand:  <br/> |[Tabellenstatus hochladen](upload-table-state.md) <br/> |
|Zu folgendem Status:  <br/> |Tabellenstatus hochladen  <br/> |
   
> [!NOTE]
> Der Replikationsstatus Computer ist ein deterministischer Statuscomputer. Ein Client, der von einem Staat zu einem anderen abgeht, muss schließlich aus letzterem zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Status initiiert das Hochladen eines Outlook-Elements (e-Mail, Kalender, Kontakt, Aufgabe, Notiz oder Journal), das neu ist oder in den aktuellen Ordner verschoben wurde oder geändert wurde. Outlook initialisiert die correpsonding **UPMSG** -Datenstruktur mit den entsprechenden Informationen für das Element als hinzugefügt, verschoben oder geändert. 
  
Wenn das Element hinzugefügt oder verschoben wurde, wird das Element vom Client entsprechend auf dem Server hinzugefügt oder aktualisiert. 
  
Wenn das Element geändert wurde, gibt Outlook weiter in der **UPMSG** -Datenstruktur an, ob sich die Änderungen in einem Nachrichtenkopf befinden (in diesem Fall ist das Element der Nachrichtenkopf), in den Elementeigenschaften oder im Element selbst, für das ein Konflikt erforderlich ist. Lösung. Der Client aktualisiert dann das Element auf dem Server. 
  
Wenn der Upload beendet ist, stellt Outlook fest, dass die Nachricht hochgeladen wurde, sodass Sie bei einem nachfolgenden Upload nicht verarbeitet wird. Der lokale Speicher gibt den Status der hochzuladenden Tabelle zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

