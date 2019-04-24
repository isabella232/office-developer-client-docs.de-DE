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
ms.openlocfilehash: 8671fcc249b7ca81c011f697721093e7842c1558
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357267"
---
# <a name="invisible-cell-shape-data-section"></a><span data-ttu-id="e79ee-103">Zelle "Invisible" (Abschnitt "Shape Data")</span><span class="sxs-lookup"><span data-stu-id="e79ee-103">Invisible Cell (Shape Data Section)</span></span>

<span data-ttu-id="e79ee-104">Gibt an, ob das Shape-Datenelement im Fenster **Shape-Daten** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e79ee-104">Specifies whether the shape data item is visible in the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="e79ee-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e79ee-105">**Value**</span></span>|<span data-ttu-id="e79ee-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e79ee-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e79ee-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e79ee-107">TRUE</span></span>  <br/> | <span data-ttu-id="e79ee-108">Shape-Datenelement wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e79ee-108">Shape data item is not visible.</span></span>  <br/> |
| <span data-ttu-id="e79ee-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e79ee-109">FALSE</span></span>  <br/> | <span data-ttu-id="e79ee-110">Shape-Datenelement wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e79ee-110">Shape data item is visible.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e79ee-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e79ee-111">Remarks</span></span>

<span data-ttu-id="e79ee-112">Der Wert in dieser Zelle entspricht dem Kontrollkästchen **Ausgeblendet** im Dialogfeld **Shape-Daten definieren** (klicken Sie mit der rechten Maustaste auf das Shape, zeigen Sie auf **Daten**, und klicken Sie dann auf **Shape-Daten definieren**).</span><span class="sxs-lookup"><span data-stu-id="e79ee-112">The value in this cell corresponds to the **Hidden** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="e79ee-113">Wenn Sie einen Verweis auf die Zelle inVisible aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e79ee-113">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e79ee-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e79ee-114">Cell name:</span></span>  <br/> | <span data-ttu-id="e79ee-115">Prop.  *Name* . Unsichtbar, wobei Prop.  *Name* ist der Name der Zeile</span><span class="sxs-lookup"><span data-stu-id="e79ee-115">Prop.  *name*  .Invisible where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="e79ee-116">Wenn Sie einen Verweis auf die unsichtbare Zelle aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="e79ee-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e79ee-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e79ee-117">Section index:</span></span>  <br/> |<span data-ttu-id="e79ee-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="e79ee-118">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="e79ee-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e79ee-119">Row index:</span></span>  <br/> |<span data-ttu-id="e79ee-120">**visRowProp** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e79ee-120">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e79ee-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e79ee-121">Cell index:</span></span>  <br/> |<span data-ttu-id="e79ee-122">**visCustPropsInvis**</span><span class="sxs-lookup"><span data-stu-id="e79ee-122">**visCustPropsInvis**</span></span> <br/> |
   

