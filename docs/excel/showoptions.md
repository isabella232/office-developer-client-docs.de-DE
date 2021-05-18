---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5b58b71dc4f2441448eb3e0dac2c3c5763675927
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407697"
---
# <a name="showoptions"></a><span data-ttu-id="e75c2-103">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="e75c2-103">ShowOptions</span></span>

<span data-ttu-id="e75c2-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e75c2-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e75c2-105">Zeigt ein modales Dialogfeld zum Sammeln von Informationen vom Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="e75c2-105">Shows a modal dialog box to collect information from the user.</span></span> <span data-ttu-id="e75c2-106">Dieser Einstiegspunkt wird aufgerufen, wenn  ein Benutzer  im Dialogfeld **Excel-Optionen** (in der Kategorie Erweitert unter dem  Abschnitt **Formeln)** neben dem Feld Clustertyp auf die Schaltfläche Optionen für den ausgewählten Clusterconnector klickt.</span><span class="sxs-lookup"><span data-stu-id="e75c2-106">This entry point is called when a user clicks the **Options** button next to the **Cluster type** box for the selected cluster connector in the **Excel Options** dialog box (in the **Advanced** category under the **Formulas** section).</span></span> <span data-ttu-id="e75c2-107">Clusterconnectors sind für die Implementierung ihrer eigenen Dialogschnittstelle für Optionen und das Speichern der zugehörigen Daten in der Registrierung oder an anderer Stelle verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="e75c2-107">Cluster connectors are responsible for implementing their own options dialog interface and for storing the related data in the registry or elsewhere.</span></span> <span data-ttu-id="e75c2-108">Die Optionen sind intern für den Clusterconnector.</span><span class="sxs-lookup"><span data-stu-id="e75c2-108">The options are internal to the cluster connector.</span></span> <span data-ttu-id="e75c2-109">Excel sie nicht kennen.</span><span class="sxs-lookup"><span data-stu-id="e75c2-109">Excel is not aware of them.</span></span> 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a><span data-ttu-id="e75c2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e75c2-110">Parameters</span></span>

<span data-ttu-id="e75c2-111">_hWndParent_</span><span class="sxs-lookup"><span data-stu-id="e75c2-111">_hWndParent_</span></span>
  
> <span data-ttu-id="e75c2-112">Ein Handle zum Excel Fenster.</span><span class="sxs-lookup"><span data-stu-id="e75c2-112">A handle to the Excel window.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e75c2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e75c2-113">Return value</span></span>

<span data-ttu-id="e75c2-114">**xlHpcRetSuccess,** wenn das Dialogfeld angezeigt wurde; **xlHpcRetCallFailed,** wenn es nicht angezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="e75c2-114">**xlHpcRetSuccess** if the dialog box was shown; **xlHpcRetCallFailed** if it was not shown.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e75c2-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e75c2-115">Remarks</span></span>

<span data-ttu-id="e75c2-116">Clusterconnectors können dieses Dialogfeld verwenden, um Informationen, z. B. den zu verwendende Clusterserver, vom Benutzer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e75c2-116">Cluster connectors can use this dialog box to get information, such as what cluster server to use, from the user.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e75c2-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e75c2-117">See also</span></span>

- [<span data-ttu-id="e75c2-118">Excel-Clusterconnector-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e75c2-118">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

