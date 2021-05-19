---
title: Hochladen Nachrichtenstatus
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
# <a name="upload-message-state"></a>Hochladen Nachrichtenstatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Status der Uploadnachricht des Replikationsstatuscomputers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Statusbezeichner:  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |
|Verwandte Datenstruktur:  <br/> |**[UPMSG](upmsg.md)** <br/> |
|In diesem Zustand:  <br/> |[Hochladen Tabellenstatus](upload-table-state.md) <br/> |
|In diesem Zustand:  <br/> |Hochladen Tabellenstatus  <br/> |
   
> [!NOTE]
> Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat. Ein Client, der von einem Zustand in einen anderen abt, muss schließlich zu dem ersten von letzterem zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Status initiiert das Hochladen eines Outlook -Elements (E-Mail, Kalender, Kontakt, Aufgabe, Notiz oder Journal), das neu ist oder in den aktuellen Ordner verschoben wurde oder geändert wurde. Outlook initialisiert die korrelierende **UPMSG-Datenstruktur** mit den entsprechenden Informationen für das Element als hinzugefügt, verschoben oder geändert. 
  
Wenn das Element hinzugefügt oder verschoben wurde, fügt der Client das Element auf dem Server entsprechend hinzu oder aktualisiert es. 
  
Wenn das Element geändert wurde, gibt Outlook in der **UPMSG-Datenstruktur** weiter an, ob sich die Änderungen in einem Nachrichtenkopf (in diesem Fall ist das Element der Nachrichtenkopf), in den Elementeigenschaften oder im Element selbst befinden, das eine Konfliktauflösung erfordert. Der Client aktualisiert dann das Element auf dem Server. 
  
Wenn der Elementupload endet, Outlook, dass die Nachricht hochgeladen wurde, sodass sie nicht in einem nachfolgenden Upload verarbeitet wird. Der lokale Speicher kehrt zum Status der Uploadtabelle zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

