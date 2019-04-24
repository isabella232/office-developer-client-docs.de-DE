---
title: Nachrichtenkopf Status herunterladen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c8e83119d724f583d40583a6a5227bc467dc94da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338836"
---
# <a name="download-message-header-state"></a>Nachrichtenkopf Status herunterladen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Download Nachrichtenkopf Status des Replikationsstatus Computers passiert. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Status-ID:  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |
|Zugehörige Datenstruktur:  <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
|Aus folgendem Zustand:  <br/> |[Zustand „Leerlauf“](idle-state.md) <br/> |
|Zu folgendem Status:  <br/> |Zustand „Leerlauf“  <br/> |
   
> [!NOTE]
> Der Replikationsstatus Computer ist ein deterministischer Statuscomputer. Ein Client, der von einem Staat zu einem anderen abgeht, muss schließlich aus letzterem zurückkehren. 
  
## <a name="description"></a>Beschreibung

Während dieses Status aktualisiert der Client die Kopfzeile einer Nachricht in einem lokalen Speicher. Der lokale Speicher gibt diesen Status bei **[IOSTX:: SyncHdrBeg](iostx-synchdrbeg.md)** und Exits ein, wenn **[IOSTX:: SyncHdrEnd](iostx-synchdrend.md)** aufgerufen wird. Während dieses Status initialisiert Outlook Member der zugeordneten **HDRSYNC** -Datenstruktur mit Informationen über die Kopfzeile einer Nachricht. Der Client downloadet zunächst das vollständige Nachrichtenelement vom Server und aktualisiert dann die Kopfzeile des Nachrichtenelements lokal. 
  
Wenn Synchronisation endet, legt der Client die Download Ergebnisse fest. Der lokale Speicher wird in den Leerlauf zurückversetzt.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

