---
title: Zelle "PlaceStyle" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dcd5a35-bd3d-447f-e4aa-986091d129de
description: Bestimmt, wie Shapes auf der Seite platziert werden, wenn Sie Shapes durch werden über das Dialogfeld Layout konfigurieren (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout, klicken Sie auf der Seite Re-Layout, und klicken Sie dann auf Weitere Layoutoptionen).
ms.openlocfilehash: 251bee427c732fe782c85c4991df07a1deb2a4dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797622"
---
# <a name="placestyle-cell-page-layout-section"></a><span data-ttu-id="0b4cb-103">PlaceStyle Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="0b4cb-103">PlaceStyle Cell (Page Layout Section)</span></span>

<span data-ttu-id="0b4cb-104">Bestimmt, wie Shapes auf der Seite platziert werden, wenn Sie Shapes durch werden über das Dialogfeld **Layout konfigurieren** (klicken Sie auf der Registerkarte **Entwurf** in der Gruppe **Layout** , klicken Sie auf **Der Seite Re-Layout**, und klicken Sie dann auf **Weitere Layoutoptionen**).</span><span class="sxs-lookup"><span data-stu-id="0b4cb-104">Determines how shapes are placed on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0b4cb-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0b4cb-105">Remarks</span></span>

<span data-ttu-id="0b4cb-106">Sie können den Wert dieser Zelle auch im Dialogfeld **Layout konfigurieren** festlegen.</span><span class="sxs-lookup"><span data-stu-id="0b4cb-106">You can also set the value of this cell in the **Configure Layout** dialog box.</span></span> 
  
<span data-ttu-id="0b4cb-107">Zum Abrufen eines Verweises auf die Zelle PlaceStyle nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0b4cb-107">To get a reference to the PlaceStyle cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0b4cb-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="0b4cb-108">Cell name:</span></span>  <br/> |<span data-ttu-id="0b4cb-109">PlaceStyle</span><span class="sxs-lookup"><span data-stu-id="0b4cb-109">PlaceStyle</span></span>  <br/> |
   
<span data-ttu-id="0b4cb-110">Wenn Sie einen Verweis auf die Zelle PlaceStyle aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="0b4cb-110">To get a reference to the PlaceStyle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0b4cb-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="0b4cb-111">Section index:</span></span>  <br/> |<span data-ttu-id="0b4cb-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0b4cb-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0b4cb-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="0b4cb-113">Row index:</span></span>  <br/> |<span data-ttu-id="0b4cb-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="0b4cb-114">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="0b4cb-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="0b4cb-115">Cell index:</span></span>  <br/> |<span data-ttu-id="0b4cb-116">**visPLOPlaceStyle**</span><span class="sxs-lookup"><span data-stu-id="0b4cb-116">**visPLOPlaceStyle**</span></span> <br/> |
   

