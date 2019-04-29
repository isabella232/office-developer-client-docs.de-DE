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
ms.openlocfilehash: 4e0860639b0d89fce2c35a8947bd5ac00fcc63e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427633"
---
# <a name="addmarkup-cell-document-properties-section"></a><span data-ttu-id="52f0c-103">Zelle "AddMarkup" (Abschnitt "Document Properties")</span><span class="sxs-lookup"><span data-stu-id="52f0c-103">AddMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="52f0c-104">Gibt an, ob das Dokument für ein Markup überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="52f0c-104">Indicates whether the document is being reviewed for markup.</span></span>
  
|<span data-ttu-id="52f0c-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="52f0c-105">**Value**</span></span>|<span data-ttu-id="52f0c-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="52f0c-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="52f0c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="52f0c-107">TRUE</span></span>  <br/> |<span data-ttu-id="52f0c-108">Dokument wird überprüft.</span><span class="sxs-lookup"><span data-stu-id="52f0c-108">Document is being reviewed.</span></span>  <br/> |
|<span data-ttu-id="52f0c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="52f0c-109">FALSE</span></span>  <br/> |<span data-ttu-id="52f0c-110">Dokument wird nicht überprüft (Standard).</span><span class="sxs-lookup"><span data-stu-id="52f0c-110">Document is not being reviewed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52f0c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52f0c-111">Remarks</span></span>

<span data-ttu-id="52f0c-112">Wenn die Zelle AddMarkup auf WAHR festgelegt ist, fügt der Prüfer das Markup hinzu, und die Änderungen werden auf Markupüberlagerungsseiten angewendet, nicht auf die ursprünglichen Zeichenblätter.</span><span class="sxs-lookup"><span data-stu-id="52f0c-112">When the AddMarkup cell is set to TRUE, the reviewer is adding markup and changes are applied to markup overlay pages, not to original drawing pages.</span></span> <span data-ttu-id="52f0c-113">Wenn die Zelle AddMarkup auf FALSE festgelegt ist, ist die Markupverfolgung deaktiviert, und die Änderungen werden auf die ursprünglichen Zeichenblätter angewendet.</span><span class="sxs-lookup"><span data-stu-id="52f0c-113">When the AddMarkup cell is FALSE, markup tracking is off and changes are applied to the original drawing pages.</span></span>
  
> [!NOTE]
> <span data-ttu-id="52f0c-114">Sie können das Markup in Ihren Dokumenten mithilfe der GUARD-Funktion verhindern.</span><span class="sxs-lookup"><span data-stu-id="52f0c-114">You can prevent markup on your documents by using the GUARD function.</span></span> <span data-ttu-id="52f0c-115">Wenn die Zelle addMarkup die Formel = GUARD (FALSE) enthält, ist der Befehl **Markup verfolgen** deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="52f0c-115">If the AddMarkup cell contains the formula =GUARD(FALSE), the **Track Markup** command is disabled.</span></span> 
  
<span data-ttu-id="52f0c-116">Diese Einstellung entspricht der Einstellung für den Befehl **Änderungen markieren** in der Gruppe **Markup** der Registerkarte **Überprüfen**.</span><span class="sxs-lookup"><span data-stu-id="52f0c-116">This setting corresponds to the **Track Markup** command setting in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="52f0c-117">Wenn Sie einen Verweis auf die Zelle addMarkup aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="52f0c-117">To get a reference to the AddMarkup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="52f0c-118">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="52f0c-118">Cell name:</span></span>  <br/> |<span data-ttu-id="52f0c-119">"AddMarkup</span><span class="sxs-lookup"><span data-stu-id="52f0c-119">AddMarkup</span></span>  <br/> |
   
<span data-ttu-id="52f0c-120">Wenn Sie einen Verweis auf die Zelle addMarkup aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="52f0c-120">To get a reference to the AddMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="52f0c-121">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="52f0c-121">Section index:</span></span>  <br/> |<span data-ttu-id="52f0c-122">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="52f0c-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="52f0c-123">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="52f0c-123">Row index:</span></span>  <br/> |<span data-ttu-id="52f0c-124">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="52f0c-124">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="52f0c-125">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="52f0c-125">Cell index:</span></span>  <br/> |<span data-ttu-id="52f0c-126">**visDocAddMarkup**</span><span class="sxs-lookup"><span data-stu-id="52f0c-126">**visDocAddMarkup**</span></span> <br/> |
   

