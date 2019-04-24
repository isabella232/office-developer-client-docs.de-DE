---
title: Hierarchie Status hochladen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f789f4d7bbaf585d0d80f2208c35313542dfc191
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286315"
---
# <a name="upload-hierarchy-state"></a>Hierarchie Status hochladen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Upload-Hierarchie Status des Replikationsstatus Computers passiert. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Status-ID:  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |
|Zugehörige Datenstruktur:  <br/> |**[UPHIER](uphier.md)** <br/> |
|Aus folgendem Zustand:  <br/> |[Zustand „Synchronisieren“](synchronize-state.md) <br/> |
|Zu folgendem Status:  <br/> |[Ordner Status hochladen](upload-folder-state.md)oder Status Synchronisieren  <br/> |
   
> [!NOTE]
> Der Replikationsstatus Computer ist ein deterministischer Statuscomputer. Ein Client, der einen Status zu einem anderen abgibt, muss schließlich aus letzterem zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Status initiiert das Hochladen einer Ordnerstruktur Hierarchie, die in einem vorhergehenden Synchronisierungsstatus angegeben wurde. Outlook bestimmt die Anzahl der Ordner, die in dieser Hierarchie erstellt oder geändert wurden, und initialisiert *cEnt* in uphere. **** In Outlook wird auch die Anzahl der hochgeladenen Ordner mit einem anderen Mitglieds *iEnt* . Um jeden *cEnt* -Ordner hochzuladen, verschiebt der Client den lokalen Speicher in den Upload-Ordner Status und kehrt zum Upload-Hierarchie Status zurück, wenn der Ordner Upload abgeschlossen ist. 
  
Wenn der Upload-Hierarchie Status endet, wird der lokale Speicher zum Synchronize-Status zurückgegeben.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

