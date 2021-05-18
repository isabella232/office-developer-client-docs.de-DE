---
title: Entwickeln Excel Clusterconnectors
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e1c70713586a7a143f119a2c3e9d34b982dcedba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412597"
---
# <a name="developing-excel-cluster-connectors"></a><span data-ttu-id="94488-103">Entwickeln Excel Clusterconnectors</span><span class="sxs-lookup"><span data-stu-id="94488-103">Developing Excel Cluster Connectors</span></span>

<span data-ttu-id="94488-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="94488-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="94488-105">Excel Clusterconnectors bieten eine Möglichkeit zum automatischen Ausladen von clustersicheren benutzerdefinierten Funktionsaufrufen in einer XLL an einen gruppierten Server.</span><span class="sxs-lookup"><span data-stu-id="94488-105">Excel cluster connectors provide a means for automatically offloading cluster-safe user-defined function calls in an XLL to a clustered server.</span></span> <span data-ttu-id="94488-106">Eine Beschreibung der clustersicheren benutzerdefinierten Funktionen finden Sie unter [Cluster Safe Functions](cluster-safe-functions.md).</span><span class="sxs-lookup"><span data-stu-id="94488-106">For a description of cluster-safe user-defined functions, see [Cluster Safe Functions](cluster-safe-functions.md).</span></span> <span data-ttu-id="94488-107">Dieses Offloading kann die Leistung verbessern, indem mehr Rechenressourcen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="94488-107">This offloading can improve performance by enabling more computing resources to be used.</span></span> <span data-ttu-id="94488-108">Ein Clusterconnector wird in der Regel von einem Anbieter von Hochleistungs-Computeclustern entwickelt.</span><span class="sxs-lookup"><span data-stu-id="94488-108">A cluster connector is typically developed by a high performance compute cluster vendor.</span></span>
  
## <a name="cluster-connectors"></a><span data-ttu-id="94488-109">Clusterconnectors</span><span class="sxs-lookup"><span data-stu-id="94488-109">Cluster Connectors</span></span>

<span data-ttu-id="94488-110">Ein Clusterconnector ist eine DLL, die definierte Einstiegspunkte Excel, die zum Koordinieren von clustersicheren benutzerdefinierten Funktionsaufrufen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="94488-110">A cluster connector is a DLL that provides defined entry points that Excel uses to coordinate cluster-safe user-defined function calls.</span></span> <span data-ttu-id="94488-111">Sie dient als Schnittstelle zwischen Excel und dem Hochleistungs-Computecluster, für die Sitzungsverwaltung, für Funktionsaufrufe (durch Übergeben des vollqualifizierten Funktionsnamens und der tatsächlichen Argumente des Aufrufs) und zum Zurückgeben von Anrufergebnissen an Excel über einen Rückrufmechanismus.</span><span class="sxs-lookup"><span data-stu-id="94488-111">It serves as an interface between Excel and the high-performance compute cluster, for session management, for making function calls (by passing the fully-qualified function name and the call's actual arguments), and for returning call results to Excel through a callback mechanism.</span></span>
  
<span data-ttu-id="94488-112">Um einen Clusterconnector zu erstellen, erstellen Sie eine DLL, die die einstiegspunkte verfügbar macht, die in Excel [Clusterconnectorfunktionen aufgeführt sind.](excel-cluster-connector-functions.md)</span><span class="sxs-lookup"><span data-stu-id="94488-112">To create a cluster connector, create a DLL that exposes the entry points listed in [Excel Cluster Connector Functions](excel-cluster-connector-functions.md).</span></span>
  
## <a name="installing-a-cluster-connector"></a><span data-ttu-id="94488-113">Installieren eines Clusterconnector</span><span class="sxs-lookup"><span data-stu-id="94488-113">Installing a Cluster Connector</span></span>

<span data-ttu-id="94488-114">Um einen Clusterconnector in Excel verfügbar zu machen, muss der Setupcode des Connectors die DLL des Connectors auf dem Computer installieren, auf dem Excel installiert ist.</span><span class="sxs-lookup"><span data-stu-id="94488-114">To make a cluster connector available in Excel, the setup code of the connector must install the DLL of the connector on the computer where Excel is installed.</span></span> <span data-ttu-id="94488-115">Darüber hinaus muss der Setupcode des Connectors einen Eintrag für den Connector unter dem folgenden Registrierungsschlüssel hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="94488-115">In addition, the setup code of the connector must add an entry for the connector under the following registry key:</span></span>
  
<span data-ttu-id="94488-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors</span><span class="sxs-lookup"><span data-stu-id="94488-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors</span></span>\
  
<span data-ttu-id="94488-117">Fügen Sie diesem Schlüssel für den Clusterconnector einen Knoten hinzu, der die folgenden Zeichenfolgen angibt:</span><span class="sxs-lookup"><span data-stu-id="94488-117">Add a node to this key for the cluster connector that specifies the following strings:</span></span>
  
-  <span data-ttu-id="94488-118">`Name`– der Name, der in der Liste der Clusterconnectors in Excel.</span><span class="sxs-lookup"><span data-stu-id="94488-118">`Name`—the name that will appear in the list of cluster connectors in Excel.</span></span>
    
-  <span data-ttu-id="94488-119">`Filename`– der vollständige Pfad für die DLL.</span><span class="sxs-lookup"><span data-stu-id="94488-119">`Filename`—the full path for the DLL.</span></span>
    

