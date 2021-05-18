---
title: Hochladen Tabellenstatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a2a9b3f214c76b8ec965c84c4731e0dc57e83352
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405821"
---
# <a name="upload-table-state"></a>Hochladen Tabellenstatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Status der Uploadtabelle des Replikationsstatuscomputers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Statusbezeichner:  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |
|Verwandte Datenstruktur:  <br/> |**[UPTBL](uptbl.md)** <br/> |
|In diesem Zustand:  <br/> |[Synchronisieren des Inhaltszustands](synchronize-contents-state.md) <br/> |
|In diesem Zustand:  <br/> |[Hochladen Status der Nachricht,](upload-message-state.md) [Statusstatus zum](upload-delete-status-state.md)Hochladen des Löschstatus, [Statusstatus](upload-read-status-state.md)des Leseinhalts hochladen oder Inhaltsstatus synchronisieren  <br/> |
   
> [!NOTE]
> Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat. Ein Client, der von einem Zustand in einen anderen abt, muss schließlich zu dem ersten von letzterem zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Zustand initiiert das Hochladen des Inhalts eines Ordners, der in einem vorherigen Synchronisierungsinhaltsstatus angegeben wurde. Der Ordner kann ein E-Mail-, Kalender-, Kontakt-, Aufgaben-, Notizen- oder Journalordner sein. Während dieses Status erstellt Outlook eine Liste der Elemente, die hinzugefügt, geändert, verschoben, gelöscht oder als gelesen markiert wurden, und bereitet die entsprechenden internen Informationen für den entsprechenden Status der Uploadnachricht, den Status "Löschstatus hochladen" oder "Lesestatus hochladen" vor.
  
Wenn dieser Status endet, Outlook der Ordner als synchronisiert markiert, sodass der Inhalt erst wieder hochgeladen wird, wenn eine weitere Änderung vorgenommen wurde. Der lokale Speicher kehrt zum Status "Inhalt synchronisieren" zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

