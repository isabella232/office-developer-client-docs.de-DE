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
ms.openlocfilehash: e03696c8f1c921c930d3563e9c73ef4ae613a7c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797602"
---
# <a name="pagewidth-cell-page-properties-section"></a><span data-ttu-id="6a6a2-103">PageWidth Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="6a6a2-103">PageWidth Cell (Page Properties Section)</span></span>

<span data-ttu-id="6a6a2-104">Legt die Breite der gedruckten Seite in Zeichnungseinheiten fest.</span><span class="sxs-lookup"><span data-stu-id="6a6a2-104">Determines the width of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6a6a2-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a6a2-105">Remarks</span></span>

<span data-ttu-id="6a6a2-106">Sie können auch die Breite der Seite auf der Registerkarte **Zeichenbl** im Dialogfeld **Seite einrichten** festlegen (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten** ) oder die Seite mit der Maus manuell ändern.</span><span class="sxs-lookup"><span data-stu-id="6a6a2-106">You can also set the page width on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) or by manually resizing the page with the mouse.</span></span> <span data-ttu-id="6a6a2-107">Ziehen Sie hierzu den Rand der Seite halten Sie die STRG-Taste.</span><span class="sxs-lookup"><span data-stu-id="6a6a2-107">To do this, drag the edge of the page while holding down the CTRL key.</span></span> 
  
<span data-ttu-id="6a6a2-108">Wenn Sie einen Verweis auf die Zelle PageWidth aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6a6a2-108">To get a reference to the PageWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a6a2-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6a6a2-109">Cell name:</span></span>  <br/> |<span data-ttu-id="6a6a2-110">PageWidth</span><span class="sxs-lookup"><span data-stu-id="6a6a2-110">PageWidth</span></span>  <br/> |
   
<span data-ttu-id="6a6a2-111">Wenn Sie einen Verweis auf die Zelle PageWidth aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="6a6a2-111">To get a reference to the PageWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a6a2-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6a6a2-112">Section index:</span></span>  <br/> |<span data-ttu-id="6a6a2-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6a6a2-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="6a6a2-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6a6a2-114">Row index:</span></span>  <br/> |<span data-ttu-id="6a6a2-115">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="6a6a2-115">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="6a6a2-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6a6a2-116">Cell index:</span></span>  <br/> |<span data-ttu-id="6a6a2-117">**visPageWidth**</span><span class="sxs-lookup"><span data-stu-id="6a6a2-117">**visPageWidth**</span></span> <br/> |
   

