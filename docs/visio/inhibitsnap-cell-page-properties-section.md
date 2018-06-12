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
ms.openlocfilehash: b95dafda9ebef36db34f60585ab3ed2164ade415
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797208"
---
# <a name="inhibitsnap-cell-page-properties-section"></a><span data-ttu-id="3379b-103">InhibitSnap Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="3379b-103">InhibitSnap Cell (Page Properties Section)</span></span>

<span data-ttu-id="3379b-104">Legt fest, ob die Shapes auf einem Vordergrundblatt an anderen Objekten auf dem Zeichenblatt und an Shapes auf dem Hintergrundblatt einrasten.</span><span class="sxs-lookup"><span data-stu-id="3379b-104">Determines whether the shapes on a foreground page snap to other objects on the page and shapes on the background page.</span></span>
  
|<span data-ttu-id="3379b-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="3379b-105">**Value**</span></span>|<span data-ttu-id="3379b-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3379b-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3379b-107">WAHR</span><span class="sxs-lookup"><span data-stu-id="3379b-107">TRUE</span></span>  <br/> | <span data-ttu-id="3379b-108">Einrasten auf dem Zeichenblatt mit Ausnahme des Einrastens am Lineal und Gitter verhindern.</span><span class="sxs-lookup"><span data-stu-id="3379b-108">Inhibit all snapping on the page, except for snapping to the ruler and grid.</span></span>  <br/> |
| <span data-ttu-id="3379b-109">FALSCH</span><span class="sxs-lookup"><span data-stu-id="3379b-109">FALSE</span></span>  <br/> | <span data-ttu-id="3379b-110">Einrasten aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3379b-110">Enable snapping.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3379b-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3379b-111">Remarks</span></span>

<span data-ttu-id="3379b-112">Wenn Sie einen Verweis auf die Zelle InhibitSnap nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3379b-112">To get a reference to the InhibitSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3379b-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="3379b-113">Cell name:</span></span>  <br/> | <span data-ttu-id="3379b-114">InhibitSnap</span><span class="sxs-lookup"><span data-stu-id="3379b-114">InhibitSnap</span></span>  <br/> |
   
<span data-ttu-id="3379b-115">Wenn Sie einen Verweis auf die Zelle InhibitSnap aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="3379b-115">To get a reference to the InhibitSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3379b-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="3379b-116">Section index:</span></span>  <br/> |<span data-ttu-id="3379b-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3379b-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3379b-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="3379b-118">Row index:</span></span>  <br/> |<span data-ttu-id="3379b-119">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="3379b-119">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="3379b-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="3379b-120">Cell index:</span></span>  <br/> |<span data-ttu-id="3379b-121">**visPageInhibitSnap**</span><span class="sxs-lookup"><span data-stu-id="3379b-121">**visPageInhibitSnap**</span></span> <br/> |
   

