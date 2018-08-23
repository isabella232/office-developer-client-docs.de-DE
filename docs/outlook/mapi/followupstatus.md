---
title: FollowUpStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c3d0f6c4-4597-784f-8d44-6e5d905895b4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6b57ed45e067ce2debd40e033d386ad2b5ae895a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568518"
---
# <a name="followupstatus"></a>FollowUpStatus

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt die verschiedenen weiteren Statusarten für eine Nachricht an.
  
## <a name="quick-info"></a>QuickInfo

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a>Elemente

 _flwupNone_
  
> Keine Nachsorge es wurde angegeben.
    
 _flwupComplete_
  
> Die Nachricht ist abgeschlossen.
    
 _flwupMarked_
  
> Die Nachricht ist für die nachverfolgung gekennzeichnet.
    
 _flwupMAX_
  
> Die Anzahl der verschiedenen Statusarten für Nachsorge unterstützt.
    
## <a name="see-also"></a>Siehe auch



[PidTagFlagStatus (kanonische Eigenschaft)](pidtagflagstatus-canonical-property.md)

