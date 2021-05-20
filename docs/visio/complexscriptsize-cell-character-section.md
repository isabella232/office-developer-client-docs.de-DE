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
ms.openlocfilehash: 38b01c4a0142c7eca2923ee9b13963eaa1a62830
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428438"
---
# <a name="complexscriptsize-cell-character-section"></a><span data-ttu-id="3dade-103">Zelle "ComplexScriptSize" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="3dade-103">ComplexScriptSize Cell (Character Section)</span></span>

<span data-ttu-id="3dade-104">Der Schriftgrad zum Formatieren von Text mit komplexen Schriftzeichen.</span><span class="sxs-lookup"><span data-stu-id="3dade-104">The size of the font used to format text composed of complex script characters.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3dade-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3dade-105">Remarks</span></span>

<span data-ttu-id="3dade-106">Komplexe Schriftgrößen für Skripts werden auf der Registerkarte **Schriftart** im  Dialogfeld **Text** aufgeführt (klicken Sie auf der Registerkarte **Start** auf den Pfeil in der Gruppe Schriftart).</span><span class="sxs-lookup"><span data-stu-id="3dade-106">Complex script font sizes are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="3dade-107">Diese Liste wird nur angezeigt, wenn Sie eine Sprache mit  asiatischen oder komplexen Skriptzeichen im Dialogfeld Spracheinstellungen Microsoft Office hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="3dade-107">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="3dade-108">(Klicken **Sie auf Start,** **klicken** Sie auf Alle Programme, **Microsoft Office**, klicken Sie **Microsoft Office Tools,** und klicken Sie **dann auf Microsoft Office Spracheinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="3dade-108">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="3dade-p102">Sie können diesen Wert als explizite Größe in Punkt oder als Prozentsatz angeben. Wenn Sie einen Prozentsatz angeben, basiert der Wert auf dem Wert in der Zelle Größe. Der Standardwert von 0 (Null) bedeutet 100 %.</span><span class="sxs-lookup"><span data-stu-id="3dade-p102">You can enter this value as an explicit point size or as a percentage. If you specify a percentage, the value is based on the value in the Size cell. A default value of 0 (zero) means 100%.</span></span> 
  
<span data-ttu-id="3dade-112">Verwenden Sie zum Erhalten eines Verweises auf die Zelle ComplexScriptSize anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="3dade-112">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3dade-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="3dade-113">Cell name:</span></span>  <br/> |<span data-ttu-id="3dade-114">Char.ComplexScriptSize[ *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="3dade-114">Char.ComplexScriptSize[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="3dade-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ComplexScriptSize-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="3dade-115">To get a reference to the ComplexScriptSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3dade-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="3dade-116">Section index:</span></span>  <br/> |<span data-ttu-id="3dade-117">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="3dade-117">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="3dade-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="3dade-118">Row index:</span></span>  <br/> |<span data-ttu-id="3dade-119">**visRowCharacter**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3dade-119">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="3dade-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="3dade-120">Cell index:</span></span>  <br/> |<span data-ttu-id="3dade-121">**visCharacterComplexScriptSize**</span><span class="sxs-lookup"><span data-stu-id="3dade-121">**visCharacterComplexScriptSize**</span></span> <br/> |
   

