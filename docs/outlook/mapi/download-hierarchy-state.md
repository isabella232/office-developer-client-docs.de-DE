---
title: Status „Downloadhierarchie“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 45535eef75c6fc091c02ec35b669675a51e4cf48
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384857"
---
# <a name="download-hierarchy-state"></a>Status „Downloadhierarchie“

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, während den Downloadstatus Hierarchie, von der Replikation Zustandsautomat erläutert. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|State-ID:  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |
|Verwandte-Datenstruktur:  <br/> |**[DNHIER](dnhier.md)** <br/> |
|Aus diesem Zustand:  <br/> |[Synchronisieren von Zustand](synchronize-state.md) <br/> |
|Diesen Status:  <br/> |Synchronisieren von Zustand  <br/> |
   
> [!NOTE]
> Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat. Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben. 
  
## <a name="description"></a>Beschreibung

Dieser Status initiiert eine Strukturhierarchie von Ordnern auf einem Server auf den lokalen Speicher herunterladen. 
  
Outlook initialisiert die zugeordnete **DNHIER** -Datenstruktur mit einem Zeiger auf der Hierarchie. Der Client downloads die Hierarchie und fügt neue Ordner oder Änderungen an Ordnern im lokalen Speicher. Der Downloadvorgang nimmt Microsoft Exchange inkrementelle Änderung Synchronisierung (ICS). Weitere Informationen zu ICS finden Sie unter [ICS Bewertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
Wenn dieser Status beendet ist, gibt der lokale Speicher auf den Status synchronisieren zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

