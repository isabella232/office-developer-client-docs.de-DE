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
ms.openlocfilehash: 654a93f939226bedab2e40ab591dad0e3f872267
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341811"
---
# <a name="lineweight-cell-line-format-section"></a><span data-ttu-id="5a46d-104">Zelle "LineWeight" (Abschnitt "Line Format")</span><span class="sxs-lookup"><span data-stu-id="5a46d-104">LineWeight Cell (Line Format Section)</span></span>

<span data-ttu-id="5a46d-105">Legt die Linienbreite eines Shapes fest.</span><span class="sxs-lookup"><span data-stu-id="5a46d-105">Determines the line weight of a shape.</span></span> <span data-ttu-id="5a46d-106">Definieren Sie die Linienbreite, indem Sie eine Zahl mit einer gültigen Maßeinheit eingeben.</span><span class="sxs-lookup"><span data-stu-id="5a46d-106">Set the line weight by entering a number with a valid unit of measure.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5a46d-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a46d-107">Remarks</span></span>

<span data-ttu-id="5a46d-108">Sie können den Wert von LineWeight auch im Dialogfeld **Linie** festlegen (Klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Linie**, zeigen Sie auf **Gewicht**, und klicken Sie dann auf **Weitere Linien**).</span><span class="sxs-lookup"><span data-stu-id="5a46d-108">You can also set the value of LineWeight in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="5a46d-109">Wenn die Maßeinheit nicht eingegeben wird, wird die im Dialogfeld **Visio-Optionen** angegebene Maßeinheit für Text verwendet (Klicken Sie auf die Registerkarte **Datei** , und klicken Sie dann auf **Optionen**).</span><span class="sxs-lookup"><span data-stu-id="5a46d-109">If the unit of measure is not entered, the unit of measure for text specified in the **Visio Options** dialog box is used (click the **File** tab, and then click **Options**).</span></span> <span data-ttu-id="5a46d-110">Die Linienbreite ist unabhängig vom Zeichnungsmaßstab.</span><span class="sxs-lookup"><span data-stu-id="5a46d-110">Line weight is independent of the scale of the drawing.</span></span> <span data-ttu-id="5a46d-111">Wenn die Zeichnung maßstäblich ist, bleibt die Linienbreite unverändert.</span><span class="sxs-lookup"><span data-stu-id="5a46d-111">If the drawing is scaled, the line weight remains the same.</span></span> 
  
<span data-ttu-id="5a46d-112">Wenn Sie einen Verweis auf die Zelle LineWeight aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5a46d-112">To get a reference to the LineWeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5a46d-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5a46d-113">Cell name:</span></span>  <br/> | <span data-ttu-id="5a46d-114">LineWeight</span><span class="sxs-lookup"><span data-stu-id="5a46d-114">LineWeight</span></span>  <br/> |
   
<span data-ttu-id="5a46d-115">Wenn Sie einen Verweis auf die Zelle LineWeight aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="5a46d-115">To get a reference to the LineWeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5a46d-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5a46d-116">Section index:</span></span>  <br/> |<span data-ttu-id="5a46d-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5a46d-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5a46d-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5a46d-118">Row index:</span></span>  <br/> |<span data-ttu-id="5a46d-119">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="5a46d-119">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="5a46d-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5a46d-120">Cell index:</span></span>  <br/> |<span data-ttu-id="5a46d-121">**visLineWeight**</span><span class="sxs-lookup"><span data-stu-id="5a46d-121">**visLineWeight**</span></span> <br/> |
   

