---
title: Zelle "PageWidth" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251372
localization_priority: Normal
ms.assetid: b98c5bf3-10c8-7299-2836-3906d6a9135d
description: Legt die Breite der gedruckten Seite in Zeichnungseinheiten fest.
ms.openlocfilehash: 6d887cb4335d2725101db54ba2b1483ccf01cff4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434270"
---
# <a name="pagewidth-cell-page-properties-section"></a><span data-ttu-id="8e629-103">Zelle "PageWidth" (Abschnitt "Page Properties")</span><span class="sxs-lookup"><span data-stu-id="8e629-103">PageWidth Cell (Page Properties Section)</span></span>

<span data-ttu-id="8e629-104">Legt die Breite der gedruckten Seite in Zeichnungseinheiten fest.</span><span class="sxs-lookup"><span data-stu-id="8e629-104">Determines the width of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8e629-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8e629-105">Remarks</span></span>

<span data-ttu-id="8e629-106">Sie können die Seitenbreite  auch auf der  Registerkarte Seitengröße des Dialogfelds Seiteneinrichtung festlegen (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil Seite **einrichten)** oder indem Sie die Größe der Seite mit der Maus manuell ändern.</span><span class="sxs-lookup"><span data-stu-id="8e629-106">You can also set the page width on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) or by manually resizing the page with the mouse.</span></span> <span data-ttu-id="8e629-107">Ziehen Sie dazu bei gedrückter STRG-TASTE den Seitenrand mit der Maus.</span><span class="sxs-lookup"><span data-stu-id="8e629-107">To do this, drag the edge of the page while holding down the CTRL key.</span></span> 
  
<span data-ttu-id="8e629-108">Um einen Verweis auf die Zelle PageWidth anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="8e629-108">To get a reference to the PageWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e629-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="8e629-109">Cell name:</span></span>  <br/> |<span data-ttu-id="8e629-110">PageWidth</span><span class="sxs-lookup"><span data-stu-id="8e629-110">PageWidth</span></span>  <br/> |
   
<span data-ttu-id="8e629-111">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die PageWidth-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="8e629-111">To get a reference to the PageWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e629-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="8e629-112">Section index:</span></span>  <br/> |<span data-ttu-id="8e629-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8e629-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8e629-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="8e629-114">Row index:</span></span>  <br/> |<span data-ttu-id="8e629-115">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="8e629-115">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="8e629-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="8e629-116">Cell index:</span></span>  <br/> |<span data-ttu-id="8e629-117">**visPageWidth**</span><span class="sxs-lookup"><span data-stu-id="8e629-117">**visPageWidth**</span></span> <br/> |
   

