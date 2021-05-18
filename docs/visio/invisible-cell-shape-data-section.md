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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405317"
---
# <a name="invisible-cell-shape-data-section"></a><span data-ttu-id="6ca20-103">Zelle "Invisible" (Abschnitt "Shape Data")</span><span class="sxs-lookup"><span data-stu-id="6ca20-103">Invisible Cell (Shape Data Section)</span></span>

<span data-ttu-id="6ca20-104">Gibt an, ob das Shape-Datenelement im Fenster **Shape-Daten** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6ca20-104">Specifies whether the shape data item is visible in the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="6ca20-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6ca20-105">**Value**</span></span>|<span data-ttu-id="6ca20-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6ca20-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6ca20-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="6ca20-107">TRUE</span></span>  <br/> | <span data-ttu-id="6ca20-108">Shape-Datenelement wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6ca20-108">Shape data item is not visible.</span></span>  <br/> |
| <span data-ttu-id="6ca20-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="6ca20-109">FALSE</span></span>  <br/> | <span data-ttu-id="6ca20-110">Shape-Datenelement wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6ca20-110">Shape data item is visible.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ca20-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6ca20-111">Remarks</span></span>

<span data-ttu-id="6ca20-112">Der Wert in dieser Zelle entspricht dem Kontrollkästchen **Ausgeblendet** im Dialogfeld **Shape-Daten definieren** (klicken Sie mit der rechten Maustaste auf das Shape, zeigen Sie auf **Daten**, und klicken Sie dann auf **Shape-Daten definieren**).</span><span class="sxs-lookup"><span data-stu-id="6ca20-112">The value in this cell corresponds to the **Hidden** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="6ca20-113">Um einen Verweis auf die Zelle Invisible anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="6ca20-113">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6ca20-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6ca20-114">Cell name:</span></span>  <br/> | <span data-ttu-id="6ca20-115">Prop.  *Name*  . Unsichtbar, wo Prop.  *Name*  ist der Zeilenname</span><span class="sxs-lookup"><span data-stu-id="6ca20-115">Prop.  *name*  .Invisible where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="6ca20-116">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Invisible nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="6ca20-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6ca20-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6ca20-117">Section index:</span></span>  <br/> |<span data-ttu-id="6ca20-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="6ca20-118">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="6ca20-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6ca20-119">Row index:</span></span>  <br/> |<span data-ttu-id="6ca20-120">**visRowProp**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6ca20-120">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6ca20-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6ca20-121">Cell index:</span></span>  <br/> |<span data-ttu-id="6ca20-122">**visCustPropsInvis**</span><span class="sxs-lookup"><span data-stu-id="6ca20-122">**visCustPropsInvis**</span></span> <br/> |
   

