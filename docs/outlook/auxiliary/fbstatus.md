---
title: FBStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f2d6a11e-847d-6bbe-cd77-e78ee961cb12
description: Eine Enumeration für den Frei/Gebucht-Status von Frei/Gebucht-Blöcken.
ms.openlocfilehash: 2a08ef142f9baddd453166c0ebcb989e69a51ceb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424091"
---
# <a name="fbstatus"></a>FBStatus

Eine Enumeration für den Frei/Gebucht-Status von Frei/Gebucht-Blöcken.
  
## <a name="quick-info"></a>QuickInfo

```cpp
enum  
    { 
      fbFree      = 0, 
      fbTentative = fbFree + 1, 
      fbBusy      = fbTentative + 1, 
      fbOutOfOffice = fbBusy + 1 
    }

```

## <a name="remarks"></a>Bemerkungen

Der Frei/Gebucht-Status eines Zeitblocks bestimmt, wie er in einem Kalender angezeigt wird: **frei**, **beschäftigt**, mit **Vorbehalt**oder **** Abwesenheit. 
  
## <a name="see-also"></a>Siehe auch

- [FBBlock_1](fbblock_1.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)

