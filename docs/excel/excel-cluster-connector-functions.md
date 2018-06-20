---
title: Excel-Clusterconnector-Funktionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4a069aa4ed3ee17320ac65ab793ea8812153cc18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790423"
---
# <a name="excel-cluster-connector-functions"></a><span data-ttu-id="19502-103">Excel-Clusterconnector-Funktionen</span><span class="sxs-lookup"><span data-stu-id="19502-103">Excel Cluster Connector Functions</span></span>

 <span data-ttu-id="19502-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="19502-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="19502-105">Microsoft Excel 2013-Clusterconnector DLLs muss die Funktionen, die in diesem Abschnitt beschriebenen implementieren.</span><span class="sxs-lookup"><span data-stu-id="19502-105">Microsoft Excel 2013 cluster connector DLLs must implement the functions described in this section.</span></span>
  
<span data-ttu-id="19502-106">Die Rückgabewerte in Referenz zu den Themen in diesem Abschnitt werden im SDK definiert erwähnten include-Datei, xlcall.h.</span><span class="sxs-lookup"><span data-stu-id="19502-106">The return values mentioned in reference topics in this section are defined in the SDK include file, xlcall.h.</span></span>
  
## <a name="cluster-connector-architecture"></a><span data-ttu-id="19502-107">Connector-Clusterarchitektur</span><span class="sxs-lookup"><span data-stu-id="19502-107">Cluster Connector Architecture</span></span>

<span data-ttu-id="19502-108">Excel ruft Einstiegspunkte in einen Clusterconnector zum Übertragen von einer benutzerdefinierten Funktion-Aufrufe zu einem High Performance Computecluster und für die Sitzung Clusterverwaltung.</span><span class="sxs-lookup"><span data-stu-id="19502-108">Excel calls entry points in a cluster connector to transfer user-defined function calls to a high-performance compute cluster, and for cluster session management.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="19502-109">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="19502-109">In this section</span></span>

[<span data-ttu-id="19502-110">CallUDF</span><span class="sxs-lookup"><span data-stu-id="19502-110">CallUDF</span></span>](calludf.md)
  
[<span data-ttu-id="19502-111">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="19502-111">CancelOutstandingRequests</span></span>](canceloutstandingrequests.md)
  
[<span data-ttu-id="19502-112">CloseSession</span><span class="sxs-lookup"><span data-stu-id="19502-112">CloseSession</span></span>](closesession.md)
  
[<span data-ttu-id="19502-113">OpenSession</span><span class="sxs-lookup"><span data-stu-id="19502-113">OpenSession</span></span>](opensession.md)
  
[<span data-ttu-id="19502-114">PingSession</span><span class="sxs-lookup"><span data-stu-id="19502-114">PingSession</span></span>](pingsession.md)
  
[<span data-ttu-id="19502-115">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="19502-115">ShowOptions</span></span>](showoptions.md)
  
## <a name="see-also"></a><span data-ttu-id="19502-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19502-116">See also</span></span>



[<span data-ttu-id="19502-117">Entwickeln von Excel 2013-Clusterconnectoren</span><span class="sxs-lookup"><span data-stu-id="19502-117">Developing Excel Cluster Connectors</span></span>](developing-excel-cluster-connectors.md)
  
[<span data-ttu-id="19502-118">Clustersichere Funktionen</span><span class="sxs-lookup"><span data-stu-id="19502-118">Cluster Safe Functions</span></span>](cluster-safe-functions.md)

