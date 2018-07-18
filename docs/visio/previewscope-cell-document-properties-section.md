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
ms.openlocfilehash: 865da052f710481c146d3c2692ddf506018be789
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797721"
---
# <a name="previewscope-cell-document-properties-section"></a><span data-ttu-id="507ee-104">PreviewScope Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="507ee-104">PreviewScope Cell (Document Properties Section)</span></span>

<span data-ttu-id="507ee-p102">Legt fest, ob die Zeichnung eine Vorschau mit einschließt. Wenn die Zeichnung eine Vorschau mit einschließt, wird hier definiert, ob die Vorschau nur die erste Seite oder alle Seiten der Zeichnung zeigt.</span><span class="sxs-lookup"><span data-stu-id="507ee-p102">Determines whether your drawing includes a preview. If your drawing does include a preview, it determines whether the preview shows the first page only or all of the pages in the drawing.</span></span>
  
|<span data-ttu-id="507ee-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="507ee-107">**Value**</span></span>|<span data-ttu-id="507ee-108">**Umfang der Vorschau**</span><span class="sxs-lookup"><span data-stu-id="507ee-108">**Preview scope**</span></span>|<span data-ttu-id="507ee-109">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="507ee-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="507ee-110">0</span><span class="sxs-lookup"><span data-stu-id="507ee-110">0</span></span>  <br/> | <span data-ttu-id="507ee-111">Erste Seite</span><span class="sxs-lookup"><span data-stu-id="507ee-111">First page</span></span>  <br/> |<span data-ttu-id="507ee-112">**visDocPreviewScope1stPage**</span><span class="sxs-lookup"><span data-stu-id="507ee-112">**visDocPreviewScope1stPage**</span></span> <br/> |
| <span data-ttu-id="507ee-113">1</span><span class="sxs-lookup"><span data-stu-id="507ee-113">1</span></span>  <br/> | <span data-ttu-id="507ee-114">Keine</span><span class="sxs-lookup"><span data-stu-id="507ee-114">None</span></span>  <br/> |<span data-ttu-id="507ee-115">**visDocPreviewScopeNone**</span><span class="sxs-lookup"><span data-stu-id="507ee-115">**visDocPreviewScopeNone**</span></span> <br/> |
| <span data-ttu-id="507ee-116">2</span><span class="sxs-lookup"><span data-stu-id="507ee-116">2</span></span>  <br/> | <span data-ttu-id="507ee-117">Alle Seiten</span><span class="sxs-lookup"><span data-stu-id="507ee-117">All pages</span></span>  <br/> |<span data-ttu-id="507ee-118">**visDocPreviewScopeAllPages**</span><span class="sxs-lookup"><span data-stu-id="507ee-118">**visDocPreviewScopeAllPages**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="507ee-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="507ee-119">Remarks</span></span>

<span data-ttu-id="507ee-120">Sie können diesen Wert auch auf der Registerkarte **Zusammenfassung** im Dialogfeld **Eigenschaften** festlegen (klicken Sie auf die **Office** -Schaltfläche, klicken Sie auf der Registerkarte **Info** , klicken Sie auf **Dokumenteigenschaften**, und klicken Sie dann auf **Erweiterte Eigenschaften**).</span><span class="sxs-lookup"><span data-stu-id="507ee-120">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="507ee-121">Wenn Sie einen Verweis auf die Zelle PreviewScope aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="507ee-121">To get a reference to the PreviewScope cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="507ee-122">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="507ee-122">Cell name:</span></span>  <br/> | <span data-ttu-id="507ee-123">PreviewScope</span><span class="sxs-lookup"><span data-stu-id="507ee-123">PreviewScope</span></span>  <br/> |
   
<span data-ttu-id="507ee-124">Wenn Sie einen Verweis auf die Zelle PreviewScope aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="507ee-124">To get a reference to the PreviewScope cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="507ee-125">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="507ee-125">Section index:</span></span>  <br/> |<span data-ttu-id="507ee-126">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="507ee-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="507ee-127">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="507ee-127">Row index:</span></span>  <br/> |<span data-ttu-id="507ee-128">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="507ee-128">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="507ee-129">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="507ee-129">Cell index:</span></span>  <br/> |<span data-ttu-id="507ee-130">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="507ee-130">**visDocPreviewScope**</span></span> <br/> |
   

