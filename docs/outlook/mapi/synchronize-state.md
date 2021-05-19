---
title: Synchronisierungsstatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7abbf049a848d417f640528e5030e37a954413e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414627"
---
# <a name="synchronize-state"></a>Synchronisierungsstatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Synchronisierungsstatus des Replikationsstatuscomputers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Statusbezeichner:  <br/> |**LR_SYNC** <br/> |
|Verwandte Datenstruktur:  <br/> |**[SYNC](sync.md)** <br/> |
|In diesem Zustand:  <br/> |[Zustand „Leerlauf“](idle-state.md) <br/> |
|In diesem Zustand:  <br/> |[Downloadhierarchiestatus,](download-hierarchy-state.md) [Inhaltsstatus synchronisieren,](synchronize-contents-state.md) [Uploadhierarchiestatus](upload-hierarchy-state.md)oder Leerlaufzustand  <br/> |
   
> [!NOTE]
> Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat. Ein Client, der von einem Zustand in einen anderen abt, muss schließlich zu dem ersten von letzterem zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Zustand initiiert die Synchronisierung. Ein lokaler Speicher kann von hier aus zu einem Upload- oder Downloadstatus überwechseln. Beispielsweise kann ein lokaler Speicher in den Uploadhierarchiestatus wechseln, um eine Ordnerhierarchie auf den Server hochzuladen, oder er kann eine vollständige Synchronisierung durchführen, indem er zuerst die Hierarchie hoch- und dann die Hierarchie vom Server herunterloaden.
  
Während dieses Status initialisiert Outlook die  zugeordnete SYNC-Datenstruktur mit dem Pfad zum lokalen Speicher, sodass Outlook änderungen während anderer Zustände sehen. 
  
Der Client legt die [in]-Mitglieder von **SYNC** fest, die Outlook wie andere Zustände zu behandeln sind. Beispielsweise kann der Client *ulFlags* auf **UPS_UPLOAD_ONLY** und **UPS_THESE_FOLDERS** und *pel* auf eine Liste der Eintragsbezeichner der Ordner festlegen, um Outlook zu informieren, dass nur diese Ordner hochgeladen werden. Wenn dieser Zustand endet, wird der lokale Speicher in den Leerlaufzustand zurückgesetzt. 
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

