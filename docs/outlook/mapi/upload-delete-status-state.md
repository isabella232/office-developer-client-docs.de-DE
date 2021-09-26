---
title: Hochladen Statusstatus löschen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 165135869e42343a0ee0818908b98e9dce64a528
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629487"
---
# <a name="upload-delete-status-state"></a>Hochladen Statusstatus löschen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Status zum Löschen des Uploads des Replikationsstatuscomputers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Statusbezeichner:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |
|Verwandte Datenstruktur:  <br/> |**[UPDEL](updel.md)** <br/> |
|Aus diesem Zustand:  <br/> |[Hochladen Tabellenstatus](upload-table-state.md) <br/> |
|In diesem Zustand:  <br/> |Hochladen Tabellenstatus  <br/> |
   
> [!NOTE]
> Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat. Ein Client, der von einem Bundesland in einen anderen wechselt, muss schließlich von letzterem zum ersten Zurückkehren zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Status initiiert die Aktualisierung auf einem Server, die Outlook Elemente (E-Mail, Kalender, Kontakt, Aufgabe, Notiz oder Journal), die in einem Ordner in einem lokalen Speicher gelöscht wurden, der in einem vorherigen Uploadtabellenstatus angegeben wurde. In diesem Zustand initialisiert Outlook Elemente in der zugeordneten **UPDEL-Datenstruktur** mit Informationen zu den Elementen, die aus dem Ordner gelöscht oder verschoben wurden. 
  
Der Client löscht dann die angegebenen Elemente im Ordner auf dem Server. Um Elemente zu unterscheiden, die verschoben wurden und nicht gelöscht wurden, muss der Client die in der **UPDEL-Struktur** *identifizierten teammitglieder Elemente* überprüfen. 
  
Wenn dieser Zustand endet, löscht Outlook die internen Informationen, die angeben, dass das Element gelöscht wurde; daher verfügen Outlook nicht mehr über einen Datensatz des Elements. Der lokale Speicher kehrt zum Uploadtabellenstatus zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

