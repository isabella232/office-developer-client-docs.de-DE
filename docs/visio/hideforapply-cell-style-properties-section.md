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
ms.openlocfilehash: 7b3830488770a66d7be35923e1807dbcdcd1f1c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423244"
---
# <a name="hideforapply-cell-style-properties-section"></a><span data-ttu-id="90a60-103">Zelle "HideForApply" (Abschnitt "Style Properties")</span><span class="sxs-lookup"><span data-stu-id="90a60-103">HideForApply Cell (Style Properties Section)</span></span>

<span data-ttu-id="90a60-104">Bestimmt, wo eine Formatvorlage auf der Microsoft Visio-Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="90a60-104">Determines where a style is shown in the Microsoft Visio user interface.</span></span>
  
|<span data-ttu-id="90a60-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="90a60-105">**Value**</span></span>|<span data-ttu-id="90a60-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="90a60-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="90a60-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="90a60-107">TRUE</span></span>  <br/> | <span data-ttu-id="90a60-108">Formatvorlage nur im **Zeichnungsexplorer** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="90a60-108">Show the style only in the **Drawing Explorer**.</span></span>  <br/> |
| <span data-ttu-id="90a60-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="90a60-109">FALSE</span></span>  <br/> | <span data-ttu-id="90a60-110">Formatvorlage im **Zeichnungsexplorer** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="90a60-110">Show the style in the **Drawing Explorer**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90a60-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90a60-111">Remarks</span></span>

<span data-ttu-id="90a60-112">Wenn Sie eine neue Formatvorlage auf der Grundlage einer ausgeblendeten Formatvorlage erstellen, erbt die neue Formatvorlage dieses Attribut nicht.</span><span class="sxs-lookup"><span data-stu-id="90a60-112">When you base a new style on a style that is hidden, the new style does not inherit this attribute.</span></span>
  
<span data-ttu-id="90a60-113">Wenn Sie einen Verweis auf die Zelle "HideForApply aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="90a60-113">To get a reference to the HideForApply cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="90a60-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="90a60-114">Cell name:</span></span>  <br/> | <span data-ttu-id="90a60-115">"HideForApply</span><span class="sxs-lookup"><span data-stu-id="90a60-115">HideForApply</span></span>  <br/> |
   
<span data-ttu-id="90a60-116">Wenn Sie einen Verweis auf die Zelle "HideForApply aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="90a60-116">To get a reference to the HideForApply cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="90a60-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="90a60-117">Section index:</span></span>  <br/> |<span data-ttu-id="90a60-118">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="90a60-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="90a60-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="90a60-119">Row index:</span></span>  <br/> |<span data-ttu-id="90a60-120">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="90a60-120">**visRowStyle**</span></span> <br/> |
| <span data-ttu-id="90a60-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="90a60-121">Cell index:</span></span>  <br/> |<span data-ttu-id="90a60-122">**visStyleHidden**</span><span class="sxs-lookup"><span data-stu-id="90a60-122">**visStyleHidden**</span></span> <br/> |
   

