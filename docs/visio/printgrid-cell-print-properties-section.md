---
title: Zelle "PrintGrid" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033794
localization_priority: Normal
ms.assetid: 0504ff7f-2274-7ae3-1f4b-a3d890dbd79a
description: Gibt an, ob beim Drucken einer Dokumentseite das Gitternetz gedruckt werden soll.
ms.openlocfilehash: 76e5b5b4e82c39cbbffbecc710f05a77dbaa6332
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797748"
---
# <a name="printgrid-cell-print-properties-section"></a><span data-ttu-id="42a6d-103">PrintGrid Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="42a6d-103">PrintGrid Cell (Print Properties Section)</span></span>

<span data-ttu-id="42a6d-104">Gibt an, ob beim Drucken einer Dokumentseite das Gitternetz gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="42a6d-104">Specifies whether to print the grid when printing a document page.</span></span>
  
|<span data-ttu-id="42a6d-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="42a6d-105">**Value**</span></span>|<span data-ttu-id="42a6d-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="42a6d-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="42a6d-107">WAHR</span><span class="sxs-lookup"><span data-stu-id="42a6d-107">TRUE</span></span>  <br/> |<span data-ttu-id="42a6d-108">Beim Drucken der Seite wird das Gitternetz gedruckt.</span><span class="sxs-lookup"><span data-stu-id="42a6d-108">Show the grid when printing this page.</span></span>  <br/> |
|<span data-ttu-id="42a6d-109">FALSCH</span><span class="sxs-lookup"><span data-stu-id="42a6d-109">FALSE</span></span>  <br/> |<span data-ttu-id="42a6d-110">Das Gitternetz wird beim Drucken der Seite nicht gedruckt (Standard).</span><span class="sxs-lookup"><span data-stu-id="42a6d-110">Do not show the grid when printing this page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42a6d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42a6d-111">Remarks</span></span>

<span data-ttu-id="42a6d-112">Dieser Wert entspricht dem Kontrollkästchen **Gitternetzlinien** auf der Registerkarte **Druckeinrichtung** im Dialogfeld **Seite einrichten** (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten** ).</span><span class="sxs-lookup"><span data-stu-id="42a6d-112">This value corresponds to the **Gridlines** check box on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="42a6d-113">Als Farbe (die Druckversion ist grau), das gedruckte Raster ist identisch mit dem in Microsoft Visio-Zeichnungsfenster angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="42a6d-113">Other than color (the printed version is gray), the printed grid is identical to the grid you see in the Microsoft Visio drawing window.</span></span> 
  
<span data-ttu-id="42a6d-114">Sie können auswählen, ob das Gitternetz auf Basis von Seite gedruckt.</span><span class="sxs-lookup"><span data-stu-id="42a6d-114">You can choose whether to print the grid on a page-by-page basis.</span></span> <span data-ttu-id="42a6d-115">Das Format des Rasters kann auch definiert werden, auf Basis von Seite in der **Lineal &amp; Raster** im Dialogfeld (klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil neben **Anzeigen** ) Wenn die Seite aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="42a6d-115">The style of grid can also be defined on a page-by-page basis in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow) when a page is active.</span></span> 
  
<span data-ttu-id="42a6d-116">Wenn Sie einen Verweis auf die Zelle PrintGrid nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="42a6d-116">To get a reference to the PrintGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="42a6d-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="42a6d-117">Cell name:</span></span>  <br/> |<span data-ttu-id="42a6d-118">PrintGrid</span><span class="sxs-lookup"><span data-stu-id="42a6d-118">PrintGrid</span></span>  <br/> |
   
<span data-ttu-id="42a6d-119">Wenn Sie einen Verweis auf die Zelle PrintGrid aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="42a6d-119">To get a reference to the PrintGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="42a6d-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="42a6d-120">Section index:</span></span>  <br/> |<span data-ttu-id="42a6d-121">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="42a6d-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="42a6d-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="42a6d-122">Row index:</span></span>  <br/> |<span data-ttu-id="42a6d-123">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="42a6d-123">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="42a6d-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="42a6d-124">Cell index:</span></span>  <br/> |<span data-ttu-id="42a6d-125">**visPrintPropertiesPrintGrid**</span><span class="sxs-lookup"><span data-stu-id="42a6d-125">**visPrintPropertiesPrintGrid**</span></span> <br/> |
   

