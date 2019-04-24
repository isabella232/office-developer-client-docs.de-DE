---
title: Zelle "PlaceStyle" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dcd5a35-bd3d-447f-e4aa-986091d129de
description: Gibt an, wie Shapes auf dem Zeichenblatt platziert werden, wenn sie im Dialogfeld Layout konfigurieren (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Seite neu anordnen, und klicken Sie anschließend auf Weitere Layoutoptionen) angeordnet werden.
ms.openlocfilehash: b3159b765922d6656d12dd42a377322e4a91fc04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346865"
---
# <a name="placestyle-cell-page-layout-section"></a><span data-ttu-id="a9ab4-103">Zelle "PlaceStyle" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="a9ab4-103">PlaceStyle Cell (Page Layout Section)</span></span>

<span data-ttu-id="a9ab4-104">Gibt an, wie Shapes auf dem Zeichenblatt platziert werden, wenn sie im Dialogfeld **Layout konfigurieren** (klicken Sie auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Seite neu anordnen**, und klicken Sie anschließend auf **Weitere Layoutoptionen**) angeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="a9ab4-104">Determines how shapes are placed on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a9ab4-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9ab4-105">Remarks</span></span>

<span data-ttu-id="a9ab4-106">Sie können den Wert dieser Zelle auch im Dialogfeld **Layout konfigurieren** festlegen.</span><span class="sxs-lookup"><span data-stu-id="a9ab4-106">You can also set the value of this cell in the **Configure Layout** dialog box.</span></span> 
  
<span data-ttu-id="a9ab4-107">Wenn Sie einen Verweis auf die Zelle PlaceStyle aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a9ab4-107">To get a reference to the PlaceStyle cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a9ab4-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a9ab4-108">Cell name:</span></span>  <br/> |<span data-ttu-id="a9ab4-109">PlaceStyle</span><span class="sxs-lookup"><span data-stu-id="a9ab4-109">PlaceStyle</span></span>  <br/> |
   
<span data-ttu-id="a9ab4-110">Wenn Sie einen Verweis auf die Zelle PlaceStyle nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a9ab4-110">To get a reference to the PlaceStyle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a9ab4-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a9ab4-111">Section index:</span></span>  <br/> |<span data-ttu-id="a9ab4-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a9ab4-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a9ab4-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a9ab4-113">Row index:</span></span>  <br/> |<span data-ttu-id="a9ab4-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="a9ab4-114">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="a9ab4-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a9ab4-115">Cell index:</span></span>  <br/> |<span data-ttu-id="a9ab4-116">**visPLOPlaceStyle**</span><span class="sxs-lookup"><span data-stu-id="a9ab4-116">**visPLOPlaceStyle**</span></span> <br/> |
   

