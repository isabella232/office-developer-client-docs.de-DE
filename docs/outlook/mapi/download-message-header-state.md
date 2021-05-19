---
title: Nachrichtenkopfstatus herunterladen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c8e83119d724f583d40583a6a5227bc467dc94da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417119"
---
# <a name="download-message-header-state"></a>Nachrichtenkopfstatus herunterladen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Nachrichtenkopfstatus des Replikationsstatuscomputers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Statusbezeichner:  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |
|Verwandte Datenstruktur:  <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
|In diesem Zustand:  <br/> |[Zustand „Leerlauf“](idle-state.md) <br/> |
|In diesem Zustand:  <br/> |Zustand „Leerlauf“  <br/> |
   
> [!NOTE]
> Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat. Ein Client, der von einem Zustand in einen anderen abt, muss schließlich zu dem ersten von letzterem zurückkehren. 
  
## <a name="description"></a>Beschreibung

Während dieses Zustands aktualisiert der Client den Header einer Nachricht in einem lokalen Speicher. Der lokale Speicher tritt diesen Status bei **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** ein und wird beendet, wenn **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** aufgerufen wird. Während dieses Status initialisiert Outlook Elemente der zugeordneten **HDRSYNC-Datenstruktur** mit Informationen zum Kopf einer Nachricht. Der Client lädt zuerst das vollständige Nachrichtenelement vom Server herunter und aktualisiert dann die Kopfzeile des Nachrichtenelements lokal. 
  
Wenn die Syncrhonisierung endet, legt der Client die Downloadergebnisse fest. Der lokale Speicher kehrt in den Leerlaufzustand zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

