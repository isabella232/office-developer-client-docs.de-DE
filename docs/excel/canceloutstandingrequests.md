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
# <a name="canceloutstandingrequests"></a><span data-ttu-id="38be0-103">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="38be0-103">CancelOutstandingRequests</span></span>

<span data-ttu-id="38be0-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="38be0-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="38be0-105">Informiert den Clusterconnector eine Excel-Berechnung abgebrochen wurde, und daher alle ausstehenden Funktionsaufrufe in dieser Sitzung sowie abgebrochen werden kann (und dass Excel davon ausgehen, dass Rückrufe durch ihre Ergebnisse).</span><span class="sxs-lookup"><span data-stu-id="38be0-105">Informs the cluster connector that an Excel calculation has been canceled, and therefore all pending function calls within that session may be cancelled as well (and that Excel does not expect callbacks with their results).</span></span>
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="38be0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="38be0-106">Parameters</span></span>

<span data-ttu-id="38be0-107">_Sitzungs-ID_</span><span class="sxs-lookup"><span data-stu-id="38be0-107">_SessionID_</span></span>
  
> <span data-ttu-id="38be0-108">Die ID der Sitzung verwendet wird, durch die Berechnung der abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="38be0-108">The ID of the session used by the canceled calculation.</span></span> <span data-ttu-id="38be0-109">Dieser Wert stimmt den von [OpenSession](opensession.md)zurückgegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="38be0-109">This value matches the value returned by [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="38be0-110">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="38be0-110">Return value</span></span>

<span data-ttu-id="38be0-111">**XlHpcRetSuccess** Wenn das Argument _SessionId_ gültig ist; **XlHpcRetInvalidSessionId** Wenn das _SessionId_ -Argument ungültig ist; **XlHpcRetCallFailed** zu anderen Fehlern.</span><span class="sxs-lookup"><span data-stu-id="38be0-111">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="38be0-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="38be0-112">Remarks</span></span>

<span data-ttu-id="38be0-113">Implementierer sollten beenden Sie alle Prozesse für die Sitzung für verbesserte Leistung als Ergebnisse erhalten, nachdem dieser Aufruf von Excel verworfen wird.</span><span class="sxs-lookup"><span data-stu-id="38be0-113">Implementers should stop all processes for the session for improved performance, as any results received after this call will be discarded by Excel.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="38be0-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38be0-114">See also</span></span>

- [<span data-ttu-id="38be0-115">Excel-Clusterconnector-Funktionen</span><span class="sxs-lookup"><span data-stu-id="38be0-115">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

