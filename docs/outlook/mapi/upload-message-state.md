---
title: Hochladen Nachrichtenstatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f8ab2d0326e8948cb27f67376238caff50935ba2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578410"
---
# <a name="upload-message-state"></a>Hochladen Nachrichtenstatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Uploadnachrichtenstatus des Replikationsstatuscomputers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Statusbezeichner:  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |
|Verwandte Datenstruktur:  <br/> |**[UPMSG](upmsg.md)** <br/> |
|Aus diesem Zustand:  <br/> |[Hochladen Tabellenstatus](upload-table-state.md) <br/> |
|In diesem Zustand:  <br/> |Hochladen Tabellenstatus  <br/> |
   
> [!NOTE]
> Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat. Ein Client, der von einem Bundesland in einen anderen wechselt, muss schließlich von letzterem zum ersten Zurückkehren zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Status initiiert das Hochladen eines Outlook Elements (E-Mail, Kalender, Kontakt, Aufgabe, Notiz oder Journal), das neu ist oder in den aktuellen Ordner verschoben oder geändert wurde. Outlook initialisiert die korrepsonierende **UPMSG-Datenstruktur** mit den entsprechenden Informationen für das Element, das hinzugefügt, verschoben oder geändert wird. 
  
Wenn das Element hinzugefügt oder verschoben wurde, fügt der Client das Element auf dem Server entsprechend hinzu oder aktualisiert es. 
  
Wenn das Element geändert wurde, gibt Outlook in der **UPMSG-Datenstruktur** weiter an, ob sich die Änderungen in einem Nachrichtenkopf befinden (in diesem Fall ist das Element der Nachrichtenkopf), in den Elementeigenschaften oder im Element selbst, das eine Konfliktbehebung erfordert. Der Client aktualisiert dann das Element auf dem Server. 
  
Wenn der Elementupload endet, Outlook notizen, dass die Nachricht hochgeladen wurde, sodass sie nicht in einem nachfolgenden Upload verarbeitet wird. Der lokale Speicher kehrt zum Uploadtabellenstatus zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

