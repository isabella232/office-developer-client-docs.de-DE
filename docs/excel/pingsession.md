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
# <a name="pingsession"></a><span data-ttu-id="d0414-103">PingSession</span><span class="sxs-lookup"><span data-stu-id="d0414-103">PingSession</span></span>

<span data-ttu-id="d0414-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d0414-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d0414-105">Überprüft, ob eine Sitzung gültig ist.</span><span class="sxs-lookup"><span data-stu-id="d0414-105">Checks whether a session is valid.</span></span> <span data-ttu-id="d0414-106">Diese Funktion wird normalerweise aufgerufen, wenn Excel ermitteln muss, ob eine zuvor zurückgegebene Sitzungs-ID noch aktiv ist und verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d0414-106">This function is typically called when Excel needs to determine if a previously returned session ID is still active and can be used.</span></span>
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="d0414-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0414-107">Parameters</span></span>

<span data-ttu-id="d0414-108">_SessionID_</span><span class="sxs-lookup"><span data-stu-id="d0414-108">_SessionID_</span></span>
  
> <span data-ttu-id="d0414-109">Die ID der zu ping-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="d0414-109">The ID of the session to ping.</span></span> <span data-ttu-id="d0414-110">Dieser Wert muss mit einer ID übereinstimmen, die von einem vorherigen Aufruf von [OpenSession zurückgegeben wurde.](opensession.md)</span><span class="sxs-lookup"><span data-stu-id="d0414-110">This value must match an ID returned by a previous call to [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d0414-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d0414-111">Return value</span></span>

<span data-ttu-id="d0414-112">**xlHpcRetSuccess,** wenn  _das Argument SessionId_ gültig ist; andernfalls **xlHpcRetInvalidSessionId**.</span><span class="sxs-lookup"><span data-stu-id="d0414-112">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; otherwise **xlHpcRetInvalidSessionId**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d0414-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0414-113">See also</span></span>

- [<span data-ttu-id="d0414-114">OpenSession</span><span class="sxs-lookup"><span data-stu-id="d0414-114">OpenSession</span></span>](opensession.md)
- [<span data-ttu-id="d0414-115">Excel-Clusterconnector-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d0414-115">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

