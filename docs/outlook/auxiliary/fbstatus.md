---
title: FBStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: f2d6a11e-847d-6bbe-cd77-e78ee961cb12
description: Eine Aufzählung für den Frei/Gebucht-Status von Frei/Gebucht-Blöcken.
ms.openlocfilehash: 61ac90849e2a0d40b48281cb6f145fc5d997d545
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592802"
---
# <a name="fbstatus"></a>FBStatus

Eine Aufzählung für den Frei/Gebucht-Status von Frei/Gebucht-Blöcken.
  
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

## <a name="remarks"></a>HinwBemerkungeneise

Der Frei/Gebucht-Status eines Zeitblocks bestimmt, wie er in einem Kalender angezeigt wird: **Frei,** **Gebucht,** **Mit Vorbehalt** oder **Außerhalb Office**. 
  
## <a name="see-also"></a>Siehe auch

- [FBBlock_1](fbblock_1.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)

