---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 9186fb14c33d507b8c9ae709a67f1b43e6206d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304137"
---
# <a name="closesession"></a><span data-ttu-id="d9a85-103">CloseSession</span><span class="sxs-lookup"><span data-stu-id="d9a85-103">CloseSession</span></span>

<span data-ttu-id="d9a85-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d9a85-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d9a85-105">Beendet eine Sitzung mit einem Cluster.</span><span class="sxs-lookup"><span data-stu-id="d9a85-105">Ends a session with a cluster.</span></span>
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="d9a85-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9a85-106">Parameters</span></span>

<span data-ttu-id="d9a85-107">_SessionId_</span><span class="sxs-lookup"><span data-stu-id="d9a85-107">_SessionId_</span></span>
  
> <span data-ttu-id="d9a85-108">Die ID der zu schließende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="d9a85-108">The ID of the session to close.</span></span> <span data-ttu-id="d9a85-109">Dieser Wert muss mit dem von OpenSession [](opensession.md)zurückgegebenen Wert übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="d9a85-109">This value must match the value returned by [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d9a85-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9a85-110">Return value</span></span>

<span data-ttu-id="d9a85-111">**xlHpcRetSuccess** , wenn die Sitzung geschlossen wurde; **xlHpcRetInvalidSessionId** , wenn das _SessionID_ -Argument ungültig ist; **xlHpcRetCallFailed** bei anderen Fehlern.</span><span class="sxs-lookup"><span data-stu-id="d9a85-111">**xlHpcRetSuccess** if the session closed; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d9a85-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9a85-112">See also</span></span>

- [<span data-ttu-id="d9a85-113">OpenSession</span><span class="sxs-lookup"><span data-stu-id="d9a85-113">OpenSession</span></span>](opensession.md)
- [<span data-ttu-id="d9a85-114">Excel-Clusterconnector-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d9a85-114">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

