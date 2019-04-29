---
title: Status "Löschvorgang löschen"
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dda9d23a572446a5fa79a9500eb69558b6e0debd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425841"
---
# <a name="upload-delete-status-state"></a>Status "Löschvorgang löschen"

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Status Status des Replikats des Replikationsstatus geschehen soll. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Status-ID:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |
|Zugehörige Datenstruktur:  <br/> |**[UPDEL](updel.md)** <br/> |
|Aus folgendem Zustand:  <br/> |[Tabellenstatus hochladen](upload-table-state.md) <br/> |
|Zu folgendem Status:  <br/> |Tabellenstatus hochladen  <br/> |
   
> [!NOTE]
> Der Replikationsstatus Computer ist ein deterministischer Statuscomputer. Ein Client, der von einem Staat zu einem anderen abgeht, muss schließlich aus letzterem zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Status initiiert die Aktualisierung auf einem Server diese Outlook-Elemente (e-Mail, Kalender, Kontakt, Aufgabe, Notiz oder Journal), die in einem Ordner in einem lokalen Speicher gelöscht wurden, der in einem vorherigen Upload-Tabellenstatus angegeben wurde. Während dieses Status initialisiert Outlook Elemente in der zugeordneten **UPDEL** -Datenstruktur mit Informationen für die Elemente, die aus dem Ordner gelöscht oder verschoben wurden. 
  
Der Client löscht dann die angegebenen Elemente im Ordner auf dem Server. Um Elemente zu unterscheiden, die verschoben wurden, anstatt sie gelöscht zu haben, muss der Client die in der **UPDEL** -Struktur angegebenen *pupmov* -Elemente überprüfen. 
  
Wenn dieser Status endet, löscht Outlook die internen Informationen, die darauf hinweisen, dass das Element gelöscht wurde. Daher hat Outlook keinen Datensatz mehr für das Element. Der lokale Speicher gibt den Status der hochzuladenden Tabelle zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

