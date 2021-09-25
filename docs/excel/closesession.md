---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cba9dbdbcab59dc178a5ae0573ff3e7f0009d72b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593012"
---
# <a name="closesession"></a>CloseSession

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beendet eine Sitzung mit einem Cluster.
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a>Parameter

_SessionId_
  
> Die ID der zu schließenden Sitzung. Dieser Wert muss mit dem von [OpenSession](opensession.md)zurückgegebenen Wert übereinstimmen.
    
## <a name="return-value"></a>Rückgabewert

**xlHpcRetSuccess,** wenn die Sitzung geschlossen wurde; **xlHpcRetInvalidSessionId,** wenn das  _Argument SessionId_ ungültig ist; **xlHpcRetCallFailed** bei anderen Fehlern. 
  
## <a name="see-also"></a>Siehe auch

- [OpenSession](opensession.md)
- [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)

