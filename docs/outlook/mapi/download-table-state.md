---
title: Downloadtabellenstatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 632592b5f9ea87b17baf0badefb6f3551c4b58da
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588101"
---
# <a name="download-table-state"></a>Downloadtabellenstatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Downloadtabellenstatus des Replikationsstatuscomputers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Statusbezeichner:  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |
|Verwandte Datenstruktur:  <br/> |**[DNTBL](dntbl.md)** <br/> |
|Aus diesem Zustand:  <br/> |[Synchronisieren des Inhaltsstatus](synchronize-contents-state.md) <br/> |
|In diesem Zustand:  <br/> |Synchronisieren des Inhaltsstatus  <br/> |
   
> [!NOTE]
> Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat. Ein Client, der von einem Bundesland in einen anderen wechselt, muss schließlich von letzterem zum ersten Zurückkehren zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Zustand initiiert das Herunterladen eines Ordners. In diesem Zustand initialisiert Outlook die zugeordnete **DNTBL-Datenstruktur** mit Informationen zum Ordner. Der Client lädt den Ordnerinhalt herunter und aktualisiert den Ordner im lokalen Speicher mit neuen Inhalten, Änderungen oder Löschungen vom Server. Der Downloadprozess übernimmt Microsoft Exchange Inkrementelle Änderungssynchronisierung (Incremental Change Synchronization, ICS). Weitere Informationen zu ICS finden Sie unter [ICS-Auswertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
Wenn dieser Zustand endet, kehrt der lokale Speicher in den Status "Synchronisierter Inhalt" zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

