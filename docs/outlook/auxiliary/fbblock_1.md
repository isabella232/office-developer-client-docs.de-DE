---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Definiert einen Datenblock Frei/Gebucht-Informationen. Dies ist ein Element in einem Kalender, dargestellt durch ein Termin oder einer Besprechungsanfrage.
ms.openlocfilehash: 93418e3777e9d9f0a016822ea5897b8fccc37ac3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790928"
---
# <a name="fbblock1"></a>FBBlock_1

Definiert einen Datenblock Frei/Gebucht-Informationen. Dies ist ein Element in einem Kalender, dargestellt durch ein Termin oder einer Besprechungsanfrage.
  
## <a name="quick-info"></a>QuickInfo

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a>Members

_m_tmStart_
  
> Die Startzeit für den Block, ausgedrückt als relative Zeit. Weitere Informationen finden Sie unter [Verwendung relative Zeit auf Frei/Gebucht-Daten zugreifen](how-to-use-relative-time-to-access-free-busy-data.md).
    
_m_tmEnd_
  
> Die Endzeit für das blockieren, ausgedrückt als relative Zeit.
    
_m_fbStatus_
  
> Der Frei/Gebucht-Status für diese-Blocks ungültig; zurück, der angibt, ob der Benutzer während des Zeitraums zwischen _M_tmStart_ und _M_tmEnd_Abwesenheits, gebucht, mit Vorbehalt oder frei ist.
    
## <a name="see-also"></a>Siehe auch

- [FBStatus](fbstatus.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)
- [Verwenden Sie relative Zeit Zugriff auf Frei/Gebucht-Daten](how-to-use-relative-time-to-access-free-busy-data.md)

