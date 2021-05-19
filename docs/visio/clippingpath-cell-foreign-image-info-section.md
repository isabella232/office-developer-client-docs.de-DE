---
title: Zelle "ClippingPath" (Abschnitt "Foreign Image Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Enthält einen Verweis auf die Geometrie des Pfads, an den ein Bild gebunden ist.
ms.openlocfilehash: cfbbb3ca7294f751f088df7c3284bf6461270af7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425512"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a><span data-ttu-id="de553-103">Zelle "ClippingPath" (Abschnitt "Foreign Image Info")</span><span class="sxs-lookup"><span data-stu-id="de553-103">ClippingPath Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="de553-104">Enthält einen Verweis auf die Geometrie des Pfads, an den ein Bild gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="de553-104">Contains a reference to the geometry of the path that an image is bounded by.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="de553-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="de553-105">Remarks</span></span>

<span data-ttu-id="de553-106">Wenn die **Zelle ClippingPath** auf einen gültigen Pfad zeigt, wird das Bild abgeschnitten, sodass das Bild innerhalb des Pfads gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="de553-106">If the **ClippingPath** cell points to a valid path, the image is clipped so that the image is rendered inside of the path.</span></span> <span data-ttu-id="de553-107">Wenn die **Zelle ClippingPath** leer ist oder einen ungültigen Eintrag enthält, wird das Bild mithilfe der Skalierungs- und Offsetwerte mit einem rechteckigen Clip gerendert.</span><span class="sxs-lookup"><span data-stu-id="de553-107">If the **ClippingPath** cell is empty or contains an invalid entry, then the image will be rendered with a rectangular clip, using the scale and offset values.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="de553-108">Nur von einem [Geometry-Abschnitt](geometry-section.md) im ShapeSheet des Bilds definierte Pfade sind gültige Einträge für die **Zelle ClippingPath.**</span><span class="sxs-lookup"><span data-stu-id="de553-108">Only paths defined by a [Geometry](geometry-section.md) section in the image's ShapeSheet are valid entries for the **ClippingPath** cell.</span></span> <span data-ttu-id="de553-109">Querverweise können nicht zum Definieren eines Pfads für die Bildausschnitte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="de553-109">Cross-sheet references cannot be used to define an image clipping path.</span></span> 
  
<span data-ttu-id="de553-110">Verwenden Sie zum Erhalten eines Verweises auf die **Zelle ClippingPath** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="de553-110">To get a reference to the **ClippingPath** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="de553-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="de553-111">Cell name:</span></span>  <br/> | <span data-ttu-id="de553-112">ClippingPath</span><span class="sxs-lookup"><span data-stu-id="de553-112">ClippingPath</span></span>  <br/> |
   
<span data-ttu-id="de553-113">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle ClippingPath** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="de553-113">To get a reference to the **ClippingPath** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="de553-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="de553-114">Section index:</span></span>  <br/> |<span data-ttu-id="de553-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="de553-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="de553-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="de553-116">Row index:</span></span>  <br/> |<span data-ttu-id="de553-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="de553-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="de553-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="de553-118">Cell index:</span></span>  <br/> |<span data-ttu-id="de553-119">**visFrgnImgClippingPath**</span><span class="sxs-lookup"><span data-stu-id="de553-119">**visFrgnImgClippingPath**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="de553-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="de553-120">Example</span></span>

<span data-ttu-id="de553-121">Sie können die begrenzungsförmige Form eines Bilds in ein Oval ändern, indem Sie die folgenden Schritte tun:</span><span class="sxs-lookup"><span data-stu-id="de553-121">You can change the bounding shape of an image to an oval by doing the following:</span></span>
  
- <span data-ttu-id="de553-122">Fügen Sie das Bild in den Zeichenbereich ein.</span><span class="sxs-lookup"><span data-stu-id="de553-122">Insert the picture onto the drawing canvas.</span></span>
    
- <span data-ttu-id="de553-123">Klicken Sie mit der rechten Maustaste auf das Bild, und wählen Sie **dann ShapeSheet anzeigen aus.**</span><span class="sxs-lookup"><span data-stu-id="de553-123">Right-click the picture and then select **Show ShapeSheet**.</span></span>
    
- <span data-ttu-id="de553-124">Klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im ShapeSheet, und wählen **Sie Abschnitt einfügen aus.**</span><span class="sxs-lookup"><span data-stu-id="de553-124">Right-click anywhere in the ShapeSheet and select **Insert Section**.</span></span>
    
- <span data-ttu-id="de553-125">Wählen Sie **im Dialogfeld Abschnitt** einfügen die Option **Geometrie** aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="de553-125">In the **Insert Section** dialog box, select **Geometry** and then click **OK**.</span></span>
    
- <span data-ttu-id="de553-126">Löschen Sie im neuen Abschnitt Geometry (z. B. "Geometry2") bis auf eine Zeile.</span><span class="sxs-lookup"><span data-stu-id="de553-126">In the new Geometry section (e.g. "Geometry2"), delete all but one row.</span></span>
    
- <span data-ttu-id="de553-127">Klicken Sie mit der rechten Maustaste auf die verbleibende Zeile, und klicken Sie dann **auf Zeilentyp ändern.**</span><span class="sxs-lookup"><span data-stu-id="de553-127">Right-click the remaining row and then click **Change Row Type**.</span></span>
    
- <span data-ttu-id="de553-128">Wählen Sie im Dialogfeld **Zeilentyp** ändern die Option **Ellipse** aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="de553-128">In the **Change Row Type** dialog box, select **Ellipse** and then click **OK**.</span></span>
    
- <span data-ttu-id="de553-129">Legen Sie **im Abschnitt** Fremdes Bild die Formel für die **Zelle ClippingPath** auf und  `="Geometry2.Path"` akzeptieren Sie die Formel.</span><span class="sxs-lookup"><span data-stu-id="de553-129">In the **Foreign Image** section, set the formula for the **ClippingPath** cell to  `="Geometry2.Path"` and then accept the formula.</span></span> 
    

