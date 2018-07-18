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
ms.openlocfilehash: bc8a53934b6dad06a0867cc73cdfacfa02d2b438
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797707"
---
# <a name="previewquality-cell-document-properties-section"></a><span data-ttu-id="c9063-103">PreviewQuality Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="c9063-103">PreviewQuality Cell (Document Properties Section)</span></span>

<span data-ttu-id="c9063-104">Bestimmt, ob die Zeichnungsvorschau Entwurfsqualität hat oder detailgetreu sein soll.</span><span class="sxs-lookup"><span data-stu-id="c9063-104">Determines whether the drawing preview is draft quality or detailed.</span></span>
  
|<span data-ttu-id="c9063-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c9063-105">**Value**</span></span>|<span data-ttu-id="c9063-106">**PreviewQuality**</span><span class="sxs-lookup"><span data-stu-id="c9063-106">**Preview quality**</span></span>|<span data-ttu-id="c9063-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="c9063-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="c9063-108">0</span><span class="sxs-lookup"><span data-stu-id="c9063-108">0</span></span>  <br/> | <span data-ttu-id="c9063-109">Entwurf</span><span class="sxs-lookup"><span data-stu-id="c9063-109">Draft</span></span>  <br/> |<span data-ttu-id="c9063-110">**visDocPreviewQualityDraft**</span><span class="sxs-lookup"><span data-stu-id="c9063-110">**visDocPreviewQualityDraft**</span></span> <br/> |
| <span data-ttu-id="c9063-111">1</span><span class="sxs-lookup"><span data-stu-id="c9063-111">1</span></span>  <br/> | <span data-ttu-id="c9063-112">Detailliert</span><span class="sxs-lookup"><span data-stu-id="c9063-112">Detailed</span></span>  <br/> |<span data-ttu-id="c9063-113">**visDocPreviewQualityDetailed**</span><span class="sxs-lookup"><span data-stu-id="c9063-113">**visDocPreviewQualityDetailed**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9063-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9063-114">Remarks</span></span>

<span data-ttu-id="c9063-115">Sie können diesen Wert auch auf der Registerkarte **Zusammenfassung** im Dialogfeld **Eigenschaften** festlegen (klicken Sie auf die **Office** -Schaltfläche, klicken Sie auf der Registerkarte **Info** , klicken Sie auf **Dokumenteigenschaften**, und klicken Sie dann auf **Erweiterte Eigenschaften**).</span><span class="sxs-lookup"><span data-stu-id="c9063-115">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="c9063-116">Wenn Sie einen Verweis auf die Zelle PreviewQuality aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c9063-116">To get a reference to the PreviewQuality cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c9063-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="c9063-117">Cell name:</span></span>  <br/> | <span data-ttu-id="c9063-118">PreviewQuality</span><span class="sxs-lookup"><span data-stu-id="c9063-118">PreviewQuality</span></span>  <br/> |
   
<span data-ttu-id="c9063-119">Wenn Sie einen Verweis auf die Zelle PreviewQuality aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="c9063-119">To get a reference to the PreviewQuality cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c9063-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="c9063-120">Section index:</span></span>  <br/> |<span data-ttu-id="c9063-121">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c9063-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c9063-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c9063-122">Row index:</span></span>  <br/> |<span data-ttu-id="c9063-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="c9063-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="c9063-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="c9063-124">Cell index:</span></span>  <br/> |<span data-ttu-id="c9063-125">**visDocPreviewQuality**</span><span class="sxs-lookup"><span data-stu-id="c9063-125">**visDocPreviewQuality**</span></span> <br/> |
   

