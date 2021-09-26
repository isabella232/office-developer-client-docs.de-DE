---
title: Hochladen Status lesen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1dc04a72c0eb904f97d18019aec41f5ed3d66e4b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619547"
---
# <a name="upload-read-status-state"></a>Hochladen Status lesen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Uploadlesestatus des Replikationsstatuscomputers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Statusbezeichner:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |
|Verwandte Datenstruktur:  <br/> |**[UPREAD](upread.md)** <br/> |
|Aus diesem Zustand:  <br/> |[Hochladen Tabellenstatus](upload-table-state.md) <br/> |
|In diesem Zustand:  <br/> |Hochladen Tabellenstatus  <br/> |
   
> [!NOTE]
> Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat. Ein Client, der von einem Bundesland in einen anderen wechselt, muss schließlich von letzterem zum ersten Zurückkehren zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Zustand initiiert das Hochladen des Lesestatus von Elementen in einem Ordner, der in einem vorherigen Uploadtabellenstatus angegeben wurde. In diesem Zustand initialisiert Outlook die zugeordnete **UPREAD-Datenstruktur** mit Informationen für die Elemente in dem Ordner, dessen Lesestatus geändert wurde. Der Client aktualisiert dann den Lesestatus dieser Elemente auf dem Server als gelesen oder ungelesen. 
  
Wenn dieser Zustand endet, löscht Outlook die internen Informationen zum Lesestatus des Elements, sodass der Lesestatus des Elements nicht erneut hochgeladen wird. Der lokale Speicher kehrt zum Uploadtabellenstatus zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

