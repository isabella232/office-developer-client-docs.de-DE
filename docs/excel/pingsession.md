---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0fa5fe57e537a7b8c7d880b934809a6f68ce27a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408362"
---
# <a name="pingsession"></a>PingSession

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Überprüft, ob eine Sitzung gültig ist. Diese Funktion wird in der Regel aufgerufen, wenn Excel ermitteln muss, ob eine zuvor zurückgegebene Sitzungs-ID noch aktiv ist und verwendet werden kann.
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a>Parameter

_SessionID_
  
> Die ID der zu pingenden Sitzung. Dieser Wert muss mit einer ID übereinstimmen, die von einem [](opensession.md)vorherigen Aufruf von OpenSession zurückgegeben wurde.
    
## <a name="return-value"></a>Rückgabewert

**xlHpcRetSuccess** , wenn das _SessionID_ -Argument gültig ist; andernfalls **xlHpcRetInvalidSessionId**.
  
## <a name="see-also"></a>Siehe auch

- [OpenSession](opensession.md)
- [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)

