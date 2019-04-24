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
ms.openlocfilehash: 2280ae9271ca73af33f395bf9e41a9ee8fa62f96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327524"
---
# <a name="followupstatus"></a>FollowUpStatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die verschiedenen nachverfolgungsstatus für eine Nachricht an.
  
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
  
> Es wurde keine Nachverfolgung angegeben.
    
 _flwupComplete_
  
> Die Nachricht ist abgeschlossen.
    
 _flwupMarked_
  
> Die Nachricht ist zur Nachverfolgung gekennzeichnet.
    
 _flwupMAX_
  
> Die Anzahl der unterstützten Status für die Nachverfolgung.
    
## <a name="see-also"></a>Siehe auch



[Kanonische Pidtagflagstatus (-Eigenschaft](pidtagflagstatus-canonical-property.md)

