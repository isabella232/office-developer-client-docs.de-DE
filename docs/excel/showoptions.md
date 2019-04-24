---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 5b58b71dc4f2441448eb3e0dac2c3c5763675927
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310427"
---
# <a name="showoptions"></a><span data-ttu-id="14f42-103">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="14f42-103">ShowOptions</span></span>

<span data-ttu-id="14f42-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="14f42-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="14f42-105">Zeigt ein modales Dialogfeld zum Erfassen von Informationen vom Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="14f42-105">Shows a modal dialog box to collect information from the user.</span></span> <span data-ttu-id="14f42-106">Dieser Einstiegspunkt wird aufgerufen, wenn ein Benutzer auf die Schaltfläche **Optionen** neben \*\*\*\* dem Feld Clustertyp für den ausgewählten Cluster-Konnektor im Dialogfeld **Excel-Optionen** klickt (in der Kategorie **erweitert** unter dem Abschnitt **Formeln** ).</span><span class="sxs-lookup"><span data-stu-id="14f42-106">This entry point is called when a user clicks the **Options** button next to the **Cluster type** box for the selected cluster connector in the **Excel Options** dialog box (in the **Advanced** category under the **Formulas** section).</span></span> <span data-ttu-id="14f42-107">Cluster-Konnektoren sind für die Implementierung einer eigenen Options Dialogfeld-Schnittstelle und zum Speichern der zugehörigen Daten in der Registrierung oder an einem anderen Ort zuständig.</span><span class="sxs-lookup"><span data-stu-id="14f42-107">Cluster connectors are responsible for implementing their own options dialog interface and for storing the related data in the registry or elsewhere.</span></span> <span data-ttu-id="14f42-108">Die Optionen sind intern für den Cluster-Konnektor.</span><span class="sxs-lookup"><span data-stu-id="14f42-108">The options are internal to the cluster connector.</span></span> <span data-ttu-id="14f42-109">Excel erkennt Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="14f42-109">Excel is not aware of them.</span></span> 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a><span data-ttu-id="14f42-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="14f42-110">Parameters</span></span>

<span data-ttu-id="14f42-111">_hWndParent_</span><span class="sxs-lookup"><span data-stu-id="14f42-111">_hWndParent_</span></span>
  
> <span data-ttu-id="14f42-112">Ein Handle für das Excel-Fenster.</span><span class="sxs-lookup"><span data-stu-id="14f42-112">A handle to the Excel window.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="14f42-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14f42-113">Return value</span></span>

<span data-ttu-id="14f42-114">**xlHpcRetSuccess** , wenn das Dialogfeld angezeigt wurde; **xlHpcRetCallFailed** , wenn Sie nicht angezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="14f42-114">**xlHpcRetSuccess** if the dialog box was shown; **xlHpcRetCallFailed** if it was not shown.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="14f42-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14f42-115">Remarks</span></span>

<span data-ttu-id="14f42-116">Cluster-Konnektoren können dieses Dialogfeldverwenden, um Informationen wie den zu verwendenden Cluster Server vom Benutzer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="14f42-116">Cluster connectors can use this dialog box to get information, such as what cluster server to use, from the user.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="14f42-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14f42-117">See also</span></span>

- [<span data-ttu-id="14f42-118">Excel-Clusterconnector-Funktionen</span><span class="sxs-lookup"><span data-stu-id="14f42-118">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

