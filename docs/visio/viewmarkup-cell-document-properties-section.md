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
ms.openlocfilehash: dda908595b243878ec755cf73351ec1fd672dc55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798403"
---
# <a name="viewmarkup-cell-document-properties-section"></a><span data-ttu-id="5b0ce-103">ViewMarkup Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="5b0ce-103">ViewMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="5b0ce-104">Bestimmt, ob im Zeichnungsfenster Markup angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5b0ce-104">Determines whether markup appears in the drawing window.</span></span> 
  
|<span data-ttu-id="5b0ce-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5b0ce-105">**Value**</span></span>|<span data-ttu-id="5b0ce-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b0ce-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5b0ce-107">WAHR</span><span class="sxs-lookup"><span data-stu-id="5b0ce-107">TRUE</span></span>  <br/> |<span data-ttu-id="5b0ce-108">Markup wird in der Zeichnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5b0ce-108">Markup is displayed on the drawing.</span></span>  <br/> |
|<span data-ttu-id="5b0ce-109">FALSCH</span><span class="sxs-lookup"><span data-stu-id="5b0ce-109">FALSE</span></span>  <br/> |<span data-ttu-id="5b0ce-110">Markup wird nicht angezeigt (Standardwert).</span><span class="sxs-lookup"><span data-stu-id="5b0ce-110">Markup is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b0ce-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b0ce-111">Remarks</span></span>

 <span data-ttu-id="5b0ce-112">Wenn Markup verfolgen aktiviert ist (die Zelle AddMarkup ist TRUE), die Zelle ViewMarkup automatisch auf TRUE festgelegt ist und der Wert WAHR auch nach dem Markup verfolgen deaktiviert ist (die Zelle AddMarkup ist FALSE).</span><span class="sxs-lookup"><span data-stu-id="5b0ce-112">When markup tracking is turned on (AddMarkup cell is TRUE), the ViewMarkup cell is automatically set to TRUE and remains TRUE even after markup tracking has been turned off (AddMarkup cell is FALSE).</span></span> <span data-ttu-id="5b0ce-113">Der Wert in der Zelle ViewMarkup wird ignoriert, wenn die Zelle AddMarkup auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5b0ce-113">The value in the ViewMarkup cell is ignored when the AddMarkup cell is TRUE.</span></span> 
  
<span data-ttu-id="5b0ce-114">Die Zelle ViewMarkup wird ebenfalls auf WAHR festgelegt, wenn Kommentare in eine Zeichnung eingefügt werden (wobei es keine Rolle spielt, ob die Markupverfolgung aktiviert ist oder nicht) und muss auf WAHR festgelegt sein, damit die Kommentare in der Zeichnung sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="5b0ce-114">The ViewMarkup cell is also set to TRUE when comments are inserted in a drawing (whether or not markup tracking is turned on) and must be TRUE to see comments in the drawing.</span></span>
  
<span data-ttu-id="5b0ce-115">Diese Zelle entspricht dem Befehl **Markup anzeigen** in der Gruppe **Markup** der Registerkarte **Überprüfen** .</span><span class="sxs-lookup"><span data-stu-id="5b0ce-115">This cell corresponds to the **Show Markup** command in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="5b0ce-116">Zum Abrufen eines Verweises auf die Zelle ViewMarkup nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5b0ce-116">To get a reference to the ViewMarkup cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5b0ce-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5b0ce-117">Cell name:</span></span>  <br/> |<span data-ttu-id="5b0ce-118">ViewMarkup</span><span class="sxs-lookup"><span data-stu-id="5b0ce-118">ViewMarkup</span></span>  <br/> |
   
<span data-ttu-id="5b0ce-119">Wenn Sie einen Verweis auf die Zelle ViewMarkup aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="5b0ce-119">To get a reference to the ViewMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5b0ce-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5b0ce-120">Section index:</span></span>  <br/> |<span data-ttu-id="5b0ce-121">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5b0ce-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5b0ce-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5b0ce-122">Row index:</span></span>  <br/> |<span data-ttu-id="5b0ce-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="5b0ce-123">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="5b0ce-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5b0ce-124">Cell index:</span></span>  <br/> |<span data-ttu-id="5b0ce-125">**visDocViewMarkup**</span><span class="sxs-lookup"><span data-stu-id="5b0ce-125">**visDocViewMarkup**</span></span> <br/> |
   

