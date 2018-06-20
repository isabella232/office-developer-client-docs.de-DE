---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 782843f11643e203488b313181d224443a1d36c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790561"
---
# <a name="opensession"></a><span data-ttu-id="09dfc-103">OpenSession</span><span class="sxs-lookup"><span data-stu-id="09dfc-103">OpenSession</span></span>

<span data-ttu-id="09dfc-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="09dfc-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="09dfc-105">Erstellt eine Sitzung in der benutzerdefinierten Funktionen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="09dfc-105">Creates a session in which user-defined functions can be executed.</span></span>
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a><span data-ttu-id="09dfc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="09dfc-106">Parameters</span></span>

<span data-ttu-id="09dfc-107">_Params_</span><span class="sxs-lookup"><span data-stu-id="09dfc-107">_Params_</span></span>
  
> <span data-ttu-id="09dfc-108">Ein Zeiger auf die durch Semikolons getrennte Unicode-Zeichenfolge der Parameter für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="09dfc-108">A pointer to semicolon-delimited UNICODE string of parameters for the session.</span></span> <span data-ttu-id="09dfc-109">Excel wird dieses Argument nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="09dfc-109">Excel does not use this argument.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="09dfc-110">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="09dfc-110">Return value</span></span>

<span data-ttu-id="09dfc-111">Eine ID für eine Sitzung in anderen Aufrufe an den Konnektor Cluster verwenden, wenn die Sitzung erfolgreich erstellt wurde; andernfalls **XlHpcRetCallFailed**.</span><span class="sxs-lookup"><span data-stu-id="09dfc-111">A session ID to use in other calls to the cluster connector, if the session was successfully created; otherwise **xlHpcRetCallFailed**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="09dfc-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09dfc-112">See also</span></span>

- [<span data-ttu-id="09dfc-113">Excel-Clusterconnector-Funktionen</span><span class="sxs-lookup"><span data-stu-id="09dfc-113">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

