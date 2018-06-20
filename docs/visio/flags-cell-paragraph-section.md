---
title: Zelle "Flags" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033782
localization_priority: Normal
ms.assetid: 898bf89d-d00f-9769-a89d-787ef708eca5
description: Gibt an, ob die Textrichtung von links nach rechts oder von rechts nach links verläuft.
ms.openlocfilehash: b471d08556bedf68ce75595b9c211758297e8352
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797010"
---
# <a name="flags-cell-paragraph-section"></a><span data-ttu-id="911d2-103">Flags Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="911d2-103">Flags Cell (Paragraph Section)</span></span>

<span data-ttu-id="911d2-104">Gibt an, ob die Textrichtung von links nach rechts oder von rechts nach links verläuft.</span><span class="sxs-lookup"><span data-stu-id="911d2-104">Indicates whether the text direction is left to right or right to left.</span></span>
  
|<span data-ttu-id="911d2-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="911d2-105">**Value**</span></span>|<span data-ttu-id="911d2-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="911d2-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="911d2-107">0</span><span class="sxs-lookup"><span data-stu-id="911d2-107">0</span></span>  <br/> |<span data-ttu-id="911d2-108">Die Textrichtung verläuft von links nach rechts (Standardwert).</span><span class="sxs-lookup"><span data-stu-id="911d2-108">The text direction is left to right (the default).</span></span>  <br/> |
|<span data-ttu-id="911d2-109">1</span><span class="sxs-lookup"><span data-stu-id="911d2-109">1</span></span>  <br/> |<span data-ttu-id="911d2-110">Die Textrichtung verläuft von rechts nach links.</span><span class="sxs-lookup"><span data-stu-id="911d2-110">The text direction is right to left.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="911d2-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="911d2-111">Remarks</span></span>

<span data-ttu-id="911d2-112">Der Wert in dieser Zelle entspricht der Einstellung **Richtung** auf der Registerkarte **Absatz** im Dialogfeld **Text** (auf der Registerkarte **Start** , klicken Sie auf den Pfeil neben **Schriftart** ), die angezeigt wird, wenn eine Sprache, die komplexe verwendet Text Skripts wurde Klicken Sie im Dialogfeld **Microsoft Office-Spracheinstellungen** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="911d2-112">The value in this cell corresponds to the **Direction** setting on the **Paragraph** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow), which appears only if a language that uses complex scripts text has been added in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="911d2-113">(Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft Office**, klicken Sie auf **Microsoft Office Tools**, und klicken Sie dann auf **Microsoft Office-Spracheinstellungen**.)</span><span class="sxs-lookup"><span data-stu-id="911d2-113">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.)</span></span> 
  
<span data-ttu-id="911d2-114">Wenn Sie einen Verweis auf die Zelle Flags nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="911d2-114">To get a reference to the Flags cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="911d2-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="911d2-115">Cell name:</span></span>  <br/> |<span data-ttu-id="911d2-116">Para.Flags [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="911d2-116">Para.Flags[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="911d2-117">Wenn Sie einen Verweis auf die Zelle Flags aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="911d2-117">To get a reference to the Flags cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="911d2-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="911d2-118">Section index:</span></span>  <br/> |<span data-ttu-id="911d2-119">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="911d2-119">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="911d2-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="911d2-120">Row index:</span></span>  <br/> |<span data-ttu-id="911d2-121">**VisRowParagraph** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="911d2-121">**visRowParagraph** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="911d2-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="911d2-122">Cell index:</span></span>  <br/> |<span data-ttu-id="911d2-123">**visFlags**</span><span class="sxs-lookup"><span data-stu-id="911d2-123">**visFlags**</span></span> <br/> |
   

