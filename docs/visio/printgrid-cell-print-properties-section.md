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
ms.openlocfilehash: 9b98999cd02fa6a47ec8564bbd7337ecf8637306
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315190"
---
# <a name="printgrid-cell-print-properties-section"></a><span data-ttu-id="41436-103">Zelle "PrintGrid" (Abschnitt "Print Properties")</span><span class="sxs-lookup"><span data-stu-id="41436-103">PrintGrid Cell (Print Properties Section)</span></span>

<span data-ttu-id="41436-104">Gibt an, ob beim Drucken einer Dokumentseite das Gitternetz gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="41436-104">Specifies whether to print the grid when printing a document page.</span></span>
  
|<span data-ttu-id="41436-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="41436-105">**Value**</span></span>|<span data-ttu-id="41436-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="41436-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="41436-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="41436-107">TRUE</span></span>  <br/> |<span data-ttu-id="41436-108">Beim Drucken der Seite wird das Gitternetz gedruckt.</span><span class="sxs-lookup"><span data-stu-id="41436-108">Show the grid when printing this page.</span></span>  <br/> |
|<span data-ttu-id="41436-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="41436-109">FALSE</span></span>  <br/> |<span data-ttu-id="41436-110">Das Gitternetz wird beim Drucken der Seite nicht gedruckt (Standard).</span><span class="sxs-lookup"><span data-stu-id="41436-110">Do not show the grid when printing this page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41436-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41436-111">Remarks</span></span>

<span data-ttu-id="41436-p101">Dieser Wert entspricht der Einstellung für das Kontrollkästchen **Gitterlinien** auf der Registerkarte **Druckeinrichtung** im Dialogfeld **Seite einrichten** (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**). Mit Ausnahme der Farbe (die Druckversion ist grau) ist das gedruckte Gitternetz identisch mit dem im Microsoft Visio-Zeichenfenster.</span><span class="sxs-lookup"><span data-stu-id="41436-p101">This value corresponds to the **Gridlines** check box on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). Other than color (the printed version is gray), the printed grid is identical to the grid you see in the Microsoft Visio drawing window.</span></span> 
  
<span data-ttu-id="41436-114">Sie können für einzelne Seiten festlegen, ob das Gitternetz gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="41436-114">You can choose whether to print the grid on a page-by-page basis.</span></span> <span data-ttu-id="41436-115">Die Art des Rasters kann auch auf Seitenbasis im Dialogfeld \*\*\*\* \*\* &amp; Lineal-Raster\*\* definiert werden (Klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil nach unten), wenn eine Seite aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="41436-115">The style of grid can also be defined on a page-by-page basis in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow) when a page is active.</span></span> 
  
<span data-ttu-id="41436-116">Wenn Sie einen Verweis auf die Zelle PrintGrid aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="41436-116">To get a reference to the PrintGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41436-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="41436-117">Cell name:</span></span>  <br/> |<span data-ttu-id="41436-118">PrintGrid</span><span class="sxs-lookup"><span data-stu-id="41436-118">PrintGrid</span></span>  <br/> |
   
<span data-ttu-id="41436-119">Wenn Sie einen Verweis auf die Zelle PrintGrid aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="41436-119">To get a reference to the PrintGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41436-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="41436-120">Section index:</span></span>  <br/> |<span data-ttu-id="41436-121">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="41436-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="41436-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="41436-122">Row index:</span></span>  <br/> |<span data-ttu-id="41436-123">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="41436-123">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="41436-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="41436-124">Cell index:</span></span>  <br/> |<span data-ttu-id="41436-125">**visPrintPropertiesPrintGrid**</span><span class="sxs-lookup"><span data-stu-id="41436-125">**visPrintPropertiesPrintGrid**</span></span> <br/> |
   

