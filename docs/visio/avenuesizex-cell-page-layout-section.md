---
title: Zelle "AvenueSizeX" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm65
localization_priority: Normal
ms.assetid: 86fe25ed-590d-b2f0-5dfe-9746a19c6b04
description: Bestimmt den horizontalen Abstand zwischen Shapes auf dem Zeichenblatt, wenn Sie Shapes mithilfe des Dialogfelds Layout konfigurieren (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout, klicken Sie auf der Seite Re-Layout, und klicken Sie dann auf Weitere Layoutoptionen).
ms.openlocfilehash: efb29181414957063e038b97c2d7b79720aa0405
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796429"
---
# <a name="avenuesizex-cell-page-layout-section"></a><span data-ttu-id="440e9-103">AvenueSizeX Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="440e9-103">AvenueSizeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="440e9-104">Bestimmt den horizontalen Abstand zwischen Shapes auf dem Zeichenblatt, wenn Sie Shapes mithilfe des Dialogfelds **Layout konfigurieren** (auf der Registerkarte **Entwurf** in der Gruppe **Layout** , klicken Sie auf **Der Seite Re-Layout**, und klicken Sie dann auf ** mehr Layoutoptionen **).</span><span class="sxs-lookup"><span data-stu-id="440e9-104">Determines the amount of horizontal space between shapes on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click ** More Layout Options **).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="440e9-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="440e9-105">Remarks</span></span>

<span data-ttu-id="440e9-106">Sie können diesen Wert auch im Dialogfeld **Abstände für Layout und Routing** festlegen. (Klicken Sie dazu auf der Registerkarte **Entwurf** in der Gruppe **Seite einrichten** auf den Pfeil, wählen Sie die Registerkarte **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.)</span><span class="sxs-lookup"><span data-stu-id="440e9-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="440e9-p101">Das dynamische Gitter verwendet die in der Zelle AvenueSizeX vorgenommene Einstellung, wenn nur ein Shape für die Berechnung des horizontalen Abstands verfügbar ist. Wenn Sie das dynamische Gitter verwenden möchten, aktivieren Sie auf der Registerkarte Ansicht in der Gruppe Visuelle Unterstützung das Kontrollkästchen Dynamisches Gitter.</span><span class="sxs-lookup"><span data-stu-id="440e9-p101">The dynamic grid uses the setting in the AvenueSizeX cell when only one shape is available for calculating horizontal spacing. To use the dynamic grid, on the **View** tab, in the **Visual Aids** group, select **Dynamic Grid**.</span></span>
  
<span data-ttu-id="440e9-109">Wenn Sie einen Verweis auf die Zelle AvenueSizeX aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="440e9-109">To get a reference to the AvenueSizeX cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="440e9-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="440e9-110">Cell name:</span></span>  <br/> | <span data-ttu-id="440e9-111">AvenueSizeY</span><span class="sxs-lookup"><span data-stu-id="440e9-111">AvenueSizeY</span></span>  <br/> |
   
<span data-ttu-id="440e9-112">Wenn Sie einen Verweis auf die Zelle AvenueSizeX aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="440e9-112">To get a reference to the AvenueSizeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="440e9-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="440e9-113">Section index:</span></span>  <br/> |<span data-ttu-id="440e9-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="440e9-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="440e9-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="440e9-115">Row index:</span></span>  <br/> |<span data-ttu-id="440e9-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="440e9-116">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="440e9-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="440e9-117">Cell index:</span></span>  <br/> |<span data-ttu-id="440e9-118">**visPLOAvenueSizeX**</span><span class="sxs-lookup"><span data-stu-id="440e9-118">**visPLOAvenueSizeX**</span></span> <br/> |
   

