---
title: Entwickeln von Excel-Clusterconnectoren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8c9a166ac06685c0a450e1e0bd60b2fbef67d336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790386"
---
# <a name="developing-excel-cluster-connectors"></a><span data-ttu-id="feeb7-103">Entwickeln von Excel-Clusterconnectoren</span><span class="sxs-lookup"><span data-stu-id="feeb7-103">Developing Excel Cluster Connectors</span></span>

<span data-ttu-id="feeb7-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="feeb7-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="feeb7-105">Excel-clusterconnectoren bieten eine Möglichkeit zum Aufrufen der clustersichere benutzerdefinierte Funktion in einer XLL für einen gruppierten Server automatisch verlagern.</span><span class="sxs-lookup"><span data-stu-id="feeb7-105">Excel cluster connectors provide a means for automatically offloading cluster-safe user-defined function calls in an XLL to a clustered server.</span></span> <span data-ttu-id="feeb7-106">Eine Beschreibung der benutzerdefinierten Funktionen clustersichere finden Sie unter [Clustersichere Funktionen](cluster-safe-functions.md).</span><span class="sxs-lookup"><span data-stu-id="feeb7-106">For a description of cluster-safe user-defined functions, see [Cluster Safe Functions](cluster-safe-functions.md).</span></span> <span data-ttu-id="feeb7-107">Diese Verschiebung kann Leistung verbessern, indem Sie weitere Netzwerke-Ressourcen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="feeb7-107">This offloading can improve performance by enabling more computing resources to be used.</span></span> <span data-ttu-id="feeb7-108">Ein Clusterconnector wird in der Regel durch eine hohe Leistung Compute Cluster Hersteller entwickelt.</span><span class="sxs-lookup"><span data-stu-id="feeb7-108">A cluster connector is typically developed by a high performance compute cluster vendor.</span></span>
  
## <a name="cluster-connectors"></a><span data-ttu-id="feeb7-109">Clusterconnectoren</span><span class="sxs-lookup"><span data-stu-id="feeb7-109">Cluster Connectors</span></span>

<span data-ttu-id="feeb7-110">Ein Clusterconnector ist, dass eine DLL, die definierten Einstiegspunkte, um Excel bietet wird verwendet, um benutzerdefinierte Funktion clustersichere Anrufe zu koordinieren.</span><span class="sxs-lookup"><span data-stu-id="feeb7-110">A cluster connector is a DLL that provides defined entry points that Excel uses to coordinate cluster-safe user-defined function calls.</span></span> <span data-ttu-id="feeb7-111">Dient als Schnittstelle zwischen Excel und leistungsfähige Computerclusters für Sitzung Management, zum Beschleunigen des Funktion aufruft (durch das übergeben den Namen der Funktion voll qualifizierte und den Anruf übergebene Argumente) und für die Rückgabe der Ergebnisse nach Excel über eine Rückrufmechanismus.</span><span class="sxs-lookup"><span data-stu-id="feeb7-111">It serves as an interface between Excel and the high-performance compute cluster, for session management, for making function calls (by passing the fully-qualified function name and the call's actual arguments), and for returning call results to Excel through a callback mechanism.</span></span>
  
<span data-ttu-id="feeb7-112">Um einen Clusterconnector zu erstellen, erstellen Sie eine DLL, die die Einstiegspunkte aufgeführt, die in [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="feeb7-112">To create a cluster connector, create a DLL that exposes the entry points listed in [Excel Cluster Connector Functions](excel-cluster-connector-functions.md).</span></span>
  
## <a name="installing-a-cluster-connector"></a><span data-ttu-id="feeb7-113">Installieren eines Clusterconnectors</span><span class="sxs-lookup"><span data-stu-id="feeb7-113">Installing a Cluster Connector</span></span>

<span data-ttu-id="feeb7-114">Der Setupcode der Verbindung muss einen Clusterconnector in Excel zur Verfügung zu stellen, die DLL der Verbindung auf dem Computer installieren, auf dem Excel installiert ist.</span><span class="sxs-lookup"><span data-stu-id="feeb7-114">To make a cluster connector available in Excel, the setup code of the connector must install the DLL of the connector on the computer where Excel is installed.</span></span> <span data-ttu-id="feeb7-115">Darüber hinaus muss der Setup-Code der Verbindung einen Eintrag für den Connector unter den folgenden Registrierungsschlüssel hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="feeb7-115">In addition, the setup code of the connector must add an entry for the connector under the following registry key:</span></span>
  
<span data-ttu-id="feeb7-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\\</span><span class="sxs-lookup"><span data-stu-id="feeb7-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\\</span></span>
  
<span data-ttu-id="feeb7-117">Fügen Sie einen Knoten auf diesen Schlüssel für den Clusterconnector, der angibt, die in der folgenden Zeichenfolgen:</span><span class="sxs-lookup"><span data-stu-id="feeb7-117">Add a node to this key for the cluster connector that specifies the following strings:</span></span>
  
-  <span data-ttu-id="feeb7-118">`Name`– der Name, der in der Liste der clusterconnectoren in Excel angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="feeb7-118">`Name`—the name that will appear in the list of cluster connectors in Excel.</span></span>
    
-  <span data-ttu-id="feeb7-119">`Filename`– der vollständige Pfad für die DLL.</span><span class="sxs-lookup"><span data-stu-id="feeb7-119">`Filename`—the full path for the DLL.</span></span>
    

