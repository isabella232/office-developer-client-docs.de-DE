---
title: Status der Nachrichtenkopfzeile herunterladen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 27f9290c7a1059d66cfb7eda53bb9a3143c04611
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630971"
---
# <a name="download-message-header-state"></a>Status der Nachrichtenkopfzeile herunterladen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Headerstatus der Downloadnachricht des Replikationsstatuscomputers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Statusbezeichner:  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |
|Verwandte Datenstruktur:  <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
|Aus diesem Zustand:  <br/> |[Zustand „Leerlauf“](idle-state.md) <br/> |
|In diesem Zustand:  <br/> |Zustand „Leerlauf“  <br/> |
   
> [!NOTE]
> Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat. Ein Client, der von einem Bundesland in einen anderen wechselt, muss schließlich von letzterem zum ersten Zurückkehren zurückkehren. 
  
## <a name="description"></a>Beschreibung

In diesem Zustand aktualisiert der Client den Header einer Nachricht in einem lokalen Speicher. Der lokale Speicher wechselt bei **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** in diesen Zustand und wird beendet, wenn **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** aufgerufen wird. In diesem Zustand initialisiert Outlook Elemente der zugeordneten **HDRSYNC-Datenstruktur** mit Informationen zum Header einer Nachricht. Der Client lädt zuerst das vollständige Nachrichtenelement vom Server herunter und aktualisiert dann den Header des Nachrichtenelements lokal. 
  
Wenn die Synchronisierung beendet ist, legt der Client die Downloadergebnisse fest. Der lokale Speicher kehrt in den Leerlaufzustand zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

