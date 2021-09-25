---
title: Herunterladen des Hierarchiestatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 16a9691cb5129fd53817db295017cdac664992bd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596568"
---
# <a name="download-hierarchy-state"></a>Herunterladen des Hierarchiestatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Downloadhierarchiestatus des Replikationsstatuscomputers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Statusbezeichner:  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |
|Verwandte Datenstruktur:  <br/> |**[DNHIER](dnhier.md)** <br/> |
|Aus diesem Zustand:  <br/> |[Zustand „Synchronisieren“](synchronize-state.md) <br/> |
|In diesem Zustand:  <br/> |Zustand „Synchronisieren“  <br/> |
   
> [!NOTE]
> Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat. Ein Client, der von einem Bundesland in einen anderen wechselt, muss schließlich von letzterem zum ersten Zurückkehren zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Zustand initiiert das Herunterladen einer Strukturhierarchie von Ordnern von einem Server in den lokalen Speicher. 
  
Outlook initialisiert die zugeordnete **DNHIER-Datenstruktur** mit einem Zeiger auf die Hierarchie. Der Client lädt die Hierarchie herunter und fügt neue Ordner oder Änderungen in Ordner im lokalen Speicher ein. Der Downloadprozess übernimmt Microsoft Exchange inkrementelle Änderungssynchronisierung (Incremental Change Synchronization, ICS). Weitere Informationen zu ICS finden Sie unter [ICS-Auswertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
Wenn dieser Zustand endet, kehrt der lokale Speicher in den Synchronisierungsstatus zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

