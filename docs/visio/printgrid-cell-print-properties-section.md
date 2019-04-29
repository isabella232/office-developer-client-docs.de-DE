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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433206"
---
# <a name="printgrid-cell-print-properties-section"></a><span data-ttu-id="9ace6-103">Zelle "PrintGrid" (Abschnitt "Print Properties")</span><span class="sxs-lookup"><span data-stu-id="9ace6-103">PrintGrid Cell (Print Properties Section)</span></span>

<span data-ttu-id="9ace6-104">Gibt an, ob beim Drucken einer Dokumentseite das Gitternetz gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ace6-104">Specifies whether to print the grid when printing a document page.</span></span>
  
|<span data-ttu-id="9ace6-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9ace6-105">**Value**</span></span>|<span data-ttu-id="9ace6-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9ace6-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9ace6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="9ace6-107">TRUE</span></span>  <br/> |<span data-ttu-id="9ace6-108">Beim Drucken der Seite wird das Gitternetz gedruckt.</span><span class="sxs-lookup"><span data-stu-id="9ace6-108">Show the grid when printing this page.</span></span>  <br/> |
|<span data-ttu-id="9ace6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9ace6-109">FALSE</span></span>  <br/> |<span data-ttu-id="9ace6-110">Das Gitternetz wird beim Drucken der Seite nicht gedruckt (Standard).</span><span class="sxs-lookup"><span data-stu-id="9ace6-110">Do not show the grid when printing this page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ace6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ace6-111">Remarks</span></span>

<span data-ttu-id="9ace6-p101">Dieser Wert entspricht der Einstellung für das Kontrollkästchen **Gitterlinien** auf der Registerkarte **Druckeinrichtung** im Dialogfeld **Seite einrichten** (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**). Mit Ausnahme der Farbe (die Druckversion ist grau) ist das gedruckte Gitternetz identisch mit dem im Microsoft Visio-Zeichenfenster.</span><span class="sxs-lookup"><span data-stu-id="9ace6-p101">This value corresponds to the **Gridlines** check box on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). Other than color (the printed version is gray), the printed grid is identical to the grid you see in the Microsoft Visio drawing window.</span></span> 
  
<span data-ttu-id="9ace6-114">Sie können für einzelne Seiten festlegen, ob das Gitternetz gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ace6-114">You can choose whether to print the grid on a page-by-page basis.</span></span> <span data-ttu-id="9ace6-115">Die Art des Rasters kann auch auf Seitenbasis im Dialogfeld \*\*\*\* \*\* &amp; Lineal-Raster\*\* definiert werden (Klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil nach unten), wenn eine Seite aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="9ace6-115">The style of grid can also be defined on a page-by-page basis in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow) when a page is active.</span></span> 
  
<span data-ttu-id="9ace6-116">Wenn Sie einen Verweis auf die Zelle PrintGrid aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9ace6-116">To get a reference to the PrintGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ace6-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9ace6-117">Cell name:</span></span>  <br/> |<span data-ttu-id="9ace6-118">PrintGrid</span><span class="sxs-lookup"><span data-stu-id="9ace6-118">PrintGrid</span></span>  <br/> |
   
<span data-ttu-id="9ace6-119">Wenn Sie einen Verweis auf die Zelle PrintGrid aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9ace6-119">To get a reference to the PrintGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ace6-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9ace6-120">Section index:</span></span>  <br/> |<span data-ttu-id="9ace6-121">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9ace6-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9ace6-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9ace6-122">Row index:</span></span>  <br/> |<span data-ttu-id="9ace6-123">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="9ace6-123">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="9ace6-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9ace6-124">Cell index:</span></span>  <br/> |<span data-ttu-id="9ace6-125">**visPrintPropertiesPrintGrid**</span><span class="sxs-lookup"><span data-stu-id="9ace6-125">**visPrintPropertiesPrintGrid**</span></span> <br/> |
   

