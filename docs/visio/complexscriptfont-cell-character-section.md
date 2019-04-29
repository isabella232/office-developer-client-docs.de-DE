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
# <a name="complexscriptfont-cell-character-section"></a><span data-ttu-id="7d5e8-104">Zelle "ComplexScriptFont" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="7d5e8-104">ComplexScriptFont Cell (Character Section)</span></span>

<span data-ttu-id="7d5e8-p102">Enthält die Nummer der Schriftart, die zum Formatieren von Text mit komplexen Schriftzeichen verwendet wird. Nummern von Schriftarten variieren entsprechend den im System installierten Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="7d5e8-p102">Contains the number of the font used to format text composed of complex script characters. Font numbers vary according to the fonts installed on your system.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7d5e8-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d5e8-107">Remarks</span></span>

<span data-ttu-id="7d5e8-108">Schriftgrößen für komplexe Schriftarten werden im Dialogfeld **Text** auf der Registerkarte **Schriftart** angezeigt (Klicken Sie auf der Registerkarte **Start** in der Gruppe **Schriftart** auf den Pfeil).</span><span class="sxs-lookup"><span data-stu-id="7d5e8-108">Complex script font sizes are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="7d5e8-109">Diese Liste wird nur angezeigt, wenn Sie im Dialogfeld **Microsoft Office-Spracheinstellungen** eine Sprache hinzugefügt haben, die asiatische oder komplexe Schriftzeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="7d5e8-109">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="7d5e8-110">(Klicken Sie auf **Start**, **Alle Programme**, **Microsoft Office**, Microsoft Office- **Tools**und dann auf **Microsoft Office-Spracheinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="7d5e8-110">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="7d5e8-111">Die Nummer Null (0) bedeutet, dass keine Schriftart festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7d5e8-111">The number 0 (zero) means no font is specified.</span></span> <span data-ttu-id="7d5e8-112">Die Schriftart Latein oder die Standardschriftarten werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d5e8-112">The Latin font or default fonts are used.</span></span>
  
<span data-ttu-id="7d5e8-113">Wenn Sie einen Verweis auf die Zelle Zelle ComplexScriptSize aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7d5e8-113">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7d5e8-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="7d5e8-114">Cell name:</span></span>  <br/> |<span data-ttu-id="7d5e8-115">Char. "ComplexScriptFont [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="7d5e8-115">Char.ComplexScriptFont[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7d5e8-116">Wenn Sie einen Verweis auf die Zelle "ComplexScriptFont aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="7d5e8-116">To get a reference to the ComplexScriptFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7d5e8-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="7d5e8-117">Section index:</span></span>  <br/> |<span data-ttu-id="7d5e8-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="7d5e8-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="7d5e8-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="7d5e8-119">Row index:</span></span>  <br/> |<span data-ttu-id="7d5e8-120">**visRowCharacter** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7d5e8-120">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="7d5e8-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="7d5e8-121">Cell index:</span></span>  <br/> |<span data-ttu-id="7d5e8-122">**visCharacterComplexScriptFont**</span><span class="sxs-lookup"><span data-stu-id="7d5e8-122">**visCharacterComplexScriptFont**</span></span> <br/> |
   

