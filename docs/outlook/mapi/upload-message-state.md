---
title: Status „Uploadnachricht“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 752756cbcf6c1ce487188dd4b9ba55eee6506cd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795804"
---
# <a name="upload-message-state"></a>Status „Uploadnachricht“

  
  
**Betrifft**: Outlook 
  
 In diesem Thema wird beschrieben, was geschieht, während die Nachrichtenstatus Hochladen von der Replikation Zustandsautomat. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|State-ID:  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |
|Verwandte-Datenstruktur:  <br/> |**[UPMSG](upmsg.md)** <br/> |
|Aus diesem Zustand:  <br/> |[Tabelle Zustand hochladen](upload-table-state.md) <br/> |
|Diesen Status:  <br/> |Tabelle Zustand hochladen  <br/> |
   
> [!NOTE]
> Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat. Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben. 
  
## <a name="description"></a>Beschreibung

Dieser Status wird initiiert, Hochladen ein Outlook-Element (e-Mail, Kalender, Kontakt, Aufgabe, Notiz oder Journal), die neu ist oder im aktuellen Ordner verschoben wurde oder geändert wurde. Outlook initialisiert die Correpsonding **UPMSG** -Datenstruktur durch die entsprechenden Informationen für das Element wie hinzugefügt, verschoben oder geändert wird. 
  
Wenn das Element hinzugefügt oder verschoben wurde, der Client dann entsprechend hinzugefügt oder das Element auf dem Server aktualisiert. 
  
Wenn das Element geändert wurde, gibt Outlook weiter in der Datenstruktur **UPMSG** , ob die Änderungen in einer e-Mail-Kopfzeile (in diesem Fall das Element der Nachrichtenkopf ist), die Elementeigenschaften oder das Element selbst, das Konflikt benötigt werden Auflösung. Der Client aktualisiert anschließend das Element auf dem Server. 
  
Wenn der Hochladevorgang Element endet, Notizen Outlook, dass die Nachricht hochgeladen wurde, damit es nicht in einer nachfolgenden Upload verarbeitet werden. Auf den Upload Tabelle Status gibt der lokale Speicher zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

