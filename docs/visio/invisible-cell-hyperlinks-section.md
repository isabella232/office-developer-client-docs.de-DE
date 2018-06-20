---
title: Zelle "Invisible" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033755
localization_priority: Normal
ms.assetid: e67dcd83-4a88-a0f8-5c6a-dae51424edbd
description: Gibt an, ob im Kontextmenü eines Shapes oder einer Seite ein Hyperlink angezeigt wird.
ms.openlocfilehash: e269c5e907afa0d49f1fc6115b7a031835467c2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797225"
---
# <a name="invisible-cell-hyperlinks-section"></a><span data-ttu-id="7adb2-103">Zelle "Invisible" (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="7adb2-103">Invisible Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="7adb2-104">Gibt an, ob im Kontextmenü eines Shapes oder einer Seite ein Hyperlink angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7adb2-104">Indicates whether a hyperlink appears on the shortcut menu for a shape or page.</span></span> 
  
|<span data-ttu-id="7adb2-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7adb2-105">**Value**</span></span>|<span data-ttu-id="7adb2-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7adb2-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7adb2-107">WAHR</span><span class="sxs-lookup"><span data-stu-id="7adb2-107">TRUE</span></span>  <br/> |<span data-ttu-id="7adb2-108">Im Kontextmenü wird kein Hyperlink als Menüelement angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7adb2-108">The hyperlink does not appear as a menu item on the shortcut menu.</span></span>  <br/> |
|<span data-ttu-id="7adb2-109">FALSCH</span><span class="sxs-lookup"><span data-stu-id="7adb2-109">FALSE</span></span>  <br/> |<span data-ttu-id="7adb2-110">Im Kontextmenü wird ein Hyperlink als Menüelement angezeigt (Standardwert).</span><span class="sxs-lookup"><span data-stu-id="7adb2-110">The hyperlink does appear as a menu item on the shortcut menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7adb2-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7adb2-111">Remarks</span></span>

<span data-ttu-id="7adb2-112">Wenn Sie einen Verweis auf die Zelle Invisible nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7adb2-112">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7adb2-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="7adb2-113">Cell name:</span></span>  <br/> |<span data-ttu-id="7adb2-114">Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="7adb2-114">Hyperlink.</span></span> <span data-ttu-id="7adb2-115">*Name* . Unsichtbar, in dem Hyperlink *.name* der Zeilenname ist</span><span class="sxs-lookup"><span data-stu-id="7adb2-115">*name*  .Invisible where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="7adb2-116">Wenn Sie einen Verweis auf die Zelle Invisible aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="7adb2-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7adb2-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="7adb2-117">Section index:</span></span>  <br/> |<span data-ttu-id="7adb2-118">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="7adb2-118">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="7adb2-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="7adb2-119">Row index:</span></span>  <br/> |<span data-ttu-id="7adb2-120">**visRow1stHyperlink** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7adb2-120">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="7adb2-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="7adb2-121">Cell index:</span></span>  <br/> |<span data-ttu-id="7adb2-122">**visHLinkInvisible**</span><span class="sxs-lookup"><span data-stu-id="7adb2-122">**visHLinkInvisible**</span></span> <br/> |
   

