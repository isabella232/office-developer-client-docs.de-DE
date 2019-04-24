---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 882458ab096cbced8e0635dab65fe0b1d680388f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310997"
---
# <a name="canceloutstandingrequests"></a>CancelOutstandingRequests

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Informiert den Cluster-Konnektor darüber, dass eine Excel-Berechnung abgebrochen wurde, und daher können alle ausstehenden Funktionsaufrufe innerhalb dieser Sitzung ebenfalls abgebrochen werden (und Excel erwarte keine Rückrufe mit ihren Ergebnissen).
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a>Parameter

_SessionID_
  
> Die ID der Sitzung, die von der abgebrochenen Berechnung verwendet wird. Dieser Wert entspricht dem von OpenSession [](opensession.md)zurückgegebenen Wert.
    
## <a name="return-value"></a>Rückgabewert

**xlHpcRetSuccess** , wenn das _SessionID_ -Argument gültig ist; **xlHpcRetInvalidSessionId** , wenn das _SessionID_ -Argument ungültig ist; **xlHpcRetCallFailed** bei anderen Fehlern. 
  
## <a name="remarks"></a>Bemerkungen

Implementierer sollten alle Prozesse für die Sitzung für eine verbesserte Leistung beenden, da alle Ergebnisse nach diesem Aufruf von Excel verworfen werden.
  
## <a name="see-also"></a>Siehe auch

- [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)

