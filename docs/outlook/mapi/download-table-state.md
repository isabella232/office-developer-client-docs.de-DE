---
title: Tabellenstatus herunterladen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7451d159ef97ef9d8160b386ec5bf88fb388706e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338339"
---
# <a name="download-table-state"></a>Tabellenstatus herunterladen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Zustands der Downloadtabelle des Replikationsstatuscomputers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Statusbezeichner:  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |
|Verwandte Datenstruktur:  <br/> |**[DNTBL](dntbl.md)** <br/> |
|In diesem Zustand:  <br/> |[Synchronisieren des Inhaltszustands](synchronize-contents-state.md) <br/> |
|In diesem Zustand:  <br/> |Synchronisieren des Inhaltszustands  <br/> |
   
> [!NOTE]
> Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat. Ein Client, der von einem Zustand in einen anderen abt, muss schließlich zu dem ersten von letzterem zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Status initiiert das Herunterladen eines Ordners. Während dieses Status initialisiert Outlook die zugeordnete **DNTBL-Datenstruktur** mit Informationen zum Ordner. Der Client lädt den Ordnerinhalt herunter und aktualisiert den Ordner im lokalen Speicher mit neuen Inhalten, Änderungen oder Löschungen vom Server. Der Downloadprozess übernimmt microsoft Exchange Incremental Change Synchronization (ICS). Weitere Informationen zu ICS finden Sie unter [ICS-Auswertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
Wenn dieser Status endet, kehrt der lokale Speicher zum Status "Inhalt synchronisieren" zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

