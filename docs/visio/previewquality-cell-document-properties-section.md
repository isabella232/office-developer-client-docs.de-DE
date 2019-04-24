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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356035"
---
# <a name="previewquality-cell-document-properties-section"></a><span data-ttu-id="55872-103">Zelle "PreviewQuality" (Abschnitt "Document Properties")</span><span class="sxs-lookup"><span data-stu-id="55872-103">PreviewQuality Cell (Document Properties Section)</span></span>

<span data-ttu-id="55872-104">Bestimmt, ob die Zeichnungsvorschau Entwurfsqualität hat oder detailgetreu sein soll.</span><span class="sxs-lookup"><span data-stu-id="55872-104">Determines whether the drawing preview is draft quality or detailed.</span></span>
  
|<span data-ttu-id="55872-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="55872-105">**Value**</span></span>|<span data-ttu-id="55872-106">**PreviewQuality**</span><span class="sxs-lookup"><span data-stu-id="55872-106">**Preview quality**</span></span>|<span data-ttu-id="55872-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="55872-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="55872-108">0</span><span class="sxs-lookup"><span data-stu-id="55872-108">0</span></span>  <br/> | <span data-ttu-id="55872-109">Entwurf</span><span class="sxs-lookup"><span data-stu-id="55872-109">Draft</span></span>  <br/> |<span data-ttu-id="55872-110">**visDocPreviewQualityDraft**</span><span class="sxs-lookup"><span data-stu-id="55872-110">**visDocPreviewQualityDraft**</span></span> <br/> |
| <span data-ttu-id="55872-111">1</span><span class="sxs-lookup"><span data-stu-id="55872-111">1</span></span>  <br/> | <span data-ttu-id="55872-112">Detaillierte</span><span class="sxs-lookup"><span data-stu-id="55872-112">Detailed</span></span>  <br/> |<span data-ttu-id="55872-113">**visDocPreviewQualityDetailed**</span><span class="sxs-lookup"><span data-stu-id="55872-113">**visDocPreviewQualityDetailed**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55872-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55872-114">Remarks</span></span>

<span data-ttu-id="55872-115">Sie können diesen Wert auch im Dialogfeld **Eigenschaften** auf der Registerkarte **Zusammenfassung** festlegen (Klicken Sie auf die **Office** -Schaltfläche, klicken Sie auf die Registerkarte **Info** , klicken Sie auf **Dokumenteigenschaften**und dann auf **Erweiterte Eigenschaften**).</span><span class="sxs-lookup"><span data-stu-id="55872-115">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="55872-116">Wenn Sie einen Verweis auf die Zelle "PreviewQuality aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="55872-116">To get a reference to the PreviewQuality cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="55872-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="55872-117">Cell name:</span></span>  <br/> | <span data-ttu-id="55872-118">"PreviewQuality</span><span class="sxs-lookup"><span data-stu-id="55872-118">PreviewQuality</span></span>  <br/> |
   
<span data-ttu-id="55872-119">Wenn Sie einen Verweis auf die Zelle "PreviewQuality aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="55872-119">To get a reference to the PreviewQuality cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="55872-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="55872-120">Section index:</span></span>  <br/> |<span data-ttu-id="55872-121">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="55872-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="55872-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="55872-122">Row index:</span></span>  <br/> |<span data-ttu-id="55872-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="55872-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="55872-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="55872-124">Cell index:</span></span>  <br/> |<span data-ttu-id="55872-125">**visDocPreviewQuality**</span><span class="sxs-lookup"><span data-stu-id="55872-125">**visDocPreviewQuality**</span></span> <br/> |
   

