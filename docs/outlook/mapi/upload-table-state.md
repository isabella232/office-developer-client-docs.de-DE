---
title: Status „Uploadtabelle“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bd54c30e8701a13637235e28ddcfef4c21d10a2b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576981"
---
# <a name="upload-table-state"></a>Status „Uploadtabelle“

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was geschieht, während die Tabelle Zustand der Replikation Zustandsautomat hochladen. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|State-ID:  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |
|Verwandte-Datenstruktur:  <br/> |**[UPTBL](uptbl.md)** <br/> |
|Aus diesem Zustand:  <br/> |[Synchronisieren von Inhalt Zustand](synchronize-contents-state.md) <br/> |
|Diesen Status:  <br/> |[Nachrichtenstatus hochladen](upload-message-state.md), [Upload löschen Status Zustand](upload-delete-status-state.md), [Status Zustand lesen hochladen](upload-read-status-state.md), oder Inhalt Zustand synchronisieren  <br/> |
   
> [!NOTE]
> Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat. Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben. 
  
## <a name="description"></a>Beschreibung

Dieser Status wird initiiert, Hochladen den Inhalt eines Ordners, der in einem vorherigen synchronisieren Inhalt Zustand angegeben wurde. Der Ordner kann einen Ordner e-Mail, Kalender, Kontakte, Aufgaben, Notizen oder Journal sein. Während dieser Zustand Outlook erstellt eine Liste der Elemente, die hinzugefügt, geändert, verschoben, gelöscht, oder wurden als gelesen markiert und bereitet die entsprechende interne Informationen für den entsprechenden Upload Nachrichtenstatus, Upload löschen Status Zustand oder Status "gelesen" Hochladen Zustand.
  
Wenn dieser Status beendet wird, markiert Outlook den Ordner mit seinen Inhalt synchronisiert, sodass der Inhalt nicht erneut hochgeladen werden soll, bis eine andere Änderung vorgenommen wird. Auf den Synchronize Inhalt Status gibt der lokale Speicher zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCHRONISIERUNGSSTATUS](syncstate.md)

