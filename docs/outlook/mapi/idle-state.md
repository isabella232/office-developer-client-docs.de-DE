---
title: Leerlaufzustand
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 67f3c24de34ebfe6b2b96fae0f64ff61037fc839
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561544"
---
# <a name="idle-state"></a>Leerlaufzustand

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Leerlaufs des Replikationsstatuscomputers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Statusbezeichner:  <br/> |**LR_SYNC_IDLE** <br/> |
|Verwandte Datenstruktur:  <br/> | *Keine*  <br/> |
|Aus diesem Zustand:  <br/> | *Nicht zutreffend*  <br/> |
|In diesem Zustand:  <br/> |[Zustand „Synchronisieren“](synchronize-state.md) <br/> |
   
> [!NOTE]
> Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat. Ein Client, der von einem Bundesland in einen anderen wechselt, muss schließlich von letzterem zum ersten Zurückkehren zurückkehren. 
  
## <a name="description"></a>Beschreibung

In diesem Zustand passiert nichts. Ein lokaler Speicher befindet sich in diesem Zustand, bevor die Replikation initiiert wird und nachdem die Replikation abgeschlossen ist.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

