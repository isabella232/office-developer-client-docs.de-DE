---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 33d0b489a8389fbf61f8bfe2abcd0b9619558929
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588399"
---
# <a name="canceloutstandingrequests"></a>CancelOutstandingRequests

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Informiert den Clusterconnector darüber, dass eine Excel Berechnung abgebrochen wurde und daher möglicherweise auch alle ausstehenden Funktionsaufrufe innerhalb dieser Sitzung abgebrochen werden (und dass Excel keine Rückrufe mit ihren Ergebnissen erwartet).
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a>Parameter

_SessionID_
  
> Die ID der Sitzung, die von der abgebrochenen Berechnung verwendet wird. Dieser Wert entspricht dem von [OpenSession](opensession.md)zurückgegebenen Wert.
    
## <a name="return-value"></a>Rückgabewert

**xlHpcRetSuccess,** wenn das  _Argument SessionId_ gültig ist; **xlHpcRetInvalidSessionId,** wenn das  _Argument SessionId_ ungültig ist; **xlHpcRetCallFailed** bei anderen Fehlern. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Implementierer sollten alle Prozesse für die Sitzung beenden, um die Leistung zu verbessern, da alle nach diesem Aufruf empfangenen Ergebnisse von Excel verworfen werden.
  
## <a name="see-also"></a>Siehe auch

- [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)

