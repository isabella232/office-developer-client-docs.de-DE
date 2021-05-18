---
title: GOTOPAGE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251432
localization_priority: Normal
ms.assetid: b131badf-1656-132e-0aae-eeedb917ba7a
description: Zeigt die Seite mit dem Namen pagename im aktuell aktiven Fenster an.
ms.openlocfilehash: c96585406b6104aeedbe46c35024a4f13bb0953e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302968"
---
# <a name="gotopage-function"></a><span data-ttu-id="fbf84-103">GOTOPAGE Function</span><span class="sxs-lookup"><span data-stu-id="fbf84-103">GOTOPAGE Function</span></span>

<span data-ttu-id="fbf84-104">Zeigt die Seite mit dem Namen  *pagename*  im aktuell aktiven Fenster an.</span><span class="sxs-lookup"><span data-stu-id="fbf84-104">Displays the page that has the name  *pagename*  in the currently active window.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fbf84-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbf84-105">Syntax</span></span>

<span data-ttu-id="fbf84-106">GOTOPAGE(" \*\* *pagename* \*\* ")</span><span class="sxs-lookup"><span data-stu-id="fbf84-106">GOTOPAGE(" \*\* *pagename* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fbf84-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbf84-107">Parameters</span></span>

|<span data-ttu-id="fbf84-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="fbf84-108">**Name**</span></span>|<span data-ttu-id="fbf84-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="fbf84-109">**Required/Optional**</span></span>|<span data-ttu-id="fbf84-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="fbf84-110">**Data Type**</span></span>|<span data-ttu-id="fbf84-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fbf84-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fbf84-112">_pagename_</span><span class="sxs-lookup"><span data-stu-id="fbf84-112">_pagename_</span></span> <br/> |<span data-ttu-id="fbf84-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fbf84-113">Required</span></span>  <br/> |<span data-ttu-id="fbf84-114">**String**</span><span class="sxs-lookup"><span data-stu-id="fbf84-114">**String**</span></span> <br/> |<span data-ttu-id="fbf84-115">Der Name des Zeichenblatts, zu dem gewechselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fbf84-115">The name of the page to go to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fbf84-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fbf84-116">Remarks</span></span>

<span data-ttu-id="fbf84-117">Wenn die Seite bereits in einem Fenster angezeigt wird, wird dieses Fenster aktiv.</span><span class="sxs-lookup"><span data-stu-id="fbf84-117">If a window is already displaying the page, that window becomes active.</span></span> <span data-ttu-id="fbf84-118">Wenn  *pagename*  nicht vorhanden ist, versucht die Anwendung, zu https://  *Pagename /zu*  navigieren.</span><span class="sxs-lookup"><span data-stu-id="fbf84-118">If  *pagename*  does not exist, the application attempts to navigate to https://  *pagename*  /.</span></span> <span data-ttu-id="fbf84-119">Wenn Visio als in-Place-Server agiert, hat die GOTOPAGE-Funktion keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="fbf84-119">If Visio is acting as an in-place server, the GOTOPAGE function has no effect.</span></span> 
  
<span data-ttu-id="fbf84-120">Sie können die HYPERLINK-Funktion verwenden, um zu einem beliebigen DOS-, UNC- oder URL-Pfad zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="fbf84-120">You can use the HYPERLINK function to navigate to any DOS, UNC, or URL path.</span></span> 
  
<span data-ttu-id="fbf84-p102">In früheren Visio-Produktversionen wird diese Funktion in der Form _GOTOPAGE angezeigt. In den Visio-Versionen 4.0 und höher werden beide Schreibweisen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="fbf84-p102">In earlier versions of Visio products, this function appears as _GOTOPAGE. Visio versions 4.0 and later accept either style.</span></span> 
  

