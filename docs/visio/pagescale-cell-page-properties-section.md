---
title: Zelle "PageScale" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm775
localization_priority: Normal
ms.assetid: e1da84b3-fd15-12b9-9342-0412e818b3b9
description: Bestimmt den Wert der Seiteneinheit im aktuellen Zeichnungsmaßstab. Der Zeichnungsmaßstab für die Seite ist das Verhältnis der in der Zelle PageScale angezeigten Seiteneinheit zur in der Zelle DrawingScale angezeigten Zeichnungseinheit.
ms.openlocfilehash: 0763fd6fad5f64bc741cbdd1e1227b0982323841
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339452"
---
# <a name="pagescale-cell-page-properties-section"></a><span data-ttu-id="02e7f-104">Zelle "PageScale" (Abschnitt "Page Properties")</span><span class="sxs-lookup"><span data-stu-id="02e7f-104">PageScale Cell (Page Properties Section)</span></span>

<span data-ttu-id="02e7f-p102">Bestimmt den Wert der Seiteneinheit im aktuellen Zeichnungsmaßstab. Der Zeichnungsmaßstab für die Seite ist das Verhältnis der in der Zelle PageScale angezeigten Seiteneinheit zur in der Zelle DrawingScale angezeigten Zeichnungseinheit.</span><span class="sxs-lookup"><span data-stu-id="02e7f-p102">Determines the value of the page unit in the current drawing scale. The drawing scale for the page is the ratio of the page unit shown in the PageScale cell to the drawing unit shown in the DrawingScale cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="02e7f-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02e7f-107">Remarks</span></span>

<span data-ttu-id="02e7f-108">Sie können den Wert der Zelle PageScale auch auf der Registerkarte **Zeichnungs Skala** im Dialogfeld **Seite** einrichten festlegen (Klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil für die **Seite einrichten** ).</span><span class="sxs-lookup"><span data-stu-id="02e7f-108">You can also set the value of the PageScale cell on the **Drawing Scale** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="02e7f-109">Der Wert der Zelle ist die erste der beiden Zahlen im vordefinierten \*\*\*\* Feld Skalieren oder **Benutzerdefiniert** , je nachdem, welche Zeichnungs Skalierungseinstellung unter **Zeichnungsmaßstab**ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="02e7f-109">The value of the cell is the first of the two numbers in the **Pre-defined scale** box or **Custom scale** box, depending on the drawing scale setting selected under **Drawing scale**.</span></span> <span data-ttu-id="02e7f-110">Wenn Sie beispielsweise einen architektonischen Maßstab für Ihre Zeichnung auswählen, lautet der Zeichnungsmaßstab für die Seite 3/32 "= 1 ' 0".</span><span class="sxs-lookup"><span data-stu-id="02e7f-110">For example, if you select an architectural scale for your drawing, the drawing scale for the page is 3/32" = 1'0".</span></span> <span data-ttu-id="02e7f-111">Der Wert in der Zelle PageScale ist 0,0938.</span><span class="sxs-lookup"><span data-stu-id="02e7f-111">The value in the PageScale cell is 0.0938 in.</span></span> <span data-ttu-id="02e7f-112">(oder 3/32 ") und der Wert in der Zelle DrawingScale ist 1 ft.</span><span class="sxs-lookup"><span data-stu-id="02e7f-112">(or 3/32") and the value in the DrawingScale cell is 1 ft.</span></span>
  
<span data-ttu-id="02e7f-113">Wenn Sie einen Verweis auf die Zelle PageScale aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="02e7f-113">To get a reference to the PageScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02e7f-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="02e7f-114">Cell name:</span></span>  <br/> |<span data-ttu-id="02e7f-115">PageScale</span><span class="sxs-lookup"><span data-stu-id="02e7f-115">PageScale</span></span>  <br/> |
   
<span data-ttu-id="02e7f-116">Wenn Sie einen Verweis auf die Zelle PageScale aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="02e7f-116">To get a reference to the PageScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02e7f-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="02e7f-117">Section index:</span></span>  <br/> |<span data-ttu-id="02e7f-118">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="02e7f-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="02e7f-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="02e7f-119">Row index:</span></span>  <br/> |<span data-ttu-id="02e7f-120">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="02e7f-120">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="02e7f-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="02e7f-121">Cell index:</span></span>  <br/> |<span data-ttu-id="02e7f-122">**visPageScale**</span><span class="sxs-lookup"><span data-stu-id="02e7f-122">**visPageScale**</span></span> <br/> |
   

