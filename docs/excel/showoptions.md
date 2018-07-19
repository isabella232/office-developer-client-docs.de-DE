---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: dbf6f0f50e9f7fa988e83f3b58012e9deac13eac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790568"
---
# <a name="showoptions"></a><span data-ttu-id="55e95-103">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="55e95-103">ShowOptions</span></span>

<span data-ttu-id="55e95-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="55e95-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="55e95-105">Zeigt ein modales Dialogfeld zum Sammeln von Informationen vom Benutzer.</span><span class="sxs-lookup"><span data-stu-id="55e95-105">Shows a modal dialog box to collect information from the user.</span></span> <span data-ttu-id="55e95-106">Dieser Einstiegspunkt wird aufgerufen, wenn ein Benutzer auf die Schaltfläche **Optionen** neben dem Feld **Clustertyp** für die ausgewählten Clusterconnector (in der Kategorie **Erweitert** im Abschnitt **Formeln** ) im Dialogfeld **Excel-Optionen** klickt.</span><span class="sxs-lookup"><span data-stu-id="55e95-106">This entry point is called when a user clicks the **Options** button next to the **Cluster type** box for the selected cluster connector in the **Excel Options** dialog box (in the **Advanced** category under the **Formulas** section).</span></span> <span data-ttu-id="55e95-107">Clusterconnectoren sind verantwortlich für die Implementierung ihrer eigenen Optionen Dialogfeld-Schnittstelle und zum Speichern der verknüpften Daten in der Registrierung oder an anderer Stelle.</span><span class="sxs-lookup"><span data-stu-id="55e95-107">Cluster connectors are responsible for implementing their own options dialog interface and for storing the related data in the registry or elsewhere.</span></span> <span data-ttu-id="55e95-108">Die Optionen sind in der Clusterconnector interne.</span><span class="sxs-lookup"><span data-stu-id="55e95-108">The options are internal to the cluster connector.</span></span> <span data-ttu-id="55e95-109">Excel ist nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="55e95-109">Excel is not aware of them.</span></span> 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a><span data-ttu-id="55e95-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="55e95-110">Parameters</span></span>

<span data-ttu-id="55e95-111">_hWndParent_</span><span class="sxs-lookup"><span data-stu-id="55e95-111">_hWndParent_</span></span>
  
> <span data-ttu-id="55e95-112">Ein Handle für das Excel-Fenster.</span><span class="sxs-lookup"><span data-stu-id="55e95-112">A handle to the Excel window.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="55e95-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55e95-113">Return value</span></span>

<span data-ttu-id="55e95-114">**XlHpcRetSuccess** , wenn das Dialogfeld angezeigt wurde; **XlHpcRetCallFailed** , wenn er nicht angezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="55e95-114">**xlHpcRetSuccess** if the dialog box was shown; **xlHpcRetCallFailed** if it was not shown.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="55e95-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="55e95-115">Remarks</span></span>

<span data-ttu-id="55e95-116">In diesem Dialogfeld können clusterconnectoren zum Abrufen von Informationen, beispielsweise welche Clusterserver aus der Benutzer verwenden.</span><span class="sxs-lookup"><span data-stu-id="55e95-116">Cluster connectors can use this dialog box to get information, such as what cluster server to use, from the user.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="55e95-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55e95-117">See also</span></span>

- [<span data-ttu-id="55e95-118">Excel-Clusterconnector-Funktionen</span><span class="sxs-lookup"><span data-stu-id="55e95-118">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

