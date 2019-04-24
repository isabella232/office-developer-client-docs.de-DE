---
title: Status Status des Uploads
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e8ad2acf019df3f07060c8e8c71a62afd3fca03c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282663"
---
# <a name="upload-read-status-state"></a>Status Status des Uploads

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Status Status des Replikats beim Hochladen des Computers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Status-ID:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |
|Zugehörige Datenstruktur:  <br/> |**[UPREAD](upread.md)** <br/> |
|Aus folgendem Zustand:  <br/> |[Tabellenstatus hochladen](upload-table-state.md) <br/> |
|Zu folgendem Status:  <br/> |Tabellenstatus hochladen  <br/> |
   
> [!NOTE]
> Der Replikationsstatus Computer ist ein deterministischer Statuscomputer. Ein Client, der von einem Staat zu einem anderen abgeht, muss schließlich aus letzterem zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Status initiiert das Hochladen des Lesestatus von Elementen in einem Ordner, der in einem vorherigen Upload-Tabellenstatus angegeben ist. Während dieses Status initialisiert Outlook die zugehörige **upread** -Datenstruktur mit Informationen für die Elemente im Ordner, deren Lesestatus geändert wurde. Der Client aktualisiert dann den Lesestatus dieser Elemente auf dem Server als gelesen oder ungelesen. 
  
Wenn dieser Status endet, werden die internen Informationen zum Lesestatus des Elements gelöscht, und es wird verhindert, dass der Lesestatus des Elements erneut hochgeladen wird. Der lokale Speicher gibt den Status der hochzuladenden Tabelle zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

