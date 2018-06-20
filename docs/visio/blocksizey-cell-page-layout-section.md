---
title: Zelle "BlockSizeY" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm110
localization_priority: Normal
ms.assetid: be51e18e-ea49-0788-1a17-866090afb9f4
description: Bestimmt die vertikale Blockgröße, den Bereich in die jeweils auf dem Zeichenblatt passen müssen, wenn Sie Shapes mithilfe des Dialogfelds Layout konfigurieren (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout, klicken Sie auf der Seite Re-Layout, und klicken Sie dann auf Weitere Layoutoptionen).
ms.openlocfilehash: 283723bf902c07cfb044ab73107491df3c170a4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796536"
---
# <a name="blocksizey-cell-page-layout-section"></a><span data-ttu-id="800a1-103">Zelle "BlockSizeY" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="800a1-103">BlockSizeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="800a1-104">Bestimmt die vertikale Blockgröße, den Bereich in die jeweils auf dem Zeichenblatt passen müssen, wenn Sie Shapes mithilfe des Dialogfelds **Layout konfigurieren** (klicken Sie auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Re-Seitenlayout** und klicken Sie dann auf **Weitere Layoutoptionen**).</span><span class="sxs-lookup"><span data-stu-id="800a1-104">Determines the vertical block size, the area in which each of your shapes must fit on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="800a1-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="800a1-105">Remarks</span></span>

<span data-ttu-id="800a1-106">Sie können diesen Wert auch im Dialogfeld **Layout und Routing Abstand** festlegen (klicken Sie auf der Registerkarte **Entwurf** klicken Sie auf den Pfeil in der Gruppe **Seite einrichten** , klicken Sie auf der Registerkarte **Layout und Routing** und klicken Sie dann auf **Abstand**).</span><span class="sxs-lookup"><span data-stu-id="800a1-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="800a1-107">Zum Abrufen eines Verweises auf die Zelle BlockSizeY nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="800a1-107">To get a reference to the BlockSizeY cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="800a1-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="800a1-108">Cell name:</span></span>  <br/> | <span data-ttu-id="800a1-109">BlockSizeY</span><span class="sxs-lookup"><span data-stu-id="800a1-109">BlockSizeY</span></span>  <br/> |
   
<span data-ttu-id="800a1-110">Wenn Sie einen Verweis auf die Zelle BlockSizeY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="800a1-110">To get a reference to the BlockSizeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="800a1-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="800a1-111">Section index:</span></span>  <br/> |<span data-ttu-id="800a1-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="800a1-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="800a1-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="800a1-113">Row index:</span></span>  <br/> |<span data-ttu-id="800a1-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="800a1-114">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="800a1-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="800a1-115">Cell index:</span></span>  <br/> |<span data-ttu-id="800a1-116">**visPLOBlockSizeY**</span><span class="sxs-lookup"><span data-stu-id="800a1-116">**visPLOBlockSizeY**</span></span> <br/> |
   

