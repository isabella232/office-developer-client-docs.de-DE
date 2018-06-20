---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 165be9eada54b2030471fc10e7a0bf0c7dcc7c8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790574"
---
# <a name="pingsession"></a><span data-ttu-id="beb26-103">PingSession</span><span class="sxs-lookup"><span data-stu-id="beb26-103">PingSession</span></span>

<span data-ttu-id="beb26-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="beb26-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="beb26-105">Überprüft, ob eine Sitzung gültig ist.</span><span class="sxs-lookup"><span data-stu-id="beb26-105">Checks whether a session is valid.</span></span> <span data-ttu-id="beb26-106">Diese Funktion ist in der Regel aufgerufen, wenn Excel benötigt, um festzustellen, ob eine zuvor zurückgegebener Sitzungs-ID noch aktiv ist und verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="beb26-106">This function is typically called when Excel needs to determine if a previously returned session ID is still active and can be used.</span></span>
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="beb26-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="beb26-107">Parameters</span></span>

<span data-ttu-id="beb26-108">_Sitzungs-ID_</span><span class="sxs-lookup"><span data-stu-id="beb26-108">_SessionID_</span></span>
  
> <span data-ttu-id="beb26-109">Die ID der Sitzung ping-Befehl an.</span><span class="sxs-lookup"><span data-stu-id="beb26-109">The ID of the session to ping.</span></span> <span data-ttu-id="beb26-110">Dieser Wert muss eine von einem vorherigen Aufruf von [OpenSession](opensession.md)zurückgegebene ID übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="beb26-110">This value must match an ID returned by a previous call to [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="beb26-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="beb26-111">Return value</span></span>

<span data-ttu-id="beb26-112">**XlHpcRetSuccess** Wenn das Argument _SessionId_ gültig ist; andernfalls **XlHpcRetInvalidSessionId**.</span><span class="sxs-lookup"><span data-stu-id="beb26-112">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; otherwise **xlHpcRetInvalidSessionId**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="beb26-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="beb26-113">See also</span></span>

- [<span data-ttu-id="beb26-114">OpenSession</span><span class="sxs-lookup"><span data-stu-id="beb26-114">OpenSession</span></span>](opensession.md)
- [<span data-ttu-id="beb26-115">Excel-Clusterconnector-Funktionen</span><span class="sxs-lookup"><span data-stu-id="beb26-115">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

