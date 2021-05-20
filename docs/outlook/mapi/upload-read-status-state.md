---
title: Hochladen Statusstatus lesen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e8ad2acf019df3f07060c8e8c71a62afd3fca03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431540"
---
# <a name="upload-read-status-state"></a>Hochladen Statusstatus lesen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Statusstatus des Upload-Lesestatus des Replikationsstatuscomputers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Statusbezeichner:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |
|Verwandte Datenstruktur:  <br/> |**[UPREAD](upread.md)** <br/> |
|In diesem Zustand:  <br/> |[Hochladen Tabellenstatus](upload-table-state.md) <br/> |
|In diesem Zustand:  <br/> |Hochladen Tabellenstatus  <br/> |
   
> [!NOTE]
> Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat. Ein Client, der von einem Zustand in einen anderen abt, muss schließlich zu dem ersten von letzterem zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Status initiiert das Hochladen des Lesestatus von Elementen in einem Ordner, der in einem vorherigen Uploadtabelle-Status angegeben ist. Während dieses Status initialisiert Outlook die zugeordnete **UPREAD-Datenstruktur** mit Informationen zu den Elementen im Ordner, dessen Lesestatus sich geändert hat. Der Client aktualisiert dann den Lesestatus dieser Elemente auf dem Server als gelesen oder ungelesen. 
  
Wenn dieser Status endet, Outlook interne Informationen zum Lesestatus des Elements entfernt, was verhindert, dass der Lesestatus des Elements erneut hochgeladen wird. Der lokale Speicher kehrt zum Status der Uploadtabelle zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

