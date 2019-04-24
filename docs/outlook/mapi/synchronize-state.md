---
title: Status Synchronisieren
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7abbf049a848d417f640528e5030e37a954413e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349511"
---
# <a name="synchronize-state"></a>Status Synchronisieren

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Synchronisierungsstatus des Replikationsstatus Computers passiert. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Status-ID:  <br/> |**LR_SYNC** <br/> |
|Zugehörige Datenstruktur:  <br/> |**[SYNC](sync.md)** <br/> |
|Aus folgendem Zustand:  <br/> |[Zustand „Leerlauf“](idle-state.md) <br/> |
|Zu folgendem Status:  <br/> |[Download-Hierarchie Status](download-hierarchy-state.md), [Inhaltsstatus synchronisieren](synchronize-contents-state.md), Status der [Upload-Hierarchie](upload-hierarchy-state.md)oder Leerlaufstatus  <br/> |
   
> [!NOTE]
> Der Replikationsstatus Computer ist ein deterministischer Statuscomputer. Ein Client, der von einem Staat zu einem anderen abgeht, muss schließlich aus letzterem zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Status initiiert die Synchronisierung. Ein lokaler Speicher kann von hier zu einem Upload-oder Downloadstatus wechseln. Beispielsweise kann ein lokaler Speicher zum Upload-Hierarchie Status wechseln, um eine Ordnerhierarchie auf den Server hochzuladen, oder eine vollständige Synchronisierung durchführen, indem Sie zunächst die Hierarchie hochladen und dann die Hierarchie vom Server herunterladen.
  
Während dieses Status initialisiert Outlook die zugehörige **Synchronisierungs** Datenstruktur mit dem Pfad zum lokalen Speicher, sodass Outlook während anderer Statusänderungen sieht. 
  
Der Client legt die [in]-Mitglieder der **Synchronisierung**fest, die Outlook anweist, wie andere Zustände behandelt werden. Der Client kann beispielsweise *ulFlags* auf **UPS_UPLOAD_ONLY** und **UPS_THESE_FOLDERS** und *PEL* auf eine Liste von Eintrags Bezeichnern der Ordner festlegen, um Outlook mitzuteilen, dass nur diese Ordner hochgeladen werden. Wenn dieser Status endet, wird der lokale Speicher in den Leerlauf zurückgesetzt. 
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

