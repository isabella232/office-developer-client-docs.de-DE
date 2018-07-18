---
title: Zelle "ComplexScriptSize" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033768
localization_priority: Normal
ms.assetid: f58687d7-2ba4-ff77-0bcc-3106867d89de
description: Der Schriftgrad zum Formatieren von Text mit komplexen Schriftzeichen.
ms.openlocfilehash: 4867ab57fa59b3a5e76598108fbb92b9bbab7913
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796685"
---
# <a name="complexscriptsize-cell-character-section"></a><span data-ttu-id="07296-103">ComplexScriptSize Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="07296-103">ComplexScriptSize Cell (Character Section)</span></span>

<span data-ttu-id="07296-104">Der Schriftgrad zum Formatieren von Text mit komplexen Schriftzeichen.</span><span class="sxs-lookup"><span data-stu-id="07296-104">The size of the font used to format text composed of complex script characters.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="07296-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07296-105">Remarks</span></span>

<span data-ttu-id="07296-106">Komplexe Schriftzeichen Schriftgrade sind aufgelistet, auf der Registerkarte **Schriftart** im Dialogfeld **Text** verwenden (klicken Sie auf der Pfeil in der **Schriftart** auf der Registerkarte **Start** gruppieren).</span><span class="sxs-lookup"><span data-stu-id="07296-106">Complex script font sizes are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="07296-107">Diese Liste wird nur dann, wenn Sie eine Sprache hinzugefügt haben, die asiatische Sprachen oder komplexe Schriftzeichen, klicken Sie im Dialogfeld **Microsoft Office-Spracheinstellungen** enthält.</span><span class="sxs-lookup"><span data-stu-id="07296-107">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="07296-108">(Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft Office**, klicken Sie auf **Microsoft Office Tools**, und klicken Sie dann auf **Microsoft Office-Spracheinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="07296-108">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="07296-p102">Sie können diesen Wert als explizite Größe in Punkt oder als Prozentsatz angeben. Wenn Sie einen Prozentsatz angeben, basiert der Wert auf dem Wert in der Zelle Größe. Der Standardwert von 0 (Null) bedeutet 100 %.</span><span class="sxs-lookup"><span data-stu-id="07296-p102">You can enter this value as an explicit point size or as a percentage. If you specify a percentage, the value is based on the value in the Size cell. A default value of 0 (zero) means 100%.</span></span> 
  
<span data-ttu-id="07296-112">Wenn Sie einen Verweis auf die Zelle ComplexScriptSize aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="07296-112">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07296-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="07296-113">Cell name:</span></span>  <br/> |<span data-ttu-id="07296-114">Char.ComplexScriptSize [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="07296-114">Char.ComplexScriptSize[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="07296-115">Wenn Sie einen Verweis auf die Zelle ComplexScriptSize aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="07296-115">To get a reference to the ComplexScriptSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07296-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="07296-116">Section index:</span></span>  <br/> |<span data-ttu-id="07296-117">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="07296-117">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="07296-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="07296-118">Row index:</span></span>  <br/> |<span data-ttu-id="07296-119">**VisRowCharacter** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="07296-119">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="07296-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="07296-120">Cell index:</span></span>  <br/> |<span data-ttu-id="07296-121">**visCharacterComplexScriptSize**</span><span class="sxs-lookup"><span data-stu-id="07296-121">**visCharacterComplexScriptSize**</span></span> <br/> |
   

