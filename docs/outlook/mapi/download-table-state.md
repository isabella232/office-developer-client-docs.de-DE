---
title: Tabellenstatus herunterladen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7451d159ef97ef9d8160b386ec5bf88fb388706e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338339"
---
# <a name="download-table-state"></a>Tabellenstatus herunterladen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Download-Tabellenstatus des Replikationsstatus Computers passiert. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Status-ID:  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |
|Zugehörige Datenstruktur:  <br/> |**[DNTBL](dntbl.md)** <br/> |
|Aus folgendem Zustand:  <br/> |[Synchronisieren des Inhaltsstatus](synchronize-contents-state.md) <br/> |
|Zu folgendem Status:  <br/> |Synchronisieren des Inhaltsstatus  <br/> |
   
> [!NOTE]
> Der Replikationsstatus Computer ist ein deterministischer Statuscomputer. Ein Client, der von einem Staat zu einem anderen abgeht, muss schließlich aus letzterem zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Status initiiert das Herunterladen eines Ordners. Während dieses Status initialisiert Outlook die zugeordnete **DNTBL** -Datenstruktur mit Informationen über den Ordner. Der Client downloadet den Ordnerinhalt und aktualisiert den Ordner im lokalen Speicher mit neuen Inhalten, Änderungen oder Löschungen vom Server. Der Downloadprozess übernimmt die Microsoft Exchange-inkrementelle Änderungs Synchronisierung (ICS). Weitere Informationen zu ICS finden Sie unter [ICS-Auswertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
Wenn dieser Status endet, gibt der lokale Speicher den Status Synchronize Content zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

