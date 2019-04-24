---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 9186fb14c33d507b8c9ae709a67f1b43e6206d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304137"
---
# <a name="closesession"></a>CloseSession

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beendet eine Sitzung mit einem Cluster.
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a>Parameter

_SessionId_
  
> Die ID der zu schließende Sitzung. Dieser Wert muss mit dem von OpenSession [](opensession.md)zurückgegebenen Wert übereinstimmen.
    
## <a name="return-value"></a>Rückgabewert

**xlHpcRetSuccess** , wenn die Sitzung geschlossen wurde; **xlHpcRetInvalidSessionId** , wenn das _SessionID_ -Argument ungültig ist; **xlHpcRetCallFailed** bei anderen Fehlern. 
  
## <a name="see-also"></a>Siehe auch

- [OpenSession](opensession.md)
- [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)

