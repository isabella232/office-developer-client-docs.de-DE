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
description: Zeigt die Seite, die den Namen Pagename in das derzeit aktive Fenster hat.
ms.openlocfilehash: 67f8a79b854fd6f2ae47e39877ffcdbe4a1be5cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797117"
---
# <a name="gotopage-function"></a><span data-ttu-id="c28e8-103">GOTOPAGE Function</span><span class="sxs-lookup"><span data-stu-id="c28e8-103">GOTOPAGE Function</span></span>

<span data-ttu-id="c28e8-104">Zeigt die Seite, die den Namen *Pagename* in das derzeit aktive Fenster hat.</span><span class="sxs-lookup"><span data-stu-id="c28e8-104">Displays the page that has the name  *pagename*  in the currently active window.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c28e8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c28e8-105">Syntax</span></span>

<span data-ttu-id="c28e8-106">GOTOPAGE ("** *Pagename* **")</span><span class="sxs-lookup"><span data-stu-id="c28e8-106">GOTOPAGE(" ** *pagename* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c28e8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c28e8-107">Parameters</span></span>

|<span data-ttu-id="c28e8-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c28e8-108">**Name**</span></span>|<span data-ttu-id="c28e8-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="c28e8-109">**Required/Optional**</span></span>|<span data-ttu-id="c28e8-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="c28e8-110">**Data Type**</span></span>|<span data-ttu-id="c28e8-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c28e8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c28e8-112">_pageName_</span><span class="sxs-lookup"><span data-stu-id="c28e8-112">_pagename_</span></span> <br/> |<span data-ttu-id="c28e8-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c28e8-113">Required</span></span>  <br/> |<span data-ttu-id="c28e8-114">**String**</span><span class="sxs-lookup"><span data-stu-id="c28e8-114">**String**</span></span> <br/> |<span data-ttu-id="c28e8-115">Der Name des Zeichenblatts, zu dem gewechselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c28e8-115">The name of the page to go to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c28e8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c28e8-116">Remarks</span></span>

<span data-ttu-id="c28e8-117">Wenn ein Fenster bereits die Seite anzeigt, wird dieses Fenster aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c28e8-117">If a window is already displaying the page, that window becomes active.</span></span> <span data-ttu-id="c28e8-118">Wenn *Zeichenblattname* nicht vorhanden ist, wird die Anwendung zum Navigieren zu http:// *Pagename* versucht /.</span><span class="sxs-lookup"><span data-stu-id="c28e8-118">If  *pagename*  does not exist, the application attempts to navigate to http://  *pagename*  /.</span></span> <span data-ttu-id="c28e8-119">Wenn Visio als in-Place-Server fungiert, hat die GOTOPAGE-Funktion keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="c28e8-119">If Visio is acting as an in-place server, the GOTOPAGE function has no effect.</span></span> 
  
<span data-ttu-id="c28e8-120">Sie können die HYPERLINK-Funktion verwenden, um zu einem beliebigen DOS-, UNC- oder URL-Pfad zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="c28e8-120">You can use the HYPERLINK function to navigate to any DOS, UNC, or URL path.</span></span> 
  
<span data-ttu-id="c28e8-p102">In früheren Visio-Produktversionen wird diese Funktion in der Form _GOTOPAGE angezeigt. In den Visio-Versionen 4.0 und höher werden beide Schreibweisen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="c28e8-p102">In earlier versions of Visio products, this function appears as _GOTOPAGE. Visio versions 4.0 and later accept either style.</span></span> 
  

