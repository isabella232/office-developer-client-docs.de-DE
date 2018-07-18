---
title: Zelle "Menu" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm690
localization_priority: Normal
ms.assetid: 29af746c-b081-24cf-a30d-a56353ee849e
description: Definiert den Namen eines Menüelements, das in einem Kontext- oder Aktionstagmenü für ein Shape oder Zeichenblatt angezeigt wird.
ms.openlocfilehash: 195af94c4c36bb3c29a4fadab3c68f8334742952
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797549"
---
# <a name="menu-cell-actions-section"></a><span data-ttu-id="db84a-103">Menu Cell (Actions Section)</span><span class="sxs-lookup"><span data-stu-id="db84a-103">Menu Cell (Actions Section)</span></span>

<span data-ttu-id="db84a-104">Definiert den Namen eines Menüelements, das in einem Kontext- oder Aktionstagmenü für ein Shape oder Zeichenblatt angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="db84a-104">Defines the name of a menu item that appears on a shortcut or action tag menu for a shape or page.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="db84a-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="db84a-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="db84a-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db84a-106">Remarks</span></span>

<span data-ttu-id="db84a-p101">Wenn Sie über diesem Element ein Trennzeichen in das Menü einfügen möchten, verwenden Sie die Zelle BeginGroup. Um den Befehl unten im Menü anzuzeigen, geben Sie vor dem Namen ein Prozentzeichen (%) ein.</span><span class="sxs-lookup"><span data-stu-id="db84a-p101">To insert a separator into the menu above this item, use the BeginGroup cell. To display the command at the bottom of the menu, prefix the name with a percent character (%) .</span></span>
  
<span data-ttu-id="db84a-109">Zum Abrufen eines Verweises auf die Zelle Menu nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="db84a-109">To get a reference to the Menu cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db84a-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="db84a-110">Cell name:</span></span>  <br/> |<span data-ttu-id="db84a-111">Aktionen.</span><span class="sxs-lookup"><span data-stu-id="db84a-111">Actions.</span></span> <span data-ttu-id="db84a-112">*Name* . Menuwhere Aktionen.</span><span class="sxs-lookup"><span data-stu-id="db84a-112">*name*  .Menuwhere Actions.</span></span>  <span data-ttu-id="db84a-113">*Name* ist der Name der Zeile Actions</span><span class="sxs-lookup"><span data-stu-id="db84a-113">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="db84a-114">Wenn Sie einen Verweis auf die Zelle Menu aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="db84a-114">To get a reference to the Menu cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db84a-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="db84a-115">Section index:</span></span>  <br/> |<span data-ttu-id="db84a-116">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="db84a-116">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="db84a-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="db84a-117">Row index:</span></span>  <br/> |<span data-ttu-id="db84a-118">**VisRowAction** +  *i* wobei i = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="db84a-118">**visRowAction** +  *i*  where i = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="db84a-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="db84a-119">Cell index:</span></span>  <br/> |<span data-ttu-id="db84a-120">**visActionMenu**</span><span class="sxs-lookup"><span data-stu-id="db84a-120">**visActionMenu**</span></span> <br/> |
   

