---
title: Status „Status der Upload-Löschung“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4a45cfafec5126c72f365858e41963bc95fa707a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574545"
---
# <a name="upload-delete-status-state"></a>Status „Status der Upload-Löschung“

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was geschieht, während der Upload löschen Status Zustand der Replikation Zustandsautomat. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|State-ID:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |
|Verwandte-Datenstruktur:  <br/> |**[UPDEL](updel.md)** <br/> |
|Aus diesem Zustand:  <br/> |[Tabelle Zustand hochladen](upload-table-state.md) <br/> |
|Diesen Status:  <br/> |Tabelle Zustand hochladen  <br/> |
   
> [!NOTE]
> Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat. Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben. 
  
## <a name="description"></a>Beschreibung

Dieser Status wird initiiert, auf einem Server aktualisieren, die Outlook-Elemente (e-Mail, Kalender, Kontakt, Aufgabe, Notiz oder Journal), die in einem Ordner in einem lokalen Speicher angegeben, die in den vorstehenden Upload-Tabelle gelöscht wurden. Während dieser Zustand initialisiert Outlook Elemente in der zugeordneten **UPDEL** Datenstruktur mit Informationen für die Elemente, die aus dem Ordner verschoben oder gelöscht wurden. 
  
Der Client löscht die angegebenen Elemente im Ordner auf dem Server. Um Elemente zu unterscheiden, die verschoben wurden, im Gegensatz zu müssen gelöscht wurden, muss der Client die *Pupmov* Member in der Struktur **UPDEL** identifiziert überprüfen. 
  
Wenn dieser Status beendet ist, löscht Outlook die interne Informationen zurück, der angibt, dass das Element gelöscht wurde. Daher müssen Outlook nicht mehr einen Datensatz des Elements. Auf den Upload Tabelle Status gibt der lokale Speicher zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCHRONISIERUNGSSTATUS](syncstate.md)

