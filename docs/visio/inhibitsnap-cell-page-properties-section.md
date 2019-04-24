---
title: Zelle "InhibitSnap" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251620
localization_priority: Normal
ms.assetid: ab9fcebc-1550-3b9e-e3b4-e8b92424390b
description: Legt fest, ob die Shapes auf einem Vordergrundblatt an anderen Objekten auf dem Zeichenblatt und an Shapes auf dem Hintergrundblatt einrasten.
ms.openlocfilehash: 665130e9f9f938349028ffa1d1c06224e746de5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335322"
---
# <a name="inhibitsnap-cell-page-properties-section"></a><span data-ttu-id="9381a-103">Zelle "InhibitSnap" (Abschnitt "Page Properties")</span><span class="sxs-lookup"><span data-stu-id="9381a-103">InhibitSnap Cell (Page Properties Section)</span></span>

<span data-ttu-id="9381a-104">Legt fest, ob die Shapes auf einem Vordergrundblatt an anderen Objekten auf dem Zeichenblatt und an Shapes auf dem Hintergrundblatt einrasten.</span><span class="sxs-lookup"><span data-stu-id="9381a-104">Determines whether the shapes on a foreground page snap to other objects on the page and shapes on the background page.</span></span>
  
|<span data-ttu-id="9381a-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9381a-105">**Value**</span></span>|<span data-ttu-id="9381a-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9381a-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="9381a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="9381a-107">TRUE</span></span>  <br/> | <span data-ttu-id="9381a-108">Einrasten auf dem Zeichenblatt mit Ausnahme des Einrastens am Lineal und Gitter verhindern.</span><span class="sxs-lookup"><span data-stu-id="9381a-108">Inhibit all snapping on the page, except for snapping to the ruler and grid.</span></span>  <br/> |
| <span data-ttu-id="9381a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9381a-109">FALSE</span></span>  <br/> | <span data-ttu-id="9381a-110">Einrasten aktivieren.</span><span class="sxs-lookup"><span data-stu-id="9381a-110">Enable snapping.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9381a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9381a-111">Remarks</span></span>

<span data-ttu-id="9381a-112">Wenn Sie einen Verweis auf die Zelle "InhibitSnap aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9381a-112">To get a reference to the InhibitSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9381a-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9381a-113">Cell name:</span></span>  <br/> | <span data-ttu-id="9381a-114">"InhibitSnap</span><span class="sxs-lookup"><span data-stu-id="9381a-114">InhibitSnap</span></span>  <br/> |
   
<span data-ttu-id="9381a-115">Wenn Sie einen Verweis auf die Zelle "InhibitSnap aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9381a-115">To get a reference to the InhibitSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9381a-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9381a-116">Section index:</span></span>  <br/> |<span data-ttu-id="9381a-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9381a-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9381a-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9381a-118">Row index:</span></span>  <br/> |<span data-ttu-id="9381a-119">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="9381a-119">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="9381a-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9381a-120">Cell index:</span></span>  <br/> |<span data-ttu-id="9381a-121">**visPageInhibitSnap**</span><span class="sxs-lookup"><span data-stu-id="9381a-121">**visPageInhibitSnap**</span></span> <br/> |
   

