---
title: Hochladen Statusstatus löschen
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
# <a name="upload-delete-status-state"></a>Hochladen Statusstatus löschen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Statusstatus zum Löschen des Uploads des Replikationsstatuscomputers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Statusbezeichner:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |
|Verwandte Datenstruktur:  <br/> |**[UPDEL](updel.md)** <br/> |
|In diesem Zustand:  <br/> |[Hochladen Tabellenstatus](upload-table-state.md) <br/> |
|In diesem Zustand:  <br/> |Hochladen Tabellenstatus  <br/> |
   
> [!NOTE]
> Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat. Ein Client, der von einem Zustand in einen anderen abt, muss schließlich zu dem ersten von letzterem zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Status initiiert die Aktualisierung auf einem Server, der Outlook Elemente (E-Mail, Kalender, Kontakt, Aufgabe, Notiz oder Journal) enthält, die in einem Ordner in einem lokalen Speicher gelöscht wurden, der in einem vorherigen Uploadtabelle-Status angegeben ist. Während dieses Status initialisiert Outlook Mitglieder in der zugeordneten **UPDEL-Datenstruktur** mit Informationen für die Elemente, die gelöscht oder aus dem Ordner verschoben wurden. 
  
Der Client löscht dann die angegebenen Elemente im Ordner auf dem Server. Um elemente zu unterscheiden, die verschoben wurden und nicht gelöscht wurden, muss der Client die  *pupmov-Mitglieder*  überprüfen, die in der **UPDEL-Struktur identifiziert** wurden. 
  
Wenn dieser Status endet, Outlook die internen Informationen gelöscht, die angeben, dass das Element gelöscht wurde. folglich Outlook nicht mehr über einen Datensatz des Elements verfügen. Der lokale Speicher kehrt zum Status der Uploadtabelle zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

