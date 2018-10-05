---
title: Status „Downloadtabelle“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7451d159ef97ef9d8160b386ec5bf88fb388706e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395070"
---
# <a name="download-table-state"></a>Status „Downloadtabelle“

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, während der Tabelle Downloadstatus von der Replikation Zustandsautomat erläutert. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|State-ID:  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |
|Verwandte-Datenstruktur:  <br/> |**[DNTBL](dntbl.md)** <br/> |
|Aus diesem Zustand:  <br/> |[Synchronisieren von Inhalt Zustand](synchronize-contents-state.md) <br/> |
|Diesen Status:  <br/> |Synchronisieren von Inhalt Zustand  <br/> |
   
> [!NOTE]
> Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat. Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben. 
  
## <a name="description"></a>Beschreibung

Dieser Status wird initiiert, einen Ordner herunterladen. Während dieser Zustand initialisiert Outlook die zugeordnete **DNTBL** -Datenstruktur mit Informationen zu den Ordner. Der Client den Ordnerinhalt downloads und aktualisiert den Ordner auf dem lokalen Speicher mit neuen Inhalt, geändert oder vom Server gelöscht. Der Downloadvorgang nimmt Microsoft Exchange inkrementelle Änderung Synchronisierung (ICS). Weitere Informationen zu ICS finden Sie unter [ICS Bewertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
Wenn dieser Status beendet ist, gibt der lokale Speicher auf den Status der Synchronize-Inhalt zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

