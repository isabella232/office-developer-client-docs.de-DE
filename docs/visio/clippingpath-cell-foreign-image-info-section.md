---
title: ClippingPath Cell (Foreign Image Info Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Enthält einen Verweis auf die Geometrie des Pfads, der ein Bild durch begrenzt wird.
ms.openlocfilehash: 9f1c159e303c1d7bc3467c36756a422a3f325c7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796631"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a><span data-ttu-id="582d0-103">ClippingPath Cell (Foreign Image Info Section)</span><span class="sxs-lookup"><span data-stu-id="582d0-103">ClippingPath Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="582d0-104">Enthält einen Verweis auf die Geometrie des Pfads, der ein Bild durch begrenzt wird.</span><span class="sxs-lookup"><span data-stu-id="582d0-104">Contains a reference to the geometry of the path that an image is bounded by.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="582d0-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="582d0-105">Remarks</span></span>

<span data-ttu-id="582d0-106">Wenn die Zelle **ClippingPath** auf einen gültigen Pfad verweist, wird das Bild abgeschnitten, damit das Bild in den Pfad gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="582d0-106">If the **ClippingPath** cell points to a valid path, the image is clipped so that the image is rendered inside of the path.</span></span> <span data-ttu-id="582d0-107">Wenn die Zelle **ClippingPath** leer ist oder einen ungültigen Eintrag enthält, wird das Bild mit einem rechteckigen Clip unter Verwendung der Skalierung und Offset-Werte gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="582d0-107">If the **ClippingPath** cell is empty or contains an invalid entry, then the image will be rendered with a rectangular clip, using the scale and offset values.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="582d0-108">Nur von einem Abschnitt [Geometry](geometry-section.md) des Bilds ShapeSheet definierten Pfade sind gültige Einträge für die Zelle **ClippingPath** .</span><span class="sxs-lookup"><span data-stu-id="582d0-108">Only paths defined by a [Geometry](geometry-section.md) section in the image's ShapeSheet are valid entries for the **ClippingPath** cell.</span></span> <span data-ttu-id="582d0-109">Cross-Tabellenbezüge können nicht verwendet werden, um ein Bild Clipping Pfad zu definieren.</span><span class="sxs-lookup"><span data-stu-id="582d0-109">Cross-sheet references cannot be used to define an image clipping path.</span></span> 
  
<span data-ttu-id="582d0-110">Wenn Sie einen Verweis auf die Zelle **ClippingPath** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="582d0-110">To get a reference to the **ClippingPath** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="582d0-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="582d0-111">Cell name:</span></span>  <br/> | <span data-ttu-id="582d0-112">ClippingPath</span><span class="sxs-lookup"><span data-stu-id="582d0-112">ClippingPath</span></span>  <br/> |
   
<span data-ttu-id="582d0-113">Wenn Sie einen Verweis auf die Zelle **ClippingPath** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="582d0-113">To get a reference to the **ClippingPath** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="582d0-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="582d0-114">Section index:</span></span>  <br/> |<span data-ttu-id="582d0-115">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="582d0-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="582d0-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="582d0-116">Row index:</span></span>  <br/> |<span data-ttu-id="582d0-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="582d0-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="582d0-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="582d0-118">Cell index:</span></span>  <br/> |<span data-ttu-id="582d0-119">**visFrgnImgClippingPath**</span><span class="sxs-lookup"><span data-stu-id="582d0-119">**visFrgnImgClippingPath**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="582d0-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="582d0-120">Example</span></span>

<span data-ttu-id="582d0-121">Sie können die umgebende Form eines Bilds in ein Oval ändern, die folgenden Schritte durch:</span><span class="sxs-lookup"><span data-stu-id="582d0-121">You can change the bounding shape of an image to an oval by doing the following:</span></span>
  
- <span data-ttu-id="582d0-122">Fügen Sie das Bild auf Zeichenbereich.</span><span class="sxs-lookup"><span data-stu-id="582d0-122">Insert the picture onto the drawing canvas.</span></span>
    
- <span data-ttu-id="582d0-123">Maustaste auf das Bild, und wählen Sie dann auf **ShapeSheet anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="582d0-123">Right-click the picture and then select **Show ShapeSheet**.</span></span>
    
- <span data-ttu-id="582d0-124">Mit der rechten Sie Maustaste in das ShapeSheet, und wählen Sie **Im Abschnitt einfügen**.</span><span class="sxs-lookup"><span data-stu-id="582d0-124">Right-click anywhere in the ShapeSheet and select **Insert Section**.</span></span>
    
- <span data-ttu-id="582d0-125">Klicken Sie im Dialogfeld **Abschnitt einfügen** wählen Sie **Geometrie aus** , und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="582d0-125">In the **Insert Section** dialog box, select **Geometry** and then click **OK**.</span></span>
    
- <span data-ttu-id="582d0-126">Löschen Sie alle Zeilen in der neuen Geometrie-Abschnitt (z. B. "Geometry2").</span><span class="sxs-lookup"><span data-stu-id="582d0-126">In the new Geometry section (e.g. "Geometry2"), delete all but one row.</span></span>
    
- <span data-ttu-id="582d0-127">Mit der rechten Maustaste der verbleibenden Zeile, und klicken Sie dann auf **Zeilentyp ändern**.</span><span class="sxs-lookup"><span data-stu-id="582d0-127">Right-click the remaining row and then click **Change Row Type**.</span></span>
    
- <span data-ttu-id="582d0-128">Klicken Sie im Dialogfeld **Zeilentyp ändern** wählen **Ellipse** aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="582d0-128">In the **Change Row Type** dialog box, select **Ellipse** and then click **OK**.</span></span>
    
- <span data-ttu-id="582d0-129">Legen Sie im Abschnitt **Foreign Image** , die Formel für die Zelle **ClippingPath** `="Geometry2.Path"` und akzeptieren Sie die Formel.</span><span class="sxs-lookup"><span data-stu-id="582d0-129">In the **Foreign Image** section, set the formula for the **ClippingPath** cell to  `="Geometry2.Path"` and then accept the formula.</span></span> 
    

