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
ms.openlocfilehash: af1e79b13d3d8bab2e7271eb79e68cf931871806
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413115"
---
# <a name="flags-cell-paragraph-section"></a><span data-ttu-id="7ddd3-103">Zelle "Flags" (Abschnitt "Paragraph")</span><span class="sxs-lookup"><span data-stu-id="7ddd3-103">Flags Cell (Paragraph Section)</span></span>

<span data-ttu-id="7ddd3-104">Gibt an, ob die Textrichtung von links nach rechts oder von rechts nach links verläuft.</span><span class="sxs-lookup"><span data-stu-id="7ddd3-104">Indicates whether the text direction is left to right or right to left.</span></span>
  
|<span data-ttu-id="7ddd3-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7ddd3-105">**Value**</span></span>|<span data-ttu-id="7ddd3-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7ddd3-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7ddd3-107">0</span><span class="sxs-lookup"><span data-stu-id="7ddd3-107">0</span></span>  <br/> |<span data-ttu-id="7ddd3-108">Die Textrichtung verläuft von links nach rechts (Standardwert).</span><span class="sxs-lookup"><span data-stu-id="7ddd3-108">The text direction is left to right (the default).</span></span>  <br/> |
|<span data-ttu-id="7ddd3-109">1</span><span class="sxs-lookup"><span data-stu-id="7ddd3-109">1</span></span>  <br/> |<span data-ttu-id="7ddd3-110">Die Textrichtung verläuft von rechts nach links.</span><span class="sxs-lookup"><span data-stu-id="7ddd3-110">The text direction is right to left.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7ddd3-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ddd3-111">Remarks</span></span>

<span data-ttu-id="7ddd3-112">Der Wert in dieser Zelle entspricht der Einstellung **Richtung** auf der Registerkarte **Absatz** im Dialogfeld **Text** (Klicken Sie auf der Registerkarte **Start** auf den Pfeil für die **Schriftart** ), der nur angezeigt wird, wenn eine Sprache, die den Text komplexer Skripts verwendet, im Dialogfeld **Microsoft Office-Spracheinstellungen** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ddd3-112">The value in this cell corresponds to the **Direction** setting on the **Paragraph** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow), which appears only if a language that uses complex scripts text has been added in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="7ddd3-113">(Klicken Sie auf **Start**, **Alle Programme**, **Microsoft Office**, Microsoft Office- **Tools**und dann auf **Microsoft Office-Spracheinstellungen**.)</span><span class="sxs-lookup"><span data-stu-id="7ddd3-113">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.)</span></span> 
  
<span data-ttu-id="7ddd3-114">Wenn Sie einen Verweis auf die Zelle Flags aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7ddd3-114">To get a reference to the Flags cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7ddd3-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="7ddd3-115">Cell name:</span></span>  <br/> |<span data-ttu-id="7ddd3-116">Para. Flags [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="7ddd3-116">Para.Flags[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7ddd3-117">Wenn Sie einen Verweis auf die Zelle Flags aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="7ddd3-117">To get a reference to the Flags cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7ddd3-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="7ddd3-118">Section index:</span></span>  <br/> |<span data-ttu-id="7ddd3-119">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="7ddd3-119">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="7ddd3-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="7ddd3-120">Row index:</span></span>  <br/> |<span data-ttu-id="7ddd3-121">**visRowParagraph** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7ddd3-121">**visRowParagraph** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="7ddd3-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="7ddd3-122">Cell index:</span></span>  <br/> |<span data-ttu-id="7ddd3-123">**visFlags**</span><span class="sxs-lookup"><span data-stu-id="7ddd3-123">**visFlags**</span></span> <br/> |
   

