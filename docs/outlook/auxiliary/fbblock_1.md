---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Definiert einen Frei/Gebucht-Datenblock. Dies ist ein Element in einem Kalender, der durch einen Termin oder eine Besprechungsanfrage dargestellt wird.
ms.openlocfilehash: 5cf556e4df99801a56857d55c43b008f4071f714
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557323"
---
# <a name="fbblock_1"></a>FBBlock_1

Definiert einen Frei/Gebucht-Datenblock. Dies ist ein Element in einem Kalender, der durch einen Termin oder eine Besprechungsanfrage dargestellt wird.
  
## <a name="quick-info"></a>QuickInfo

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a>Elemente

_m_tmStart_
  
> Die Startzeit für den Block, ausgedrückt in relativer Zeit. Weitere Informationen finden Sie unter [Verwenden der relativen Zeit für den Zugriff auf Frei/Gebucht-Daten.](how-to-use-relative-time-to-access-free-busy-data.md)
    
_m_tmEnd_
  
> Die Endzeit für den Block, ausgedrückt in relativer Zeit.
    
_m_fbStatus_
  
> Der Frei/Gebucht-Status für diesen Block, der angibt, ob der Benutzer während des Zeitraums zwischen  _m_tmStart_ und  _m_tmEnd_ außer Haus, beschäftigt, mit Vorbehalt oder kostenlos ist.
    
## <a name="see-also"></a>Siehe auch

- [FBStatus](fbstatus.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)
- [Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten](how-to-use-relative-time-to-access-free-busy-data.md)

