---
title: Synchronisierungsstatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 11d9b10c9872b7f6904cc9268f8954b9953462f7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578536"
---
# <a name="synchronize-state"></a>Synchronisierungsstatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Synchronisierungsstatus des Replikationsstatuscomputers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Statusbezeichner:  <br/> |**LR_SYNC** <br/> |
|Verwandte Datenstruktur:  <br/> |**[SYNC](sync.md)** <br/> |
|Aus diesem Zustand:  <br/> |[Zustand „Leerlauf“](idle-state.md) <br/> |
|In diesem Zustand:  <br/> |[Downloadhierarchiestatus,](download-hierarchy-state.md) [Synchronisieren des Inhaltsstatus,](synchronize-contents-state.md) [Uploadhierarchiestatus](upload-hierarchy-state.md)oder Leerlaufzustand  <br/> |
   
> [!NOTE]
> Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat. Ein Client, der von einem Bundesland in einen anderen wechselt, muss schließlich von letzterem zum ersten Zurückkehren zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Zustand initiiert die Synchronisierung. Ein lokaler Store kann von hier aus in einen Upload- oder Downloadstatus übergehen. Beispielsweise kann ein lokaler Speicher in den Uploadhierarchiestatus verschoben werden, um eine Ordnerhierarchie auf den Server hochzuladen, oder er kann eine vollständige Synchronisierung durchführen, indem er zuerst die Hierarchie hochlädt und dann die Hierarchie vom Server herunterlädt.
  
In diesem Zustand initialisiert Outlook die zugeordnete **SYNC-Datenstruktur** mit dem Pfad zum lokalen Speicher, sodass Outlook Änderungen während anderer Zustände sieht. 
  
Der Client legt die [in]-Elemente von **SYNC** fest, wodurch Outlook angewiesen wird, wie andere Zustände behandelt werden sollen. Beispielsweise kann der Client *ulFlags* auf **UPS_UPLOAD_ONLY** und **UPS_THESE_FOLDERS** festlegen und in eine Liste der Eintragsbezeichner der Ordner *wechseln,* um Outlook mitzuteilen, dass nur diese Ordner hochgeladen werden. Wenn dieser Zustand endet, wird der lokale Speicher in den Leerlaufzustand zurückgesetzt. 
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

