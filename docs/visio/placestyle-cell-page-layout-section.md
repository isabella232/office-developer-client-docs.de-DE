---
title: Zelle "PlaceStyle" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dcd5a35-bd3d-447f-e4aa-986091d129de
description: Gibt an, wie Shapes auf dem Zeichenblatt platziert werden, wenn sie im Dialogfeld Layout konfigurieren (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Seite neu anordnen, und klicken Sie anschließend auf Weitere Layoutoptionen) angeordnet werden.
ms.openlocfilehash: 251bee427c732fe782c85c4991df07a1deb2a4dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797622"
---
# <a name="placestyle-cell-page-layout-section"></a><span data-ttu-id="241e0-103">PlaceStyle Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="241e0-103">PlaceStyle Cell (Page Layout Section)</span></span>

<span data-ttu-id="241e0-104">Gibt an, wie Shapes auf dem Zeichenblatt platziert werden, wenn sie im Dialogfeld **Layout konfigurieren** (klicken Sie auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Seite neu anordnen**, und klicken Sie anschließend auf **Weitere Layoutoptionen**) angeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="241e0-104">Determines how shapes are placed on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="241e0-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="241e0-105">Remarks</span></span>

<span data-ttu-id="241e0-106">Sie können den Wert dieser Zelle auch im Dialogfeld **Layout konfigurieren** festlegen.</span><span class="sxs-lookup"><span data-stu-id="241e0-106">You can also set the value of this cell in the **Configure Layout** dialog box.</span></span> 
  
<span data-ttu-id="241e0-107">Wenn Sie eine Referenz auf die Zelle PlaceStyle nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft erhalten möchten, verwenden Sie Folgendes.</span><span class="sxs-lookup"><span data-stu-id="241e0-107">To get a reference to the PlaceStyle cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="241e0-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="241e0-108">Cell name:</span></span>  <br/> |<span data-ttu-id="241e0-109">PlaceStyle</span><span class="sxs-lookup"><span data-stu-id="241e0-109">PlaceStyle</span></span>  <br/> |
   
<span data-ttu-id="241e0-110">Wenn Sie eine Referenz auf die Zelle PlaceStyle aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="241e0-110">To get a reference to the PlaceStyle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="241e0-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="241e0-111">Section index:</span></span>  <br/> |<span data-ttu-id="241e0-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="241e0-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="241e0-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="241e0-113">Row index:</span></span>  <br/> |<span data-ttu-id="241e0-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="241e0-114">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="241e0-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="241e0-115">Cell index:</span></span>  <br/> |<span data-ttu-id="241e0-116">**visPLOPlaceStyle**</span><span class="sxs-lookup"><span data-stu-id="241e0-116">**visPLOPlaceStyle**</span></span> <br/> |
   

