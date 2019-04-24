---
title: Zelle "OnPage" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033793
localization_priority: Normal
ms.assetid: 4015506a-e24a-0276-c854-7791a7019067
description: Gibt an, ob die Zeichnung auf einer bestimmten Anzahl von Seiten gedruckt wird.
ms.openlocfilehash: 61d45a5bffdbb1afd5db9c608f80bc4f797f5191
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360984"
---
# <a name="onpage-cell-print-properties-section"></a><span data-ttu-id="b03e6-103">Zelle "OnPage" (Abschnitt "Print Properties")</span><span class="sxs-lookup"><span data-stu-id="b03e6-103">OnPage Cell (Print Properties Section)</span></span>

<span data-ttu-id="b03e6-104">Gibt an, ob die Zeichnung auf einer bestimmten Anzahl von Seiten gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="b03e6-104">Indicates whether the drawing is printed on a specific number of printer pages.</span></span> 
  
|<span data-ttu-id="b03e6-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b03e6-105">**Value**</span></span>|<span data-ttu-id="b03e6-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b03e6-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b03e6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b03e6-107">TRUE</span></span>  <br/> |<span data-ttu-id="b03e6-108">Das Zeichenblatt wird an eine bestimmte Anzahl von Drucker Seiten angepasst.</span><span class="sxs-lookup"><span data-stu-id="b03e6-108">Fit the drawing page to a defined number of printer pages.</span></span>  <br/> |
|<span data-ttu-id="b03e6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b03e6-109">FALSE</span></span>  <br/> |<span data-ttu-id="b03e6-110">Das Zeichenblatt wird nicht auf einer definierten Anzahl von Druckseiten ausgegeben (Standardwert).</span><span class="sxs-lookup"><span data-stu-id="b03e6-110">Do not fit the drawing page to a defined number of printer pages (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b03e6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b03e6-111">Remarks</span></span>

<span data-ttu-id="b03e6-p101">Wenn die Zelle OnPage auf WAHR festgelegt ist, bestimmt Microsoft Visio anhand der Zellen PagesX und PagesY die Anzahl der Druckseiten, auf denen die Zeichnung ausgegeben werden soll. Die Werte in den Zellen ScaleX und ScaleY werden ignoriert. Diese Einstellung ist eine AutoSkalieren-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="b03e6-p101">If the OnPage cell is set to TRUE, Microsoft Visio uses the PagesX and PagesY cells to determine the number of printer pages on which to fit the drawing. Values in the ScaleX and ScaleY cells are ignored. This can be considered an "autoscale" setting.</span></span>
  
<span data-ttu-id="b03e6-115">Dieser Wert entspricht der Option **an anpassen** auf der Register **Karte Druckeinrichtung** im Dialogfeld **Seite einrichten** (Klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil für die **Seite einrichten** ).</span><span class="sxs-lookup"><span data-stu-id="b03e6-115">This value corresponds to the **Fit to** option on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) .</span></span> 
  
<span data-ttu-id="b03e6-116">Wenn Sie einen Verweis auf die Zelle onPage aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b03e6-116">To get a reference to the OnPage cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b03e6-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b03e6-117">Cell name:</span></span>  <br/> |<span data-ttu-id="b03e6-118">OnPage</span><span class="sxs-lookup"><span data-stu-id="b03e6-118">OnPage</span></span>  <br/> |
   
<span data-ttu-id="b03e6-119">Wenn Sie einen Verweis auf die Zelle onPage aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="b03e6-119">To get a reference to the OnPage cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b03e6-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b03e6-120">Section index:</span></span>  <br/> |<span data-ttu-id="b03e6-121">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b03e6-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b03e6-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b03e6-122">Row index:</span></span>  <br/> |<span data-ttu-id="b03e6-123">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="b03e6-123">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="b03e6-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b03e6-124">Cell index:</span></span>  <br/> |<span data-ttu-id="b03e6-125">**visPrintPropertiesOnPage**</span><span class="sxs-lookup"><span data-stu-id="b03e6-125">**visPrintPropertiesOnPage**</span></span> <br/> |
   

