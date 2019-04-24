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
ms.openlocfilehash: 4af7e590a7bd0733ad622f3df259aa6c01837c4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341329"
---
# <a name="asianfont-cell-character-section"></a><span data-ttu-id="a22d4-104">Zelle "AsianFont" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="a22d4-104">AsianFont Cell (Character Section)</span></span>

<span data-ttu-id="a22d4-p102">Enthält die Nummer der Schriftart, die zum Formatieren des Texts mit asiatischen Zeichen verwendet wird. Nummern von Schriftarten variieren entsprechend den im System installierten Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="a22d4-p102">Contains the number of the font used to format the text containing Asian characters. Font numbers vary according to the fonts installed on your system.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a22d4-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a22d4-107">Remarks</span></span>

<span data-ttu-id="a22d4-p103">Asiatische Schriftarten sind im Dialogfeld **Text** auf der Registerkarte **Schriftart** aufgelistet. (Klicken Sie auf der Registerkarte **Start** in der Gruppe **Schriftart** auf den Pfeil.) Diese Liste wird nur dann angezeigt, wenn Sie im Dialogfeld **Microsoft Office-Spracheinstellungen** eine Sprache mit asiatischen Zeichen oder komplexen Schriftzeichen hinzugefügt haben. (Klicken Sie auf **Start**, auf **Alle Programme**, auf **Microsoft Office** und auf **Microsoft Office Tools**, und klicken Sie dann auf **Microsoft Office-Spracheinstellungen**.)</span><span class="sxs-lookup"><span data-stu-id="a22d4-p103">Asian fonts are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab). This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box. (Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="a22d4-p104">Die Nummer 0 bedeutet, dass keine Schriftart festgelegt ist. Die Schriftart Latein oder Standardschriftarten werden verwendet, wenn sie die erforderlichen Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="a22d4-p104">The number 0 means no font is specified. The Latin font or default fonts are used if they contain the necessary characters.</span></span>
  
<span data-ttu-id="a22d4-113">Wenn Sie einen Verweis auf die Zelle "AsianFont aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a22d4-113">To get a reference to the AsianFont cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a22d4-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a22d4-114">Cell name:</span></span>  <br/> |<span data-ttu-id="a22d4-115">Char. "AsianFont [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="a22d4-115">Char.AsianFont[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a22d4-116">Wenn Sie einen Verweis auf die Zelle "AsianFont aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a22d4-116">To get a reference to the AsianFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a22d4-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a22d4-117">Section index:</span></span>  <br/> |<span data-ttu-id="a22d4-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="a22d4-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="a22d4-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a22d4-119">Row index:</span></span>  <br/> |<span data-ttu-id="a22d4-120">**visRowCharacter** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a22d4-120">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="a22d4-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a22d4-121">Cell index:</span></span>  <br/> |<span data-ttu-id="a22d4-122">**visCharacterAsianFont**</span><span class="sxs-lookup"><span data-stu-id="a22d4-122">**visCharacterAsianFont**</span></span> <br/> |
   

