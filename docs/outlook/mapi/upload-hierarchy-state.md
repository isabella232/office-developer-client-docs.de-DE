---
title: Hochladen Hierarchiestatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f789f4d7bbaf585d0d80f2208c35313542dfc191
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415425"
---
# <a name="upload-hierarchy-state"></a>Hochladen Hierarchiestatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Uploadhierarchiestatus des Replikationsstatuscomputers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Statusbezeichner:  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |
|Verwandte Datenstruktur:  <br/> |**[UPHIER](uphier.md)** <br/> |
|In diesem Zustand:  <br/> |[Zustand „Synchronisieren“](synchronize-state.md) <br/> |
|In diesem Zustand:  <br/> |[Hochladen Ordnerstatus](upload-folder-state.md)oder Synchronisierungsstatus  <br/> |
   
> [!NOTE]
> Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat. Ein Client, der einen Zustand in einen anderen verlässt, muss schließlich zu dem ersten von letzterem zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Zustand initiiert das Hochladen einer Ordnerstrukturhierarchie, die in einem vorherigen Synchronisierungsstatus angegeben wurde. Outlook bestimmt die Anzahl der Ordner, die in dieser Hierarchie erstellt oder geändert wurden, und initialisiert *cEnt* in **UPHIER**. Outlook behält auch die Anzahl der hochgeladenen Ordner mit einem anderen Mitglied *iEnt bei.* Um jeden der  *cEnt-Ordner*  hochzuladen, verschiebt der Client den lokalen Speicher in den Uploadordnerstatus und kehrt zum Status der Uploadhierarchie zurück, wenn der Ordnerupload abgeschlossen ist. 
  
Wenn der Uploadhierarchiestatus endet, kehrt der lokale Speicher in den Synchronisierungsstatus zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

