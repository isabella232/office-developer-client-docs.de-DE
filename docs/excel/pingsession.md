---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 195feaebe15d6306859d8b5112f4fb2f05134ff9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621388"
---
# <a name="pingsession"></a>PingSession

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Überprüft, ob eine Sitzung gültig ist. Diese Funktion wird in der Regel aufgerufen, wenn Excel ermitteln muss, ob eine zuvor zurückgegebene Sitzungs-ID noch aktiv ist und verwendet werden kann.
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a>Parameter

_SessionID_
  
> Die ID der Sitzung zum Pingen. Dieser Wert muss mit einer ID übereinstimmen, die von einem vorherigen Aufruf von [OpenSession](opensession.md)zurückgegeben wurde.
    
## <a name="return-value"></a>Rückgabewert

**xlHpcRetSuccess,** wenn das  _Argument SessionId_ gültig ist; andernfalls **xlHpcRetInvalidSessionId**.
  
## <a name="see-also"></a>Siehe auch

- [OpenSession](opensession.md)
- [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)

