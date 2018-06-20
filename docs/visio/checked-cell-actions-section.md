---
title: Zelle "Checked" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm155
localization_priority: Normal
ms.assetid: 50937e29-eaa1-0cd0-53cc-dc17e7793e55
description: Gibt an, ob ein Element im Kontext- oder Aktionstagmenü aktiviert ist.
ms.openlocfilehash: 7c5bcdbfe5b7d8e796af49c8da6ef0fc233e3d62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796648"
---
# <a name="checked-cell-actions-section"></a><span data-ttu-id="2a9dd-103">Checked Cell (Actions Section)</span><span class="sxs-lookup"><span data-stu-id="2a9dd-103">Checked Cell (Actions Section)</span></span>

<span data-ttu-id="2a9dd-104">Gibt an, ob ein Element im Kontext- oder Aktionstagmenü aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-104">Indicates whether an item is checked on the shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2a9dd-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="2a9dd-106">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2a9dd-106">**Value**</span></span>|<span data-ttu-id="2a9dd-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2a9dd-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2a9dd-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="2a9dd-108">TRUE</span></span>  <br/> |<span data-ttu-id="2a9dd-109">Häkchen wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-109">Check mark is displayed.</span></span>  <br/> |
|<span data-ttu-id="2a9dd-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="2a9dd-110">FALSE</span></span>  <br/> |<span data-ttu-id="2a9dd-111">Häkchen wird nicht angezeigt (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="2a9dd-111">Check mark is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a9dd-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2a9dd-112">Remarks</span></span>

<span data-ttu-id="2a9dd-113">Zum Abrufen eines Verweises auf die Zelle Checked nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2a9dd-113">To get a reference to the Checked cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2a9dd-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2a9dd-114">Cell name:</span></span>  <br/> |<span data-ttu-id="2a9dd-115">Aktionen.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-115">Actions.</span></span> <span data-ttu-id="2a9dd-116">*Name* . Überprüft, wobei Aktionen.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-116">*name*  .Checked           where Actions.</span></span> <span data-ttu-id="2a9dd-117">*Name* ist der Name der Zeile Actions</span><span class="sxs-lookup"><span data-stu-id="2a9dd-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="2a9dd-118">Wenn Sie einen Verweis auf die Zelle Checked aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="2a9dd-118">To get a reference to the Checked cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2a9dd-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2a9dd-119">Section index:</span></span>  <br/> |<span data-ttu-id="2a9dd-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="2a9dd-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="2a9dd-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2a9dd-121">Row index:</span></span>  <br/> |<span data-ttu-id="2a9dd-122">**VisRowAction** +  *i* wobei *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="2a9dd-122">**visRowAction** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="2a9dd-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2a9dd-123">Cell index:</span></span>  <br/> |<span data-ttu-id="2a9dd-124">**visActionChecked**</span><span class="sxs-lookup"><span data-stu-id="2a9dd-124">**visActionChecked**</span></span> <br/> |
   

