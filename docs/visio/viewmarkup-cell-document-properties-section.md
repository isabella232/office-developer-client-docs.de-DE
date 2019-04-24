---
title: Zelle "ViewMarkup" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030802
localization_priority: Normal
ms.assetid: 6c956266-8266-3312-5a68-cc9d8bdb8cd9
description: Bestimmt, ob im Zeichnungsfenster Markup angezeigt wird.
ms.openlocfilehash: eeccdd0d14bf28630937b0e480822abb6fb19da5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355825"
---
# <a name="viewmarkup-cell-document-properties-section"></a><span data-ttu-id="a1b31-103">Zelle "ViewMarkup" (Abschnitt "Document Properties")</span><span class="sxs-lookup"><span data-stu-id="a1b31-103">ViewMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="a1b31-104">Bestimmt, ob im Zeichnungsfenster Markup angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a1b31-104">Determines whether markup appears in the drawing window.</span></span> 
  
|<span data-ttu-id="a1b31-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a1b31-105">**Value**</span></span>|<span data-ttu-id="a1b31-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a1b31-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a1b31-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a1b31-107">TRUE</span></span>  <br/> |<span data-ttu-id="a1b31-108">Markup wird in der Zeichnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a1b31-108">Markup is displayed on the drawing.</span></span>  <br/> |
|<span data-ttu-id="a1b31-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a1b31-109">FALSE</span></span>  <br/> |<span data-ttu-id="a1b31-110">Markup wird nicht angezeigt (Standardwert).</span><span class="sxs-lookup"><span data-stu-id="a1b31-110">Markup is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1b31-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1b31-111">Remarks</span></span>

 <span data-ttu-id="a1b31-112">Wenn die Markupverfolgung aktiviert ist (die addMarkup-Zelle ist TRUE), wird die Zelle "ViewMarkup automatisch auf TRUE festgelegt und bleibt auch dann TRUE, wenn die Markupverfolgung deaktiviert ist (addMarkup cell is FALSE).</span><span class="sxs-lookup"><span data-stu-id="a1b31-112">When markup tracking is turned on (AddMarkup cell is TRUE), the ViewMarkup cell is automatically set to TRUE and remains TRUE even after markup tracking has been turned off (AddMarkup cell is FALSE).</span></span> <span data-ttu-id="a1b31-113">Der Wert in der Zelle ViewMarkup wird ignoriert, wenn die Zelle AddMarkup WAHR ist.</span><span class="sxs-lookup"><span data-stu-id="a1b31-113">The value in the ViewMarkup cell is ignored when the AddMarkup cell is TRUE.</span></span> 
  
<span data-ttu-id="a1b31-114">Die Zelle ViewMarkup wird ebenfalls auf WAHR festgelegt, wenn Kommentare in eine Zeichnung eingefügt werden (wobei es keine Rolle spielt, ob die Markupverfolgung aktiviert ist oder nicht) und muss auf WAHR festgelegt sein, damit die Kommentare in der Zeichnung sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="a1b31-114">The ViewMarkup cell is also set to TRUE when comments are inserted in a drawing (whether or not markup tracking is turned on) and must be TRUE to see comments in the drawing.</span></span>
  
<span data-ttu-id="a1b31-115">Diese Zelle entspricht dem Befehl **Markup anzeigen** in der Gruppe **Markup** der Registerkarte **Überprüfen**.</span><span class="sxs-lookup"><span data-stu-id="a1b31-115">This cell corresponds to the **Show Markup** command in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="a1b31-116">Wenn Sie einen Verweis auf die Zelle "ViewMarkup aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a1b31-116">To get a reference to the ViewMarkup cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1b31-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a1b31-117">Cell name:</span></span>  <br/> |<span data-ttu-id="a1b31-118">"ViewMarkup</span><span class="sxs-lookup"><span data-stu-id="a1b31-118">ViewMarkup</span></span>  <br/> |
   
<span data-ttu-id="a1b31-119">Wenn Sie einen Verweis auf die Zelle "ViewMarkup aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a1b31-119">To get a reference to the ViewMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1b31-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a1b31-120">Section index:</span></span>  <br/> |<span data-ttu-id="a1b31-121">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a1b31-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a1b31-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a1b31-122">Row index:</span></span>  <br/> |<span data-ttu-id="a1b31-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="a1b31-123">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="a1b31-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a1b31-124">Cell index:</span></span>  <br/> |<span data-ttu-id="a1b31-125">**visDocViewMarkup**</span><span class="sxs-lookup"><span data-stu-id="a1b31-125">**visDocViewMarkup**</span></span> <br/> |
   

