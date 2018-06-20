---
title: Zelle "AddMarkup" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030801
localization_priority: Normal
ms.assetid: 46146424-b4c9-2240-36c0-19bb35ec51d1
description: Gibt an, ob das Dokument für ein Markup überprüft wird.
ms.openlocfilehash: 69430122b0a7665d7daa4a6b28f3a51745b74473
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796399"
---
# <a name="addmarkup-cell-document-properties-section"></a><span data-ttu-id="cb8ca-103">AddMarkup Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="cb8ca-103">AddMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="cb8ca-104">Gibt an, ob das Dokument für ein Markup überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="cb8ca-104">Indicates whether the document is being reviewed for markup.</span></span>
  
|<span data-ttu-id="cb8ca-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="cb8ca-105">**Value**</span></span>|<span data-ttu-id="cb8ca-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cb8ca-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cb8ca-107">WAHR</span><span class="sxs-lookup"><span data-stu-id="cb8ca-107">TRUE</span></span>  <br/> |<span data-ttu-id="cb8ca-108">Dokument wird überprüft.</span><span class="sxs-lookup"><span data-stu-id="cb8ca-108">Document is being reviewed.</span></span>  <br/> |
|<span data-ttu-id="cb8ca-109">FALSCH</span><span class="sxs-lookup"><span data-stu-id="cb8ca-109">FALSE</span></span>  <br/> |<span data-ttu-id="cb8ca-110">Dokument wird nicht überprüft (Standard).</span><span class="sxs-lookup"><span data-stu-id="cb8ca-110">Document is not being reviewed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb8ca-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb8ca-111">Remarks</span></span>

<span data-ttu-id="cb8ca-112">Wenn die Zelle auf true festgelegt ist, der Prüfer festgelegt ist AddMarkup ist gelten Hinzufügen von Markup und Änderungen für Markup Überlagerung Seiten, nicht auf das ursprüngliche Zeichenblätter.</span><span class="sxs-lookup"><span data-stu-id="cb8ca-112">When the AddMarkup cell is set to TRUE, the reviewer is adding markup and changes are applied to markup overlay pages, not to original drawing pages.</span></span> <span data-ttu-id="cb8ca-113">Wenn die Zelle AddMarkup Markup nachverfolgen "false" ist ist deaktiviert, und Änderungen auf die ursprüngliche Zeichenblätter angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="cb8ca-113">When the AddMarkup cell is FALSE, markup tracking is off and changes are applied to the original drawing pages.</span></span>
  
> [!NOTE]
> <span data-ttu-id="cb8ca-114">Sie können auf Ihre Dokumente Markup verhindern, mithilfe der GUARD-Funktion.</span><span class="sxs-lookup"><span data-stu-id="cb8ca-114">You can prevent markup on your documents by using the GUARD function.</span></span> <span data-ttu-id="cb8ca-115">Wenn die Zelle AddMarkup die Formel =Guard(falsch), der Befehl **Markup verfolgen** ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="cb8ca-115">If the AddMarkup cell contains the formula =GUARD(FALSE), the **Track Markup** command is disabled.</span></span> 
  
<span data-ttu-id="cb8ca-116">Diese Einstellung entspricht der Einstellung **Markup verfolgen** den Befehl in der Gruppe **Markup** der Registerkarte **Überprüfen** .</span><span class="sxs-lookup"><span data-stu-id="cb8ca-116">This setting corresponds to the **Track Markup** command setting in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="cb8ca-117">Wenn Sie einen Verweis auf die Zelle AddMarkup nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="cb8ca-117">To get a reference to the AddMarkup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cb8ca-118">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="cb8ca-118">Cell name:</span></span>  <br/> |<span data-ttu-id="cb8ca-119">AddMarkup</span><span class="sxs-lookup"><span data-stu-id="cb8ca-119">AddMarkup</span></span>  <br/> |
   
<span data-ttu-id="cb8ca-120">Wenn Sie einen Verweis auf die Zelle AddMarkup aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="cb8ca-120">To get a reference to the AddMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cb8ca-121">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="cb8ca-121">Section index:</span></span>  <br/> |<span data-ttu-id="cb8ca-122">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cb8ca-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="cb8ca-123">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="cb8ca-123">Row index:</span></span>  <br/> |<span data-ttu-id="cb8ca-124">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="cb8ca-124">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="cb8ca-125">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="cb8ca-125">Cell index:</span></span>  <br/> |<span data-ttu-id="cb8ca-126">**visDocAddMarkup**</span><span class="sxs-lookup"><span data-stu-id="cb8ca-126">**visDocAddMarkup**</span></span> <br/> |
   

