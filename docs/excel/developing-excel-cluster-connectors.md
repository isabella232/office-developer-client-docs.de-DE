---
title: Entwickeln von Excel-Cluster-Konnektoren
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
# <a name="developing-excel-cluster-connectors"></a><span data-ttu-id="b0d21-103">Entwickeln von Excel-Cluster-Konnektoren</span><span class="sxs-lookup"><span data-stu-id="b0d21-103">Developing Excel Cluster Connectors</span></span>

<span data-ttu-id="b0d21-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b0d21-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b0d21-105">Excel-Cluster-Konnektoren bieten eine Möglichkeit, Cluster sichere benutzerdefinierte Funktionsaufrufe in einer XLL automatisch an einen gruppierten Server zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="b0d21-105">Excel cluster connectors provide a means for automatically offloading cluster-safe user-defined function calls in an XLL to a clustered server.</span></span> <span data-ttu-id="b0d21-106">Eine Beschreibung der Cluster sicheren benutzerdefinierten Funktionen finden Sie unter [Cluster Safe Functions](cluster-safe-functions.md).</span><span class="sxs-lookup"><span data-stu-id="b0d21-106">For a description of cluster-safe user-defined functions, see [Cluster Safe Functions](cluster-safe-functions.md).</span></span> <span data-ttu-id="b0d21-107">Diese Verschiebung kann die Leistung verbessern, indem mehr Computerressourcen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="b0d21-107">This offloading can improve performance by enabling more computing resources to be used.</span></span> <span data-ttu-id="b0d21-108">Ein Cluster-Konnektor wird in der Regel von einem Hochleistungs-Compute-Cluster-Anbieter entwickelt.</span><span class="sxs-lookup"><span data-stu-id="b0d21-108">A cluster connector is typically developed by a high performance compute cluster vendor.</span></span>
  
## <a name="cluster-connectors"></a><span data-ttu-id="b0d21-109">Cluster-Konnektoren</span><span class="sxs-lookup"><span data-stu-id="b0d21-109">Cluster Connectors</span></span>

<span data-ttu-id="b0d21-110">Ein Cluster-Konnektor ist eine DLL, die definierte Einstiegspunkte bereitstellt, die Excel zum Koordinieren von Cluster sicheren benutzerdefinierten Funktionsaufrufen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b0d21-110">A cluster connector is a DLL that provides defined entry points that Excel uses to coordinate cluster-safe user-defined function calls.</span></span> <span data-ttu-id="b0d21-111">Sie dient als Schnittstelle zwischen Excel und dem Hochleistungs-Compute-Cluster, für die Sitzungsverwaltung, für Funktionsaufrufe (durch Übergeben des vollqualifizierten Funktionsnamens und der tatsächlichen Argumente des Aufrufs) sowie für das Zurückgeben von Anruf Ergebnissen an Excel über eine Callback-Mechanismus.</span><span class="sxs-lookup"><span data-stu-id="b0d21-111">It serves as an interface between Excel and the high-performance compute cluster, for session management, for making function calls (by passing the fully-qualified function name and the call's actual arguments), and for returning call results to Excel through a callback mechanism.</span></span>
  
<span data-ttu-id="b0d21-112">Erstellen Sie zum Erstellen eines Cluster-Konnektors eine DLL, die die in den [Excel-Cluster](excel-cluster-connector-functions.md)-konnektorfunktionen aufgeführten Einstiegspunkte verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="b0d21-112">To create a cluster connector, create a DLL that exposes the entry points listed in [Excel Cluster Connector Functions](excel-cluster-connector-functions.md).</span></span>
  
## <a name="installing-a-cluster-connector"></a><span data-ttu-id="b0d21-113">Installieren eines Cluster-Konnektors</span><span class="sxs-lookup"><span data-stu-id="b0d21-113">Installing a Cluster Connector</span></span>

<span data-ttu-id="b0d21-114">Damit ein Cluster-Konnektor in Excel verfügbar ist, muss der Setup-Code des Connectors die DLL des Connectors auf dem Computer installieren, auf dem Excel installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b0d21-114">To make a cluster connector available in Excel, the setup code of the connector must install the DLL of the connector on the computer where Excel is installed.</span></span> <span data-ttu-id="b0d21-115">Darüber hinaus muss der Setup-Code des Connectors einen Eintrag für den Connector unter dem folgenden Registrierungsschlüssel hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="b0d21-115">In addition, the setup code of the connector must add an entry for the connector under the following registry key:</span></span>
  
<span data-ttu-id="b0d21-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel-Cluster-Connectors \\</span><span class="sxs-lookup"><span data-stu-id="b0d21-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\\</span></span>
  
<span data-ttu-id="b0d21-117">Fügen Sie diesem Schlüssel einen Knoten für den Cluster-Konnektor hinzu, der die folgenden Zeichenfolgen angibt:</span><span class="sxs-lookup"><span data-stu-id="b0d21-117">Add a node to this key for the cluster connector that specifies the following strings:</span></span>
  
-  <span data-ttu-id="b0d21-118">`Name`– der Name, der in der Liste der Cluster-Konnektoren in Excel angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b0d21-118">`Name`—the name that will appear in the list of cluster connectors in Excel.</span></span>
    
-  <span data-ttu-id="b0d21-119">`Filename`– der vollständige Pfad für die DLL.</span><span class="sxs-lookup"><span data-stu-id="b0d21-119">`Filename`—the full path for the DLL.</span></span>
    

