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
# <a name="canceloutstandingrequests"></a><span data-ttu-id="9a805-103">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="9a805-103">CancelOutstandingRequests</span></span>

<span data-ttu-id="9a805-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9a805-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9a805-105">Informiert den Cluster-Konnektor darüber, dass eine Excel-Berechnung abgebrochen wurde, und daher können alle ausstehenden Funktionsaufrufe innerhalb dieser Sitzung ebenfalls abgebrochen werden (und Excel erwarte keine Rückrufe mit ihren Ergebnissen).</span><span class="sxs-lookup"><span data-stu-id="9a805-105">Informs the cluster connector that an Excel calculation has been canceled, and therefore all pending function calls within that session may be cancelled as well (and that Excel does not expect callbacks with their results).</span></span>
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="9a805-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a805-106">Parameters</span></span>

<span data-ttu-id="9a805-107">_SessionID_</span><span class="sxs-lookup"><span data-stu-id="9a805-107">_SessionID_</span></span>
  
> <span data-ttu-id="9a805-108">Die ID der Sitzung, die von der abgebrochenen Berechnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9a805-108">The ID of the session used by the canceled calculation.</span></span> <span data-ttu-id="9a805-109">Dieser Wert entspricht dem von OpenSession [](opensession.md)zurückgegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="9a805-109">This value matches the value returned by [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9a805-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a805-110">Return value</span></span>

<span data-ttu-id="9a805-111">**xlHpcRetSuccess** , wenn das _SessionID_ -Argument gültig ist; **xlHpcRetInvalidSessionId** , wenn das _SessionID_ -Argument ungültig ist; **xlHpcRetCallFailed** bei anderen Fehlern.</span><span class="sxs-lookup"><span data-stu-id="9a805-111">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9a805-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a805-112">Remarks</span></span>

<span data-ttu-id="9a805-113">Implementierer sollten alle Prozesse für die Sitzung für eine verbesserte Leistung beenden, da alle Ergebnisse nach diesem Aufruf von Excel verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="9a805-113">Implementers should stop all processes for the session for improved performance, as any results received after this call will be discarded by Excel.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9a805-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a805-114">See also</span></span>

- [<span data-ttu-id="9a805-115">Excel-Clusterconnector-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9a805-115">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

