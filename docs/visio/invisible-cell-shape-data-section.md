---
title: Zelle "Invisible" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251341
localization_priority: Normal
ms.assetid: 5f368c2e-2a40-38ee-3568-ed5c57633345
description: Gibt an, ob das Shape-Datenelement im Fenster Shape-Daten angezeigt wird.
ms.openlocfilehash: 2cd3fcad5db7b1752c55055354f1ec842bff4899
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797215"
---
# <a name="invisible-cell-shape-data-section"></a><span data-ttu-id="52319-103">Invisible Cell (Shape Data Section)</span><span class="sxs-lookup"><span data-stu-id="52319-103">Invisible Cell (Shape Data Section)</span></span>

<span data-ttu-id="52319-104">Gibt an, ob das Shape-Datenelement im Fenster **Shape-Daten** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="52319-104">Specifies whether the shape data item is visible in the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="52319-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="52319-105">**Value**</span></span>|<span data-ttu-id="52319-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="52319-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="52319-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="52319-107">TRUE</span></span>  <br/> | <span data-ttu-id="52319-108">Shape-Datenelement wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="52319-108">Shape data item is not visible.</span></span>  <br/> |
| <span data-ttu-id="52319-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="52319-109">FALSE</span></span>  <br/> | <span data-ttu-id="52319-110">Shape-Datenelement wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="52319-110">Shape data item is visible.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52319-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52319-111">Remarks</span></span>

<span data-ttu-id="52319-112">Der Wert in dieser Zelle entspricht dem Kontrollkästchen **ausgeblendet** im Dialogfeld **Shape-Daten definieren** (mit der rechten Maustaste in des Shapes, zeigen Sie auf **Daten**, und klicken Sie dann auf **Shape-Daten definieren**).</span><span class="sxs-lookup"><span data-stu-id="52319-112">The value in this cell corresponds to the **Hidden** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="52319-113">Wenn Sie einen Verweis auf die Zelle Invisible nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="52319-113">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="52319-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="52319-114">Cell name:</span></span>  <br/> | <span data-ttu-id="52319-115">Eigenschaft.  *Name* . Nicht sichtbare Where Prop.  *Name* ist der Zeilenname</span><span class="sxs-lookup"><span data-stu-id="52319-115">Prop.  *name*  .Invisible where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="52319-116">Wenn Sie einen Verweis auf die Zelle Invisible aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="52319-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="52319-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="52319-117">Section index:</span></span>  <br/> |<span data-ttu-id="52319-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="52319-118">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="52319-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="52319-119">Row index:</span></span>  <br/> |<span data-ttu-id="52319-120">**VisRowProp** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="52319-120">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="52319-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="52319-121">Cell index:</span></span>  <br/> |<span data-ttu-id="52319-122">**visCustPropsInvis**</span><span class="sxs-lookup"><span data-stu-id="52319-122">**visCustPropsInvis**</span></span> <br/> |
   

