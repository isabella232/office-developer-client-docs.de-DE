---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: af8f7398ed9d5edfbf1615930874a800d8835487
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790398"
---
# <a name="closesession"></a><span data-ttu-id="81eda-103">CloseSession</span><span class="sxs-lookup"><span data-stu-id="81eda-103">CloseSession</span></span>

<span data-ttu-id="81eda-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="81eda-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="81eda-105">Beendet eine Sitzung mit einem Cluster.</span><span class="sxs-lookup"><span data-stu-id="81eda-105">Ends a session with a cluster.</span></span>
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="81eda-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="81eda-106">Parameters</span></span>

<span data-ttu-id="81eda-107">_Sitzungs-ID_</span><span class="sxs-lookup"><span data-stu-id="81eda-107">_SessionId_</span></span>
  
> <span data-ttu-id="81eda-108">Die ID der Sitzung zu schließen.</span><span class="sxs-lookup"><span data-stu-id="81eda-108">The ID of the session to close.</span></span> <span data-ttu-id="81eda-109">Dieser Wert muss den von [OpenSession](opensession.md)zurückgegebenen Wert übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="81eda-109">This value must match the value returned by [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="81eda-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81eda-110">Return value</span></span>

<span data-ttu-id="81eda-111">**XlHpcRetSuccess** , wenn die Sitzung beendet; **XlHpcRetInvalidSessionId** Wenn das _SessionId_ -Argument ungültig ist; **XlHpcRetCallFailed** zu anderen Fehlern.</span><span class="sxs-lookup"><span data-stu-id="81eda-111">**xlHpcRetSuccess** if the session closed; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="81eda-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81eda-112">See also</span></span>

- [<span data-ttu-id="81eda-113">OpenSession</span><span class="sxs-lookup"><span data-stu-id="81eda-113">OpenSession</span></span>](opensession.md)
- [<span data-ttu-id="81eda-114">Excel-Clusterconnector-Funktionen</span><span class="sxs-lookup"><span data-stu-id="81eda-114">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

