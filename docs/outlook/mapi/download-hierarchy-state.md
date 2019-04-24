---
title: Download-Hierarchie Status
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 45535eef75c6fc091c02ec35b669675a51e4cf48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337009"
---
# <a name="download-hierarchy-state"></a>Download-Hierarchie Status

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Download-Hierarchie Status des Replikationsstatus Computers passiert. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Status-ID:  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |
|Zugehörige Datenstruktur:  <br/> |**[DNHIER](dnhier.md)** <br/> |
|Aus folgendem Zustand:  <br/> |[Zustand „Synchronisieren“](synchronize-state.md) <br/> |
|Zu folgendem Status:  <br/> |Zustand „Synchronisieren“  <br/> |
   
> [!NOTE]
> Der Replikationsstatus Computer ist ein deterministischer Statuscomputer. Ein Client, der von einem Staat zu einem anderen abgeht, muss schließlich aus letzterem zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Status initiiert das Herunterladen einer Strukturhierarchie von Ordnern von einem Server in den lokalen Speicher. 
  
Outlook initialisiert die zugeordnete **DNHIER** -Datenstruktur mit einem Zeiger auf die Hierarchie. Der Client downloadet die Hierarchie und fügt neue Ordner oder Änderungen in Ordner im lokalen Speicher ein. Der Downloadprozess übernimmt die Microsoft Exchange-inkrementelle Änderungs Synchronisierung (ICS). Weitere Informationen zu ICS finden Sie unter [ICS-Auswertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
Wenn dieser Status endet, wird der lokale Speicher zum Synchronize-Status zurückgegeben.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

