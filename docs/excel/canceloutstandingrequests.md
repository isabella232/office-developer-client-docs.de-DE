---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 882458ab096cbced8e0635dab65fe0b1d680388f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414718"
---
# <a name="canceloutstandingrequests"></a>CancelOutstandingRequests

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Informiert den Clusterconnector darüber, dass eine Excel-Berechnung abgebrochen wurde, und daher können auch alle ausstehenden Funktionsaufrufe innerhalb dieser Sitzung abgebrochen werden (und dass Excel keine Rückrufe mit ihren Ergebnissen erwartet).
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a>Parameter

_SessionID_
  
> Die ID der Sitzung, die von der abgebrochenen Berechnung verwendet wird. Dieser Wert entspricht dem von [OpenSession zurückgegebenen Wert.](opensession.md)
    
## <a name="return-value"></a>Rückgabewert

**xlHpcRetSuccess,** wenn  _das Argument SessionId_ gültig ist; **xlHpcRetInvalidSessionId,** wenn  _das Argument SessionId_ ungültig ist; **xlHpcRetCallFailed** bei anderen Fehlern. 
  
## <a name="remarks"></a>Hinweise

Implementierer sollten alle Prozesse für die Sitzung beenden, um die Leistung zu verbessern, da alle Ergebnisse, die nach diesem Aufruf empfangen werden, von der Excel.
  
## <a name="see-also"></a>Siehe auch

- [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)

