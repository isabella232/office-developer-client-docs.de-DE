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
ms.openlocfilehash: 0aae3a22be26f206763f18107eaced74f1078503
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796680"
---
# <a name="complexscriptfont-cell-character-section"></a><span data-ttu-id="7a878-104">ComplexScriptFont Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="7a878-104">ComplexScriptFont Cell (Character Section)</span></span>

<span data-ttu-id="7a878-p102">Enthält die Nummer der Schriftart, die zum Formatieren von Text mit komplexen Schriftzeichen verwendet wird. Nummern von Schriftarten variieren entsprechend den im System installierten Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="7a878-p102">Contains the number of the font used to format text composed of complex script characters. Font numbers vary according to the fonts installed on your system.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7a878-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a878-107">Remarks</span></span>

<span data-ttu-id="7a878-108">Komplexe Schriftzeichen Schriftgrade sind aufgelistet, auf der Registerkarte **Schriftart** im Dialogfeld **Text** verwenden (klicken Sie auf der Pfeil in der **Schriftart** auf der Registerkarte **Start** gruppieren).</span><span class="sxs-lookup"><span data-stu-id="7a878-108">Complex script font sizes are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="7a878-109">Diese Liste wird nur dann, wenn Sie eine Sprache hinzugefügt haben, die asiatische Sprachen oder komplexe Schriftzeichen, klicken Sie im Dialogfeld **Microsoft Office-Spracheinstellungen** enthält.</span><span class="sxs-lookup"><span data-stu-id="7a878-109">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="7a878-110">(Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft Office**, klicken Sie auf **Microsoft Office Tools**, und klicken Sie dann auf **Microsoft Office-Spracheinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="7a878-110">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="7a878-111">Die Zahl 0 (null) bedeutet, dass keine Schriftart festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7a878-111">The number 0 (zero) means no font is specified.</span></span> <span data-ttu-id="7a878-112">Die Lateinische Schriftart oder den Standard-Schriftarten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a878-112">The Latin font or default fonts are used.</span></span>
  
<span data-ttu-id="7a878-113">Wenn Sie einen Verweis auf die Zelle ComplexScriptSize aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7a878-113">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7a878-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="7a878-114">Cell name:</span></span>  <br/> |<span data-ttu-id="7a878-115">Char.ComplexScriptFont [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="7a878-115">Char.ComplexScriptFont[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7a878-116">Wenn Sie einen Verweis auf die Zelle ComplexScriptFont aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="7a878-116">To get a reference to the ComplexScriptFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7a878-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="7a878-117">Section index:</span></span>  <br/> |<span data-ttu-id="7a878-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="7a878-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="7a878-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="7a878-119">Row index:</span></span>  <br/> |<span data-ttu-id="7a878-120">**VisRowCharacter** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7a878-120">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="7a878-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="7a878-121">Cell index:</span></span>  <br/> |<span data-ttu-id="7a878-122">**visCharacterComplexScriptFont**</span><span class="sxs-lookup"><span data-stu-id="7a878-122">**visCharacterComplexScriptFont**</span></span> <br/> |
   

