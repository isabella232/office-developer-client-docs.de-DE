---
title: Tabellenstatus hochladen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a2a9b3f214c76b8ec965c84c4731e0dc57e83352
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342840"
---
# <a name="upload-table-state"></a>Tabellenstatus hochladen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Upload-Tabellenstatus des Replikationsstatus Computers passiert. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Status-ID:  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |
|Zugehörige Datenstruktur:  <br/> |**[UPTBL](uptbl.md)** <br/> |
|Aus folgendem Zustand:  <br/> |[Synchronisieren des Inhaltsstatus](synchronize-contents-state.md) <br/> |
|Zu folgendem Status:  <br/> |[Nachrichtenstatus hochladen](upload-message-state.md), [Löschstatus](upload-delete-status-state.md)hochladen, Status [Lesen hochladen](upload-read-status-state.md)oder Inhaltsstatus synchronisieren  <br/> |
   
> [!NOTE]
> Der Replikationsstatus Computer ist ein deterministischer Statuscomputer. Ein Client, der von einem Staat zu einem anderen abgeht, muss schließlich aus letzterem zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Status initiiert das Hochladen des Inhalts eines Ordners, der in einem vorhergehenden Synchronisierungsstatus angegeben wurde. Der Ordner kann ein Mail-, Kalender-, Kontakt-, Aufgaben-, Notizen-oder Journalordner sein. Während dieses Zustands erstellt Outlook eine Liste von Elementen, die hinzugefügt, geändert, verschoben, gelöscht oder als gelesen markiert wurden, und bereitet die entsprechenden internen Informationen für den entsprechenden Upload-Status, den Zustand "Delete" oder "Lesestatus hochladen" vor. Staat.
  
Wenn dieser Status endet, markiert Outlook den Ordner als den Inhalt synchronisiert, sodass der Inhalt nicht erneut hochgeladen werden, bis eine andere Änderung vorgenommen wird. Der lokale Speicher gibt den Status "Inhalte synchronisieren" zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

