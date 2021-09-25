---
title: FollowUpStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c3d0f6c4-4597-784f-8d44-6e5d905895b4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ad601ff547bfb89b98f0733b9e070b923ad92e1c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556735"
---
# <a name="followupstatus"></a>FollowUpStatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die verschiedenen Nachverfolgungsstatus für eine Nachricht an.
  
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
  
> Die Nachricht wird zur Nachverfolgung markiert.
    
 _flwupMAX_
  
> Die Anzahl der verschiedenen Status, die für die Nachverfolgung unterstützt werden.
    
## <a name="see-also"></a>Siehe auch



[PidTagFlagStatus (kanonische Eigenschaft)](pidtagflagstatus-canonical-property.md)

