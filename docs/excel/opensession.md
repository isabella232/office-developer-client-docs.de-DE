---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e4df0c5772f28ab4ab8d84eaddfe4409a88061b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421837"
---
# <a name="opensession"></a><span data-ttu-id="7edd0-103">OpenSession</span><span class="sxs-lookup"><span data-stu-id="7edd0-103">OpenSession</span></span>

<span data-ttu-id="7edd0-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7edd0-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7edd0-105">Erstellt eine Sitzung, in der benutzerdefinierte Funktionen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="7edd0-105">Creates a session in which user-defined functions can be executed.</span></span>
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a><span data-ttu-id="7edd0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7edd0-106">Parameters</span></span>

<span data-ttu-id="7edd0-107">_Parameter_</span><span class="sxs-lookup"><span data-stu-id="7edd0-107">_Params_</span></span>
  
> <span data-ttu-id="7edd0-108">Ein Zeiger auf durch Semikolons getrennte UNICODE-Zeichenfolge von Parametern für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="7edd0-108">A pointer to semicolon-delimited UNICODE string of parameters for the session.</span></span> <span data-ttu-id="7edd0-109">Excel verwendet dieses Argument nicht.</span><span class="sxs-lookup"><span data-stu-id="7edd0-109">Excel does not use this argument.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7edd0-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7edd0-110">Return value</span></span>

<span data-ttu-id="7edd0-111">Eine Sitzungs-ID, die in anderen Aufrufen des Cluster-Konnektors verwendet werden soll, wenn die Sitzung erfolgreich erstellt wurde; andernfalls **xlHpcRetCallFailed**.</span><span class="sxs-lookup"><span data-stu-id="7edd0-111">A session ID to use in other calls to the cluster connector, if the session was successfully created; otherwise **xlHpcRetCallFailed**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7edd0-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7edd0-112">See also</span></span>

- [<span data-ttu-id="7edd0-113">Excel-Clusterconnector-Funktionen</span><span class="sxs-lookup"><span data-stu-id="7edd0-113">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

