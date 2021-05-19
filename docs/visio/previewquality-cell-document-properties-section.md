---
title: Zelle "PreviewQuality" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm815
localization_priority: Normal
ms.assetid: b7d90666-a1bb-f0de-32da-b2855977f648
description: Bestimmt, ob die Zeichnungsvorschau Entwurfsqualität hat oder detailgetreu sein soll.
ms.openlocfilehash: 9db2d3e1eb829bfd2ad787fcfc94cd9ba5abaf9e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416818"
---
# <a name="previewquality-cell-document-properties-section"></a><span data-ttu-id="84605-103">Zelle "PreviewQuality" (Abschnitt "Document Properties")</span><span class="sxs-lookup"><span data-stu-id="84605-103">PreviewQuality Cell (Document Properties Section)</span></span>

<span data-ttu-id="84605-104">Bestimmt, ob die Zeichnungsvorschau Entwurfsqualität hat oder detailgetreu sein soll.</span><span class="sxs-lookup"><span data-stu-id="84605-104">Determines whether the drawing preview is draft quality or detailed.</span></span>
  
|<span data-ttu-id="84605-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="84605-105">**Value**</span></span>|<span data-ttu-id="84605-106">**PreviewQuality**</span><span class="sxs-lookup"><span data-stu-id="84605-106">**Preview quality**</span></span>|<span data-ttu-id="84605-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="84605-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="84605-108">0</span><span class="sxs-lookup"><span data-stu-id="84605-108">0</span></span>  <br/> | <span data-ttu-id="84605-109">Entwurf</span><span class="sxs-lookup"><span data-stu-id="84605-109">Draft</span></span>  <br/> |<span data-ttu-id="84605-110">**visDocPreviewQualityDraft**</span><span class="sxs-lookup"><span data-stu-id="84605-110">**visDocPreviewQualityDraft**</span></span> <br/> |
| <span data-ttu-id="84605-111">1</span><span class="sxs-lookup"><span data-stu-id="84605-111">1</span></span>  <br/> | <span data-ttu-id="84605-112">Detailliert</span><span class="sxs-lookup"><span data-stu-id="84605-112">Detailed</span></span>  <br/> |<span data-ttu-id="84605-113">**visDocPreviewQualityDetailed**</span><span class="sxs-lookup"><span data-stu-id="84605-113">**visDocPreviewQualityDetailed**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84605-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="84605-114">Remarks</span></span>

<span data-ttu-id="84605-115">Sie können diesen Wert  auch auf  der Registerkarte Zusammenfassung im Dialogfeld Eigenschaften festlegen (klicken Sie auf die Schaltfläche **Office,** klicken Sie auf die Registerkarte **Info,** klicken Sie auf Dokumenteigenschaften **und** dann auf **Erweiterte Eigenschaften**).</span><span class="sxs-lookup"><span data-stu-id="84605-115">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="84605-116">Um einen Verweis auf die Zelle PreviewQuality anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="84605-116">To get a reference to the PreviewQuality cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="84605-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="84605-117">Cell name:</span></span>  <br/> | <span data-ttu-id="84605-118">PreviewQuality</span><span class="sxs-lookup"><span data-stu-id="84605-118">PreviewQuality</span></span>  <br/> |
   
<span data-ttu-id="84605-119">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle PreviewQuality nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="84605-119">To get a reference to the PreviewQuality cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="84605-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="84605-120">Section index:</span></span>  <br/> |<span data-ttu-id="84605-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="84605-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="84605-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="84605-122">Row index:</span></span>  <br/> |<span data-ttu-id="84605-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="84605-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="84605-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="84605-124">Cell index:</span></span>  <br/> |<span data-ttu-id="84605-125">**visDocPreviewQuality**</span><span class="sxs-lookup"><span data-stu-id="84605-125">**visDocPreviewQuality**</span></span> <br/> |
   

