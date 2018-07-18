---
title: Zelle "PageHeight" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm760
localization_priority: Normal
ms.assetid: 0184814c-2d67-6ad4-e336-5694612e518d
description: Enthält die Höhe der gedruckten Seite in Zeichnungseinheiten.
ms.openlocfilehash: e198e90e9c70aad1e41ee02d5dcefea68846486c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797578"
---
# <a name="pageheight-cell-page-properties-section"></a><span data-ttu-id="4a55f-103">PageHeight Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="4a55f-103">PageHeight Cell (Page Properties Section)</span></span>

<span data-ttu-id="4a55f-104">Enthält die Höhe der gedruckten Seite in Zeichnungseinheiten.</span><span class="sxs-lookup"><span data-stu-id="4a55f-104">Contains the height of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4a55f-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a55f-105">Remarks</span></span>

<span data-ttu-id="4a55f-106">Sie können die Seitenhöhe auch auf der Registerkarte **Zeichenblattgröße** im Dialogfeld **Seite einrichten** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**) oder die Seitengröße manuell mit der Maus ändern.</span><span class="sxs-lookup"><span data-stu-id="4a55f-106">You can also set the page height on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow), or by manually resizing the page with the mouse.</span></span> 
  
<span data-ttu-id="4a55f-107">Wenn Sie einen Verweis auf die Zelle PageHeight aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4a55f-107">To get a reference to the PageHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a55f-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="4a55f-108">Cell name:</span></span>  <br/> |<span data-ttu-id="4a55f-109">PageHeight</span><span class="sxs-lookup"><span data-stu-id="4a55f-109">PageHeight</span></span>  <br/> |
   
<span data-ttu-id="4a55f-110">Wenn Sie einen Verweis auf die Zelle PageHeight aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="4a55f-110">To get a reference to the PageHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a55f-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="4a55f-111">Section index:</span></span>  <br/> |<span data-ttu-id="4a55f-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4a55f-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4a55f-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="4a55f-113">Row index:</span></span>  <br/> |<span data-ttu-id="4a55f-114">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="4a55f-114">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="4a55f-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="4a55f-115">Cell index:</span></span>  <br/> |<span data-ttu-id="4a55f-116">**visPageHeight**</span><span class="sxs-lookup"><span data-stu-id="4a55f-116">**visPageHeight**</span></span> <br/> |
   

