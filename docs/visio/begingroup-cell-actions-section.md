---
title: Zelle "BeginGroup" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60022
localization_priority: Normal
ms.assetid: 1ae7f629-fb9f-1a11-1194-b381d6c9de5b
description: Gibt an, ob über dieser Aktion ein Trennzeichen in das Menü eingefügt wird.
ms.openlocfilehash: 749f611209d362811f5e4fb051780a4a642295c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796425"
---
# <a name="begingroup-cell-actions-section"></a><span data-ttu-id="85ecb-103">BeginGroup Cell (Actions Section)</span><span class="sxs-lookup"><span data-stu-id="85ecb-103">BeginGroup Cell (Actions Section)</span></span>

<span data-ttu-id="85ecb-104">Gibt an, ob über dieser Aktion ein Trennzeichen in das Menü eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="85ecb-104">Indicates whether a separator is inserted into the menu above this action.</span></span> 
  
|<span data-ttu-id="85ecb-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="85ecb-105">**Value**</span></span>|<span data-ttu-id="85ecb-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="85ecb-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85ecb-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="85ecb-107">TRUE</span></span>  <br/> |<span data-ttu-id="85ecb-108">Klicken Sie im Menü über der Aktion wird ein Trennzeichen eingefügt.</span><span class="sxs-lookup"><span data-stu-id="85ecb-108">A separator is inserted into the menu above this action.</span></span>  <br/> |
|<span data-ttu-id="85ecb-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="85ecb-109">FALSE</span></span>  <br/> |<span data-ttu-id="85ecb-110">Ein Trennzeichen ist nicht in das Menü über der Aktion (Standardeinstellung) eingefügt.</span><span class="sxs-lookup"><span data-stu-id="85ecb-110">A separator is not inserted into the menu above this action (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85ecb-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="85ecb-111">Remarks</span></span>

<span data-ttu-id="85ecb-112">Wenn Sie einen Verweis auf die Zelle BeginGroup nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="85ecb-112">To get a reference to the BeginGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="85ecb-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="85ecb-113">Cell name:</span></span>  <br/> |<span data-ttu-id="85ecb-114">Aktionen.</span><span class="sxs-lookup"><span data-stu-id="85ecb-114">Actions.</span></span> <span data-ttu-id="85ecb-115">*Name*. BeginGroup wobei Aktionen.</span><span class="sxs-lookup"><span data-stu-id="85ecb-115">*name*.BeginGroup where Actions.</span></span> <span data-ttu-id="85ecb-116">*Name* ist der Name der Zeile Actions</span><span class="sxs-lookup"><span data-stu-id="85ecb-116">*name* is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="85ecb-117">Wenn Sie einen Verweis auf die Zelle BeginGroup aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="85ecb-117">To get a reference to the BeginGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="85ecb-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="85ecb-118">Section index:</span></span>  <br/> |<span data-ttu-id="85ecb-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="85ecb-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="85ecb-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="85ecb-120">Row index:</span></span>  <br/> |<span data-ttu-id="85ecb-121">**VisRowAction** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="85ecb-121">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="85ecb-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="85ecb-122">Cell index:</span></span>  <br/> |<span data-ttu-id="85ecb-123">**visActionBeginGroup**</span><span class="sxs-lookup"><span data-stu-id="85ecb-123">**visActionBeginGroup**</span></span> <br/> |
   

