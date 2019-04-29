---
title: Zelle "BeginGroup" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60022
localization_priority: Normal
ms.assetid: 1ae7f629-fb9f-1a11-1194-b381d6c9de5b
description: Gibt an, ob über dieser Aktion ein Trennzeichen in das Menü eingefügt wird.
ms.openlocfilehash: 115dbfe051201dc3ec2b127ff129b077e1067865
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407837"
---
# <a name="begingroup-cell-actions-section"></a><span data-ttu-id="dadb7-103">Zelle "BeginGroup" (Abschnitt "Actions")</span><span class="sxs-lookup"><span data-stu-id="dadb7-103">BeginGroup Cell (Actions Section)</span></span>

<span data-ttu-id="dadb7-104">Gibt an, ob über dieser Aktion ein Trennzeichen in das Menü eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="dadb7-104">Indicates whether a separator is inserted into the menu above this action.</span></span> 
  
|<span data-ttu-id="dadb7-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="dadb7-105">**Value**</span></span>|<span data-ttu-id="dadb7-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dadb7-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dadb7-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="dadb7-107">TRUE</span></span>  <br/> |<span data-ttu-id="dadb7-108">Über der Aktion wird ein Trennzeichen in das Menü eingefügt.</span><span class="sxs-lookup"><span data-stu-id="dadb7-108">A separator is inserted into the menu above this action.</span></span>  <br/> |
|<span data-ttu-id="dadb7-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="dadb7-109">FALSE</span></span>  <br/> |<span data-ttu-id="dadb7-110">Über der Aktion wird kein Trennzeichen in das Menü eingefügt (Standard).</span><span class="sxs-lookup"><span data-stu-id="dadb7-110">A separator is not inserted into the menu above this action (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dadb7-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dadb7-111">Remarks</span></span>

<span data-ttu-id="dadb7-112">Wenn Sie einen Verweis auf die Zelle beginGroup aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="dadb7-112">To get a reference to the BeginGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dadb7-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="dadb7-113">Cell name:</span></span>  <br/> |<span data-ttu-id="dadb7-114">Aktionen.</span><span class="sxs-lookup"><span data-stu-id="dadb7-114">Actions.</span></span> <span data-ttu-id="dadb7-115">*Name*. BeginGroup-Aktion.</span><span class="sxs-lookup"><span data-stu-id="dadb7-115">*name*.BeginGroup where Actions.</span></span> <span data-ttu-id="dadb7-116">*Name* ist der Name der Zeile Actions.</span><span class="sxs-lookup"><span data-stu-id="dadb7-116">*name* is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="dadb7-117">Wenn Sie einen Verweis auf die Zelle beginGroup nach Index aus einem Programm abrufen möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="dadb7-117">To get a reference to the BeginGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dadb7-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="dadb7-118">Section index:</span></span>  <br/> |<span data-ttu-id="dadb7-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="dadb7-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="dadb7-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="dadb7-120">Row index:</span></span>  <br/> |<span data-ttu-id="dadb7-121">**visRowAction** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="dadb7-121">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="dadb7-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="dadb7-122">Cell index:</span></span>  <br/> |<span data-ttu-id="dadb7-123">**visActionBeginGroup**</span><span class="sxs-lookup"><span data-stu-id="dadb7-123">**visActionBeginGroup**</span></span> <br/> |
   

