---
title: Excel-Cluster-Konnektorfunktionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 41a5cf1ecb7c8f38f4aa5b62a493b3f45c2fe090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408586"
---
# <a name="excel-cluster-connector-functions"></a><span data-ttu-id="5daba-103">Excel-Cluster-Konnektorfunktionen</span><span class="sxs-lookup"><span data-stu-id="5daba-103">Excel Cluster Connector Functions</span></span>

 <span data-ttu-id="5daba-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5daba-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5daba-105">Microsoft Excel 2013-Cluster-Connector-DLLs müssen die in diesem Abschnitt beschriebenen Funktionen implementieren.</span><span class="sxs-lookup"><span data-stu-id="5daba-105">Microsoft Excel 2013 cluster connector DLLs must implement the functions described in this section.</span></span>
  
<span data-ttu-id="5daba-106">Die in den Referenzthemen in diesem Abschnitt genannten Rückgabewerte sind in der SDK-Include-Datei xlcall. h definiert.</span><span class="sxs-lookup"><span data-stu-id="5daba-106">The return values mentioned in reference topics in this section are defined in the SDK include file, xlcall.h.</span></span>
  
## <a name="cluster-connector-architecture"></a><span data-ttu-id="5daba-107">Cluster-Connector-Architektur</span><span class="sxs-lookup"><span data-stu-id="5daba-107">Cluster Connector Architecture</span></span>

<span data-ttu-id="5daba-108">Excel ruft Einstiegspunkte in einem Cluster-Konnektor auf, um benutzerdefinierte Funktionsaufrufe an einen Hochleistungs-Compute-Cluster und für die Cluster Sitzungsverwaltung zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="5daba-108">Excel calls entry points in a cluster connector to transfer user-defined function calls to a high-performance compute cluster, and for cluster session management.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="5daba-109">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="5daba-109">In this section</span></span>

[<span data-ttu-id="5daba-110">CallUDF</span><span class="sxs-lookup"><span data-stu-id="5daba-110">CallUDF</span></span>](calludf.md)
  
[<span data-ttu-id="5daba-111">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="5daba-111">CancelOutstandingRequests</span></span>](canceloutstandingrequests.md)
  
[<span data-ttu-id="5daba-112">CloseSession</span><span class="sxs-lookup"><span data-stu-id="5daba-112">CloseSession</span></span>](closesession.md)
  
[<span data-ttu-id="5daba-113">OpenSession</span><span class="sxs-lookup"><span data-stu-id="5daba-113">OpenSession</span></span>](opensession.md)
  
[<span data-ttu-id="5daba-114">PingSession</span><span class="sxs-lookup"><span data-stu-id="5daba-114">PingSession</span></span>](pingsession.md)
  
[<span data-ttu-id="5daba-115">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="5daba-115">ShowOptions</span></span>](showoptions.md)
  
## <a name="see-also"></a><span data-ttu-id="5daba-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5daba-116">See also</span></span>



[<span data-ttu-id="5daba-117">Entwickeln von Excel-Clusterconnectors</span><span class="sxs-lookup"><span data-stu-id="5daba-117">Developing Excel Cluster Connectors</span></span>](developing-excel-cluster-connectors.md)
  
[<span data-ttu-id="5daba-118">Clustersichere Funktionen</span><span class="sxs-lookup"><span data-stu-id="5daba-118">Cluster Safe Functions</span></span>](cluster-safe-functions.md)

