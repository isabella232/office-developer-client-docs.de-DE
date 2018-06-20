---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: af8f7398ed9d5edfbf1615930874a800d8835487
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790398"
---
# <a name="closesession"></a>CloseSession

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beendet eine Sitzung mit einem Cluster.
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a>Parameter

_Sitzungs-ID_
  
> Die ID der Sitzung zu schließen. Dieser Wert muss den von [OpenSession](opensession.md)zurückgegebenen Wert übereinstimmen.
    
## <a name="return-value"></a>R�ckgabewert

**XlHpcRetSuccess** , wenn die Sitzung beendet; **XlHpcRetInvalidSessionId** Wenn das _SessionId_ -Argument ungültig ist; **XlHpcRetCallFailed** zu anderen Fehlern. 
  
## <a name="see-also"></a>Siehe auch

- [OpenSession](opensession.md)
- [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)

