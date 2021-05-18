---
title: Zelle "ComplexScriptFont" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60034
localization_priority: Normal
ms.assetid: e1cf9e97-101b-384f-65fe-0169c89dfccc
description: Enthält die Nummer der Schriftart, die zum Formatieren von Text mit komplexen Schriftzeichen verwendet wird. Nummern von Schriftarten variieren entsprechend den im System installierten Schriftarten.
ms.openlocfilehash: 5ec8deb59b875a01592b6d7b652204089ecf11e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404834"
---
# <a name="complexscriptfont-cell-character-section"></a><span data-ttu-id="d27b1-104">Zelle "ComplexScriptFont" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="d27b1-104">ComplexScriptFont Cell (Character Section)</span></span>

<span data-ttu-id="d27b1-p102">Enthält die Nummer der Schriftart, die zum Formatieren von Text mit komplexen Schriftzeichen verwendet wird. Nummern von Schriftarten variieren entsprechend den im System installierten Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="d27b1-p102">Contains the number of the font used to format text composed of complex script characters. Font numbers vary according to the fonts installed on your system.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d27b1-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d27b1-107">Remarks</span></span>

<span data-ttu-id="d27b1-108">Komplexe Schriftgrößen für Skripts werden auf der Registerkarte **Schriftart** im  Dialogfeld **Text** aufgeführt (klicken Sie auf der Registerkarte **Start** auf den Pfeil in der Gruppe Schriftart).</span><span class="sxs-lookup"><span data-stu-id="d27b1-108">Complex script font sizes are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="d27b1-109">Diese Liste wird nur angezeigt, wenn Sie eine Sprache mit  asiatischen oder komplexen Skriptzeichen im Dialogfeld Spracheinstellungen Microsoft Office hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="d27b1-109">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="d27b1-110">(Klicken **Sie auf Start,** **klicken** Sie auf Alle Programme, **Microsoft Office**, klicken Sie **Microsoft Office Tools,** und klicken Sie **dann auf Microsoft Office Spracheinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="d27b1-110">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="d27b1-111">Die Nummer Null (0) bedeutet, dass keine Schriftart festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d27b1-111">The number 0 (zero) means no font is specified.</span></span> <span data-ttu-id="d27b1-112">Die Schriftart Latein oder die Standardschriftarten werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="d27b1-112">The Latin font or default fonts are used.</span></span>
  
<span data-ttu-id="d27b1-113">Verwenden Sie zum Erhalten eines Verweises auf die Zelle ComplexScriptSize anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="d27b1-113">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d27b1-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d27b1-114">Cell name:</span></span>  <br/> |<span data-ttu-id="d27b1-115">Char.ComplexScriptFont[ *i*  ] wobei  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d27b1-115">Char.ComplexScriptFont[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d27b1-116">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ComplexScriptFont-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="d27b1-116">To get a reference to the ComplexScriptFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d27b1-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d27b1-117">Section index:</span></span>  <br/> |<span data-ttu-id="d27b1-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="d27b1-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="d27b1-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d27b1-119">Row index:</span></span>  <br/> |<span data-ttu-id="d27b1-120">**visRowCharacter**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d27b1-120">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="d27b1-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="d27b1-121">Cell index:</span></span>  <br/> |<span data-ttu-id="d27b1-122">**visCharacterComplexScriptFont**</span><span class="sxs-lookup"><span data-stu-id="d27b1-122">**visCharacterComplexScriptFont**</span></span> <br/> |
   

