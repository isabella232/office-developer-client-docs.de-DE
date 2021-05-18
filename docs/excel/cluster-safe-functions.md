---
title: Clustersichere Funktionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 787badaf-8782-454d-a016-7eae83bbd8a9
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d32925fcd5c3be7fe3e615ee2290f25c7595911c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409300"
---
# <a name="cluster-safe-functions"></a><span data-ttu-id="3de83-103">Clustersichere Funktionen</span><span class="sxs-lookup"><span data-stu-id="3de83-103">Cluster safe functions</span></span>

<span data-ttu-id="3de83-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3de83-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3de83-105">In Excel 2013 können Excel aufrufe von User-Defined (UDF) über eine dedizierte Clusterconnectorschnittstelle an einen Hochleistungscomputercluster ausladen.</span><span class="sxs-lookup"><span data-stu-id="3de83-105">In Excel 2013, Excel can offload User-Defined Function (UDF) calls to a high-performance computing cluster through a dedicated cluster connector interface.</span></span> <span data-ttu-id="3de83-106">Computeclusteranbieter stellen Clusterconnectors zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="3de83-106">Compute cluster vendors provide Cluster Connectors.</span></span> <span data-ttu-id="3de83-107">UDF-Autoren können ihre UDFs als clustersicher deklarieren und dann, wenn ein Clusterconnector vorhanden ist, Excel Aufrufe an diese UDFs zum Offloading an den Clusterconnector senden.</span><span class="sxs-lookup"><span data-stu-id="3de83-107">UDF authors can declare their UDFs as cluster safe and then, when a cluster connector is present, Excel sends calls to these UDFs to the cluster connector for offloading.</span></span>
  
<span data-ttu-id="3de83-108">Wenn Excel bei der Neuberechnung eine clustersichere UDF ermittelt, übergibt sie den Namen der aktuell ausgeführten XLL, den Namen der clustersicheren UDF und alle Parameter an den Clusterconnector.</span><span class="sxs-lookup"><span data-stu-id="3de83-108">When Excel discovers a cluster-safe UDF during recalculation, it passes the name of the XLL that is currently running, the name of the cluster-safe UDF, and any parameters to the cluster connector.</span></span> <span data-ttu-id="3de83-109">Der Connector führt den UDF-Aufruf remote aus und gibt die Ergebnisse an Excel.</span><span class="sxs-lookup"><span data-stu-id="3de83-109">The connector runs the UDF call remotely and returns the results to Excel.</span></span> <span data-ttu-id="3de83-110">Die nicht abhängige Berechnung wird fortgesetzt, und wenn der Clusterconnector die Ausführung der UDF beendet hat, werden die Ergebnisse an Excel und abhängige Berechnungen fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="3de83-110">Non-dependent calculation continues and when the cluster connector has finished running the UDF, it passes the results to Excel and dependent calculations continue.</span></span> <span data-ttu-id="3de83-111">Der Mechanismus für dieses asynchrone Verhalten imitiert den mechanismus, der von asynchronen UDFs verwendet wird, mit der Ausnahme, dass der Clusterconnector die asynchronen Aspekte anstelle des UDF-Autors verwaltet.</span><span class="sxs-lookup"><span data-stu-id="3de83-111">The mechanism for this asynchronous behavior mimics the mechanism used by asynchronous UDFs, except that the cluster connector manages the asynchronous aspects instead of the UDF author.</span></span> <span data-ttu-id="3de83-112">In der Regel implementiert ein Clusterconnector einen XLL-Shim zum Laden von XLLs und Ausführen von UDFs auf Computeclusterknoten.</span><span class="sxs-lookup"><span data-stu-id="3de83-112">Typically, a cluster connector implements an XLL shim to load XLLs and run UDFs on compute cluster nodes.</span></span>
  
<span data-ttu-id="3de83-113">Die Mechanik der Deklarierung von UDFs als clustersicher ähnelt denen der Deklarierung von UDFs als sicher für die Neuberechnung mit mehreren Threads.</span><span class="sxs-lookup"><span data-stu-id="3de83-113">The mechanics of declaring UDFs as cluster-safe resemble those of declaring UDFs as safe for multi-threaded recalculation.</span></span> <span data-ttu-id="3de83-114">Da die UDF jedoch nicht unbedingt auf demselben Computer wie andere UDFs aus derselben Excel-Sitzung ausgeführt wird, gibt es beim Schreiben clustersicherer UDFs unterschiedliche Überlegungen.</span><span class="sxs-lookup"><span data-stu-id="3de83-114">However, because the UDF is not necessarily running on the same computer as other UDFs from the same Excel session, there are different considerations when writing cluster-safe UDFs.</span></span>
  
