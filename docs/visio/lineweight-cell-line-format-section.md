---
title: Zelle "LineWeight" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm585
localization_priority: Normal
ms.assetid: 16b0e293-eeef-34b4-aeb0-4472815dd543
description: Legt die Linienbreite eines Shapes fest. Definieren Sie die Linienbreite, indem Sie eine Zahl mit einer gültigen Maßeinheit eingeben.
ms.openlocfilehash: a5207607d90ef6a79dcb3acc191521b73e2cdf54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797339"
---
# <a name="lineweight-cell-line-format-section"></a><span data-ttu-id="c619e-104">LineWeight Cell (Line Format Section)</span><span class="sxs-lookup"><span data-stu-id="c619e-104">LineWeight Cell (Line Format Section)</span></span>

<span data-ttu-id="c619e-p102">Legt die Linienbreite eines Shapes fest. Definieren Sie die Linienbreite, indem Sie eine Zahl mit einer gültigen Maßeinheit eingeben.</span><span class="sxs-lookup"><span data-stu-id="c619e-p102">Determines the line weight of a shape. Set the line weight by entering a number with a valid unit of measure.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c619e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c619e-107">Remarks</span></span>

<span data-ttu-id="c619e-108">Sie können den Wert der LineWeight auch im Dialogfeld **Linie** festlegen (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** klicken Sie auf **Zeile**, **Weight**, und klicken Sie dann auf **Weitere Linien**).</span><span class="sxs-lookup"><span data-stu-id="c619e-108">You can also set the value of LineWeight in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="c619e-109">Wenn die Einheit nicht eingegeben wird, wird die Maßeinheit für den Text im Dialogfeld **Visio-Optionen** (klicken Sie auf der Registerkarte **Datei** , und klicken Sie dann auf **Optionen**).</span><span class="sxs-lookup"><span data-stu-id="c619e-109">If the unit of measure is not entered, the unit of measure for text specified in the **Visio Options** dialog box is used (click the **File** tab, and then click **Options**).</span></span> <span data-ttu-id="c619e-110">Linienbreite ist unabhängig von der Skalierung der Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="c619e-110">Line weight is independent of the scale of the drawing.</span></span> <span data-ttu-id="c619e-111">Wenn die Zeichnung skaliert wird, bleibt die Linienstärke unverändert.</span><span class="sxs-lookup"><span data-stu-id="c619e-111">If the drawing is scaled, the line weight remains the same.</span></span> 
  
<span data-ttu-id="c619e-112">Wenn Sie einen Verweis auf die Zelle LineWeight nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c619e-112">To get a reference to the LineWeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c619e-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="c619e-113">Cell name:</span></span>  <br/> | <span data-ttu-id="c619e-114">LineWeight</span><span class="sxs-lookup"><span data-stu-id="c619e-114">LineWeight</span></span>  <br/> |
   
<span data-ttu-id="c619e-115">Wenn Sie einen Verweis auf die Zelle LineWeight aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="c619e-115">To get a reference to the LineWeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c619e-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="c619e-116">Section index:</span></span>  <br/> |<span data-ttu-id="c619e-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c619e-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c619e-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c619e-118">Row index:</span></span>  <br/> |<span data-ttu-id="c619e-119">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="c619e-119">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="c619e-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="c619e-120">Cell index:</span></span>  <br/> |<span data-ttu-id="c619e-121">**visLineWeight**</span><span class="sxs-lookup"><span data-stu-id="c619e-121">**visLineWeight**</span></span> <br/> |
   

