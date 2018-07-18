---
title: Status „Status des Upload-Lesevorgangs“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 172eaf47d305cf6e4d1ba54ceb4ac4b4feab80e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795806"
---
# <a name="upload-read-status-state"></a>Status „Status des Upload-Lesevorgangs“

  
  
**Betrifft**: Outlook 
  
 In diesem Thema wird beschrieben, was geschieht, während der Upload Status Zustand des Computers Zustand Replikation lesen. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|State-ID:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |
|Verwandte-Datenstruktur:  <br/> |**[UPREAD](upread.md)** <br/> |
|Aus diesem Zustand:  <br/> |[Tabelle Zustand hochladen](upload-table-state.md) <br/> |
|Diesen Status:  <br/> |Tabelle Zustand hochladen  <br/> |
   
> [!NOTE]
> Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat. Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben. 
  
## <a name="description"></a>Beschreibung

Dieser Status wird initiiert, Hochladen des Status Lesen von Elementen in einem Ordner, in den vorstehenden Upload-Tabelle angegeben. Während dieser Zustand initialisiert Outlook die zugeordnete **UPREAD** -Datenstruktur mit Informationen für diese Elemente im Ordner, deren Status Lesen geändert wurde. Der Client aktualisiert anschließend den lesen Status dieser Elemente auf dem Server als gelesen oder ungelesen. 
  
Wenn dieser Status beendet ist, löscht Outlook die interne Informationen über das Element gelesen-Status, verhindert, dass das Element gelesen-Status wird erneut hochgeladen. Auf den Upload Tabelle Status gibt der lokale Speicher zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

