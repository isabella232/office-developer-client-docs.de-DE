---
title: Hochladen Tabellenstatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e6946b80d57c4bcf4dc14e68cc0023574d884c46
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623936"
---
# <a name="upload-table-state"></a>Hochladen Tabellenstatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Uploadtabellenstatus des Replikationsstatuscomputers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Statusbezeichner:  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |
|Verwandte Datenstruktur:  <br/> |**[UPTBL](uptbl.md)** <br/> |
|Aus diesem Zustand:  <br/> |[Synchronisieren des Inhaltsstatus](synchronize-contents-state.md) <br/> |
|In diesem Zustand:  <br/> |[Hochladen Nachrichtenstatus,](upload-message-state.md)Status des [Löschstatus hochladen,](upload-delete-status-state.md)Status des [Lesestatus hochladen](upload-read-status-state.md)oder Inhaltsstatus synchronisieren  <br/> |
   
> [!NOTE]
> Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat. Ein Client, der von einem Bundesland in einen anderen wechselt, muss schließlich von letzterem zum ersten Zurückkehren zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Zustand initiiert das Hochladen des Inhalts eines Ordners, der in einem vorherigen Status für die Synchronisierung von Inhalten angegeben wurde. Der Ordner kann ein E-Mail-, Kalender-, Kontakte-, Aufgaben-, Notizen- oder Journalordner sein. In diesem Zustand erstellt Outlook eine Liste der Elemente, die hinzugefügt, geändert, verschoben, gelöscht oder als gelesen markiert wurden, und bereitet die entsprechenden internen Informationen für den entsprechenden Status der Uploadnachricht, den Status des Upload-Löschstatus oder den Status "Lesestatus hochladen" vor.
  
Wenn dieser Zustand endet, kennzeichnet Outlook den Ordner als synchronisierten Inhalt, sodass der Inhalt erst dann erneut hochgeladen wird, wenn eine weitere Änderung vorgenommen wird. Der lokale Speicher kehrt in den Zustand "Inhalt synchronisieren" zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

