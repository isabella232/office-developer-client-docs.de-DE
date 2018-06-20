---
title: Zelle "AsianFont" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033764
localization_priority: Normal
ms.assetid: 45bfaaaa-52cc-f8b4-68e7-8b99e5788ce1
description: Enthält die Nummer der Schriftart, die zum Formatieren des Texts mit asiatischen Zeichen verwendet wird. Nummern von Schriftarten variieren entsprechend den im System installierten Schriftarten.
ms.openlocfilehash: 1fbaa0b27a0c639519c302129142dcefe5708115
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796401"
---
# <a name="asianfont-cell-character-section"></a><span data-ttu-id="32935-104">AsianFont Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="32935-104">AsianFont Cell (Character Section)</span></span>

<span data-ttu-id="32935-p102">Enthält die Nummer der Schriftart, die zum Formatieren des Texts mit asiatischen Zeichen verwendet wird. Nummern von Schriftarten variieren entsprechend den im System installierten Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="32935-p102">Contains the number of the font used to format the text containing Asian characters. Font numbers vary according to the fonts installed on your system.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="32935-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32935-107">Remarks</span></span>

<span data-ttu-id="32935-108">Asiatische Schriftarten sind auf der Registerkarte **Schriftart** im Dialogfeld **Text** verwenden (klicken Sie auf der Pfeil in der **Schriftart** auf der Registerkarte **Start** gruppieren) aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="32935-108">Asian fonts are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="32935-109">Diese Liste wird nur dann, wenn Sie eine Sprache hinzugefügt haben, die asiatische Sprachen oder komplexe Schriftzeichen, klicken Sie im Dialogfeld **Microsoft Office-Spracheinstellungen** enthält.</span><span class="sxs-lookup"><span data-stu-id="32935-109">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="32935-110">(Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft Office**, klicken Sie auf **Microsoft Office Tools**, und klicken Sie dann auf **Microsoft Office-Spracheinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="32935-110">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="32935-p104">Die Nummer 0 bedeutet, dass keine Schriftart festgelegt ist. Die Schriftart Latein oder Standardschriftarten werden verwendet, wenn sie die erforderlichen Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="32935-p104">The number 0 means no font is specified. The Latin font or default fonts are used if they contain the necessary characters.</span></span>
  
<span data-ttu-id="32935-113">Zum Abrufen eines Verweises auf die Zelle AsianFont nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="32935-113">To get a reference to the AsianFont cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="32935-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="32935-114">Cell name:</span></span>  <br/> |<span data-ttu-id="32935-115">Char.AsianFont [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="32935-115">Char.AsianFont[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="32935-116">Wenn Sie einen Verweis auf die Zelle AsianFont aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="32935-116">To get a reference to the AsianFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="32935-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="32935-117">Section index:</span></span>  <br/> |<span data-ttu-id="32935-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="32935-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="32935-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="32935-119">Row index:</span></span>  <br/> |<span data-ttu-id="32935-120">**VisRowCharacter** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="32935-120">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="32935-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="32935-121">Cell index:</span></span>  <br/> |<span data-ttu-id="32935-122">**visCharacterAsianFont**</span><span class="sxs-lookup"><span data-stu-id="32935-122">**visCharacterAsianFont**</span></span> <br/> |
   

