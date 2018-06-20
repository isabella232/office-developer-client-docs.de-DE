---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 65d4257037b18c8fa68cabe0c08091ec67343fa5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790388"
---
# <a name="canceloutstandingrequests"></a>CancelOutstandingRequests

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Informiert den Clusterconnector eine Excel-Berechnung abgebrochen wurde, und daher alle ausstehenden Funktionsaufrufe in dieser Sitzung sowie abgebrochen werden kann (und dass Excel davon ausgehen, dass Rückrufe durch ihre Ergebnisse).
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a>Parameter

_Sitzungs-ID_
  
> Die ID der Sitzung verwendet wird, durch die Berechnung der abgebrochen. Dieser Wert stimmt den von [OpenSession](opensession.md)zurückgegebenen Wert.
    
## <a name="return-value"></a>R�ckgabewert

**XlHpcRetSuccess** Wenn das Argument _SessionId_ gültig ist; **XlHpcRetInvalidSessionId** Wenn das _SessionId_ -Argument ungültig ist; **XlHpcRetCallFailed** zu anderen Fehlern. 
  
## <a name="remarks"></a>Hinweise

Implementierer sollten beenden Sie alle Prozesse für die Sitzung für verbesserte Leistung als Ergebnisse erhalten, nachdem dieser Aufruf von Excel verworfen wird.
  
## <a name="see-also"></a>Siehe auch

- [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)

