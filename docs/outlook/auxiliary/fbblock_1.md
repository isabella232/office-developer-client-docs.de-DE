---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Definiert einen frei/gebucht-Datenblock. Dies ist ein Element in einem Kalender, dargestellt durch einen Termin oder eine Besprechungsanfrage.
ms.openlocfilehash: 60d2ff50081a8950a397df6f2f6bbfd37d3bdb61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413199"
---
# <a name="fbblock1"></a>FBBlock_1

Definiert einen frei/gebucht-Datenblock. Dies ist ein Element in einem Kalender, dargestellt durch einen Termin oder eine Besprechungsanfrage.
  
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
  
> Die Startzeit für den Block, ausgedrückt in relativer Zeit. Weitere Informationen finden Sie unter [Verwenden von relativer Zeit für den Zugriff auf Frei/Gebucht-Daten](how-to-use-relative-time-to-access-free-busy-data.md).
    
_m_tmEnd_
  
> Die Endzeit für den Block, ausgedrückt in relativer Zeit.
    
_m_fbStatus_
  
> Der Frei/Gebucht-Status für diesen Block, der angibt, ob der Benutzer Abwesenheit, beschäftigt, mit Vorbehalt oder kostenlos ist, während des Zeitraums zwischen _m_tmStart_ und _m_tmEnd_.
    
## <a name="see-also"></a>Siehe auch

- [FBStatus](fbstatus.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)
- [Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten](how-to-use-relative-time-to-access-free-busy-data.md)

