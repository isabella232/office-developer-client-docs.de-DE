---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 165be9eada54b2030471fc10e7a0bf0c7dcc7c8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790574"
---
# <a name="pingsession"></a>PingSession

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Überprüft, ob eine Sitzung gültig ist. Diese Funktion ist in der Regel aufgerufen, wenn Excel benötigt, um festzustellen, ob eine zuvor zurückgegebener Sitzungs-ID noch aktiv ist und verwendet werden kann.
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a>Parameter

_Sitzungs-ID_
  
> Die ID der Sitzung ping-Befehl an. Dieser Wert muss eine von einem vorherigen Aufruf von [OpenSession](opensession.md)zurückgegebene ID übereinstimmen.
    
## <a name="return-value"></a>R�ckgabewert

**XlHpcRetSuccess** Wenn das Argument _SessionId_ gültig ist; andernfalls **XlHpcRetInvalidSessionId**.
  
## <a name="see-also"></a>Siehe auch

- [OpenSession](opensession.md)
- [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)

