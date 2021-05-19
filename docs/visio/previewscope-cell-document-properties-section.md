---
title: Zelle "PreviewScope" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm820
localization_priority: Normal
ms.assetid: d03ae1b3-da6c-56d3-4f96-6e131c04e93e
description: Legt fest, ob die Zeichnung eine Vorschau mit einschließt. Wenn die Zeichnung eine Vorschau mit einschließt, wird hier definiert, ob die Vorschau nur die erste Seite oder alle Seiten der Zeichnung zeigt.
ms.openlocfilehash: 34dbc9ac02032b2cb5cb6373c3c6361e3d822312
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426506"
---
# <a name="previewscope-cell-document-properties-section"></a><span data-ttu-id="719c0-104">Zelle "PreviewScope" (Abschnitt "Document Properties")</span><span class="sxs-lookup"><span data-stu-id="719c0-104">PreviewScope Cell (Document Properties Section)</span></span>

<span data-ttu-id="719c0-p102">Legt fest, ob die Zeichnung eine Vorschau mit einschließt. Wenn die Zeichnung eine Vorschau mit einschließt, wird hier definiert, ob die Vorschau nur die erste Seite oder alle Seiten der Zeichnung zeigt.</span><span class="sxs-lookup"><span data-stu-id="719c0-p102">Determines whether your drawing includes a preview. If your drawing does include a preview, it determines whether the preview shows the first page only or all of the pages in the drawing.</span></span>
  
|<span data-ttu-id="719c0-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="719c0-107">**Value**</span></span>|<span data-ttu-id="719c0-108">**Umfang der Vorschau**</span><span class="sxs-lookup"><span data-stu-id="719c0-108">**Preview scope**</span></span>|<span data-ttu-id="719c0-109">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="719c0-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="719c0-110">0</span><span class="sxs-lookup"><span data-stu-id="719c0-110">0</span></span>  <br/> | <span data-ttu-id="719c0-111">Erste Seite</span><span class="sxs-lookup"><span data-stu-id="719c0-111">First page</span></span>  <br/> |<span data-ttu-id="719c0-112">**visDocPreviewScope1stPage**</span><span class="sxs-lookup"><span data-stu-id="719c0-112">**visDocPreviewScope1stPage**</span></span> <br/> |
| <span data-ttu-id="719c0-113">1</span><span class="sxs-lookup"><span data-stu-id="719c0-113">1</span></span>  <br/> | <span data-ttu-id="719c0-114">Keinen</span><span class="sxs-lookup"><span data-stu-id="719c0-114">None</span></span>  <br/> |<span data-ttu-id="719c0-115">**visDocPreviewScopeNone**</span><span class="sxs-lookup"><span data-stu-id="719c0-115">**visDocPreviewScopeNone**</span></span> <br/> |
| <span data-ttu-id="719c0-116">2</span><span class="sxs-lookup"><span data-stu-id="719c0-116">2</span></span>  <br/> | <span data-ttu-id="719c0-117">Alle Seiten</span><span class="sxs-lookup"><span data-stu-id="719c0-117">All pages</span></span>  <br/> |<span data-ttu-id="719c0-118">**visDocPreviewScopeAllPages**</span><span class="sxs-lookup"><span data-stu-id="719c0-118">**visDocPreviewScopeAllPages**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="719c0-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="719c0-119">Remarks</span></span>

<span data-ttu-id="719c0-120">Sie können diesen Wert  auch auf  der Registerkarte Zusammenfassung im Dialogfeld Eigenschaften festlegen (klicken Sie auf die Schaltfläche **Office,** klicken Sie auf die Registerkarte **Info,** klicken Sie auf Dokumenteigenschaften **und** dann auf **Erweiterte Eigenschaften**).</span><span class="sxs-lookup"><span data-stu-id="719c0-120">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="719c0-121">Um einen Verweis auf die Zelle PreviewScope anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="719c0-121">To get a reference to the PreviewScope cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="719c0-122">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="719c0-122">Cell name:</span></span>  <br/> | <span data-ttu-id="719c0-123">PreviewScope</span><span class="sxs-lookup"><span data-stu-id="719c0-123">PreviewScope</span></span>  <br/> |
   
<span data-ttu-id="719c0-124">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle PreviewScope nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="719c0-124">To get a reference to the PreviewScope cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="719c0-125">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="719c0-125">Section index:</span></span>  <br/> |<span data-ttu-id="719c0-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="719c0-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="719c0-127">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="719c0-127">Row index:</span></span>  <br/> |<span data-ttu-id="719c0-128">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="719c0-128">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="719c0-129">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="719c0-129">Cell index:</span></span>  <br/> |<span data-ttu-id="719c0-130">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="719c0-130">**visDocPreviewScope**</span></span> <br/> |
   

