---
title: Zelle "HideForApply" (Abschnitt "Style Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251698
localization_priority: Normal
ms.assetid: 62d87db9-b8ca-60b6-bf27-5168c718ec96
description: Bestimmt, wo eine Formatvorlage auf der Microsoft Visio-Benutzeroberfläche angezeigt wird.
ms.openlocfilehash: 5b0221c54c17a3b9957cce5e890842def0ba7525
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797164"
---
# <a name="hideforapply-cell-style-properties-section"></a><span data-ttu-id="83d01-103">HideForApply Cell (Style Properties Section)</span><span class="sxs-lookup"><span data-stu-id="83d01-103">HideForApply Cell (Style Properties Section)</span></span>

<span data-ttu-id="83d01-104">Bestimmt, wo eine Formatvorlage auf der Microsoft Visio-Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="83d01-104">Determines where a style is shown in the Microsoft Visio user interface.</span></span>
  
|<span data-ttu-id="83d01-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="83d01-105">**Value**</span></span>|<span data-ttu-id="83d01-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="83d01-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="83d01-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="83d01-107">TRUE</span></span>  <br/> | <span data-ttu-id="83d01-108">
          Formatvorlage nur im **Zeichnungsexplorer** anzeigen.
</span><span class="sxs-lookup"><span data-stu-id="83d01-108">Show the style only in the **Drawing Explorer**.</span></span>  <br/> |
| <span data-ttu-id="83d01-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="83d01-109">FALSE</span></span>  <br/> | <span data-ttu-id="83d01-110">
          Formatvorlage im **Zeichnungsexplorer** anzeigen.
</span><span class="sxs-lookup"><span data-stu-id="83d01-110">Show the style in the **Drawing Explorer**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83d01-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="83d01-111">Remarks</span></span>

<span data-ttu-id="83d01-112">Wenn Sie eine neue Formatvorlage auf der Grundlage einer ausgeblendeten Formatvorlage erstellen, erbt die neue Formatvorlage dieses Attribut nicht.</span><span class="sxs-lookup"><span data-stu-id="83d01-112">When you base a new style on a style that is hidden, the new style does not inherit this attribute.</span></span>
  
<span data-ttu-id="83d01-113">Wenn Sie einen Verweis auf die Zelle HideForApply aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="83d01-113">To get a reference to the HideForApply cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="83d01-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="83d01-114">Cell name:</span></span>  <br/> | <span data-ttu-id="83d01-115">HideForApply</span><span class="sxs-lookup"><span data-stu-id="83d01-115">HideForApply</span></span>  <br/> |
   
<span data-ttu-id="83d01-116">Wenn Sie einen Verweis auf die Zelle HideForApply aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="83d01-116">To get a reference to the HideForApply cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="83d01-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="83d01-117">Section index:</span></span>  <br/> |<span data-ttu-id="83d01-118">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="83d01-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="83d01-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="83d01-119">Row index:</span></span>  <br/> |<span data-ttu-id="83d01-120">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="83d01-120">**visRowStyle**</span></span> <br/> |
| <span data-ttu-id="83d01-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="83d01-121">Cell index:</span></span>  <br/> |<span data-ttu-id="83d01-122">**visStyleHidden**</span><span class="sxs-lookup"><span data-stu-id="83d01-122">**visStyleHidden**</span></span> <br/> |
   

