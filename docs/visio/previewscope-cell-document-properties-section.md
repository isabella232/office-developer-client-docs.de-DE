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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356112"
---
# <a name="previewscope-cell-document-properties-section"></a><span data-ttu-id="531fc-104">Zelle "PreviewScope" (Abschnitt "Document Properties")</span><span class="sxs-lookup"><span data-stu-id="531fc-104">PreviewScope Cell (Document Properties Section)</span></span>

<span data-ttu-id="531fc-p102">Legt fest, ob die Zeichnung eine Vorschau mit einschließt. Wenn die Zeichnung eine Vorschau mit einschließt, wird hier definiert, ob die Vorschau nur die erste Seite oder alle Seiten der Zeichnung zeigt.</span><span class="sxs-lookup"><span data-stu-id="531fc-p102">Determines whether your drawing includes a preview. If your drawing does include a preview, it determines whether the preview shows the first page only or all of the pages in the drawing.</span></span>
  
|<span data-ttu-id="531fc-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="531fc-107">**Value**</span></span>|<span data-ttu-id="531fc-108">**Umfang der Vorschau**</span><span class="sxs-lookup"><span data-stu-id="531fc-108">**Preview scope**</span></span>|<span data-ttu-id="531fc-109">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="531fc-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="531fc-110">0</span><span class="sxs-lookup"><span data-stu-id="531fc-110">0</span></span>  <br/> | <span data-ttu-id="531fc-111">Erste Seite</span><span class="sxs-lookup"><span data-stu-id="531fc-111">First page</span></span>  <br/> |<span data-ttu-id="531fc-112">**visDocPreviewScope1stPage**</span><span class="sxs-lookup"><span data-stu-id="531fc-112">**visDocPreviewScope1stPage**</span></span> <br/> |
| <span data-ttu-id="531fc-113">1</span><span class="sxs-lookup"><span data-stu-id="531fc-113">1</span></span>  <br/> | <span data-ttu-id="531fc-114">Keine</span><span class="sxs-lookup"><span data-stu-id="531fc-114">None</span></span>  <br/> |<span data-ttu-id="531fc-115">**visDocPreviewScopeNone**</span><span class="sxs-lookup"><span data-stu-id="531fc-115">**visDocPreviewScopeNone**</span></span> <br/> |
| <span data-ttu-id="531fc-116">2</span><span class="sxs-lookup"><span data-stu-id="531fc-116">2</span></span>  <br/> | <span data-ttu-id="531fc-117">Alle Seiten</span><span class="sxs-lookup"><span data-stu-id="531fc-117">All pages</span></span>  <br/> |<span data-ttu-id="531fc-118">**visDocPreviewScopeAllPages**</span><span class="sxs-lookup"><span data-stu-id="531fc-118">**visDocPreviewScopeAllPages**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="531fc-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="531fc-119">Remarks</span></span>

<span data-ttu-id="531fc-120">Sie können diesen Wert auch im Dialogfeld **Eigenschaften** auf der Registerkarte **Zusammenfassung** festlegen (Klicken Sie auf die **Office** -Schaltfläche, klicken Sie auf die Registerkarte **Info** , klicken Sie auf **Dokumenteigenschaften**und dann auf **Erweiterte Eigenschaften**).</span><span class="sxs-lookup"><span data-stu-id="531fc-120">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="531fc-121">Wenn Sie einen Verweis auf die Zelle "PreviewScope aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="531fc-121">To get a reference to the PreviewScope cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="531fc-122">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="531fc-122">Cell name:</span></span>  <br/> | <span data-ttu-id="531fc-123">"PreviewScope</span><span class="sxs-lookup"><span data-stu-id="531fc-123">PreviewScope</span></span>  <br/> |
   
<span data-ttu-id="531fc-124">Wenn Sie einen Verweis auf die Zelle "PreviewScope aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="531fc-124">To get a reference to the PreviewScope cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="531fc-125">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="531fc-125">Section index:</span></span>  <br/> |<span data-ttu-id="531fc-126">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="531fc-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="531fc-127">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="531fc-127">Row index:</span></span>  <br/> |<span data-ttu-id="531fc-128">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="531fc-128">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="531fc-129">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="531fc-129">Cell index:</span></span>  <br/> |<span data-ttu-id="531fc-130">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="531fc-130">**visDocPreviewScope**</span></span> <br/> |
   