<span data-ttu-id="3de83-115">Um eine UDF als clustersicher zu registrieren, müssen Sie die [xlfRegister (Form 1)-Rückruffunktion](xlfregister-form-1.md) über die **Excel12-** oder **Excel12v-Schnittstelle** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3de83-115">To register a UDF as cluster-safe, you must call the [xlfRegister (Form 1)](xlfregister-form-1.md) callback function through the **Excel12** or **Excel12v** interface.</span></span> <span data-ttu-id="3de83-116">Weitere Informationen zu diesen Schnittstellen finden Sie unter [Excel4/Excel12](excel4-excel12.md) und [Excel4v/Excel12v](excel4v-excel12v.md).</span><span class="sxs-lookup"><span data-stu-id="3de83-116">For more information about these interfaces, see the [Excel4/Excel12](excel4-excel12.md) and [Excel4v/Excel12v](excel4v-excel12v.md).</span></span> <span data-ttu-id="3de83-117">Die Registrierung einer UDF als clustersicher über die **Excel4-** oder **Excel4v-Schnittstelle** wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3de83-117">Registering a UDF as cluster-safe through the **Excel4** or **Excel4v** interface is not supported.</span></span> 
  
<span data-ttu-id="3de83-118">Wenn Sie eine Funktion als clustersicher registrieren, müssen Sie sicherstellen, dass sich die Funktion clustersicher verhält.</span><span class="sxs-lookup"><span data-stu-id="3de83-118">If you register a function as cluster-safe, you must ensure that the function behaves in a cluster-safe way.</span></span> <span data-ttu-id="3de83-119">Obwohl das genaue Verhalten des Clusterconnector implementierungsspezifisch ist, sollten Sie Ihre UDF so entwerfen, dass sie auf einem verteilten Computersystem ausgeführt wird und die folgenden Merkmale aufweist:</span><span class="sxs-lookup"><span data-stu-id="3de83-119">Although the exact behavior of the cluster connector is implementation-specific, you should design your UDF to run on a distributed computer system and to have the following characteristics:</span></span>
  
- <span data-ttu-id="3de83-120">Ein UDF sollte sich nicht auf einen Speicherstatus verlassen.</span><span class="sxs-lookup"><span data-stu-id="3de83-120">A UDF should not rely on any memory state.</span></span> <span data-ttu-id="3de83-121">Beispielsweise sollte sich ein UDF nicht auf einen vorhandenen Speichercache verlassen.</span><span class="sxs-lookup"><span data-stu-id="3de83-121">For example, a UDF should not rely on an existing in-memory cache.</span></span>
    
- <span data-ttu-id="3de83-122">Ein UDF sollte keine Excel ausführen, die vom Clusterconnectoranbieter nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3de83-122">A UDF should not perform Excel callbacks that the cluster connector provider does not support.</span></span>
    
<span data-ttu-id="3de83-123">Neben dem clustersicheren Verhalten gibt es die folgenden technischen Einschränkungen für clustersichere UDFs:</span><span class="sxs-lookup"><span data-stu-id="3de83-123">In addition to cluster-safe behavior, there are the following technical restrictions on cluster-safe UDFs:</span></span>
  
1. <span data-ttu-id="3de83-124">Keine XLOPER-Argumente (Typen 'P', 'R').</span><span class="sxs-lookup"><span data-stu-id="3de83-124">No XLOPER arguments (types 'P', 'R').</span></span>
    
2. <span data-ttu-id="3de83-125">Keine XLOPER12-Argumente, die Bereichsverweise unterstützen (Typ 'U').</span><span class="sxs-lookup"><span data-stu-id="3de83-125">No XLOPER12 arguments that support range references (type 'U').</span></span>
    
3. <span data-ttu-id="3de83-126">Es kann sich nicht um eine makroblattäquivalente Funktion ('#' und &amp; ' ' kann nicht kombiniert werden).</span><span class="sxs-lookup"><span data-stu-id="3de83-126">Cannot be a macro sheet equivalent function ('#' and '&amp;' cannot be combined).</span></span>
    
<span data-ttu-id="3de83-127">Bei UDFs mit kürzeren Ausführungszeiten kann der Aufwand für das Offloading größer sein als die Ausführungszeit der UDF, was viele vorteile der Verwendung dieser Infrastruktur negiert.</span><span class="sxs-lookup"><span data-stu-id="3de83-127">For UDFs with shorter execution times, the overhead of offloading may be larger than the time it takes the UDF to execute, negating many of the benefits of using this infrastructure.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3de83-128">Sie können eine clustersichere UDF nicht als asynchrones UDF deklarieren.</span><span class="sxs-lookup"><span data-stu-id="3de83-128">You cannot declare a cluster-safe UDF as an asynchronous UDF.</span></span> 
  
<span data-ttu-id="3de83-129">Eine UDF kann ermitteln, ob sie mit einem Clusterconnector ausgeführt wird, indem sie die [xlRunningOnCluster-Rückruffunktion](xlrunningoncluster.md) aufruft.</span><span class="sxs-lookup"><span data-stu-id="3de83-129">A UDF can determine whether it is being run using a cluster connector by calling the [xlRunningOnCluster](xlrunningoncluster.md) callback function.</span></span> 
  

