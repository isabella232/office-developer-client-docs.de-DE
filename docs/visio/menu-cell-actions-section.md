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
ms.openlocfilehash: adb6915c34946472ada8c4ab4d02fa88bab6651a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436328"
---
# <a name="menu-cell-actions-section"></a><span data-ttu-id="262a8-103">Zelle "Menu" (Abschnitt "Actions")</span><span class="sxs-lookup"><span data-stu-id="262a8-103">Menu Cell (Actions Section)</span></span>

<span data-ttu-id="262a8-104">Definiert den Namen eines Menüelements, das in einem Kontext- oder Aktionstagmenü für ein Shape oder Zeichenblatt angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="262a8-104">Defines the name of a menu item that appears on a shortcut or action tag menu for a shape or page.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="262a8-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="262a8-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="262a8-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="262a8-106">Remarks</span></span>

<span data-ttu-id="262a8-p101">Wenn Sie über diesem Element ein Trennzeichen in das Menü einfügen möchten, verwenden Sie die Zelle BeginGroup. Um den Befehl unten im Menü anzuzeigen, geben Sie vor dem Namen ein Prozentzeichen (%) ein.</span><span class="sxs-lookup"><span data-stu-id="262a8-p101">To insert a separator into the menu above this item, use the BeginGroup cell. To display the command at the bottom of the menu, prefix the name with a percent character (%) .</span></span>
  
<span data-ttu-id="262a8-109">Wenn Sie einen Verweis auf die Zelle Menü aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="262a8-109">To get a reference to the Menu cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="262a8-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="262a8-110">Cell name:</span></span>  <br/> |<span data-ttu-id="262a8-111">Aktionen.</span><span class="sxs-lookup"><span data-stu-id="262a8-111">Actions.</span></span> <span data-ttu-id="262a8-112">*Name* . Menuwobei-Aktionen.</span><span class="sxs-lookup"><span data-stu-id="262a8-112">*name*  .Menuwhere Actions.</span></span>  <span data-ttu-id="262a8-113">*Name* ist der Name der Zeile Actions.</span><span class="sxs-lookup"><span data-stu-id="262a8-113">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="262a8-114">Wenn Sie einen Verweis auf die Zelle Menu aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="262a8-114">To get a reference to the Menu cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="262a8-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="262a8-115">Section index:</span></span>  <br/> |<span data-ttu-id="262a8-116">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="262a8-116">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="262a8-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="262a8-117">Row index:</span></span>  <br/> |<span data-ttu-id="262a8-118">**visRowAction** +  *i* , wobei i = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="262a8-118">**visRowAction** +  *i*  where i = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="262a8-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="262a8-119">Cell index:</span></span>  <br/> |<span data-ttu-id="262a8-120">**visActionMenu**</span><span class="sxs-lookup"><span data-stu-id="262a8-120">**visActionMenu**</span></span> <br/> |
   

