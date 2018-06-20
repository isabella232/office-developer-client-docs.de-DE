---
title: Zelle "UIVisibility" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60090
localization_priority: Normal
ms.assetid: df7f79df-770a-4868-e7e2-05c3828e23eb
description: Bestimmt, ob der Seitenname auf der Benutzeroberfläche angezeigt wird.
ms.openlocfilehash: dcb4a14ff89c7f5c77916e6b188aaf87e1711ab0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798365"
---
# <a name="uivisibility-cell-page-properties-section"></a><span data-ttu-id="1f78c-103">Zelle "UIVisibility" (Abschnitt "Page Properties")</span><span class="sxs-lookup"><span data-stu-id="1f78c-103">UIVisibility Cell (Page Properties Section)</span></span>

<span data-ttu-id="1f78c-104">Bestimmt, ob der Seitenname auf der Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1f78c-104">Determines whether the page name is exposed in the user interface (UI).</span></span>
  
|<span data-ttu-id="1f78c-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="1f78c-105">**Value**</span></span>|<span data-ttu-id="1f78c-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1f78c-106">**Description**</span></span>|<span data-ttu-id="1f78c-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="1f78c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1f78c-108">0</span><span class="sxs-lookup"><span data-stu-id="1f78c-108">0</span></span>  <br/> |<span data-ttu-id="1f78c-109">Der Seitenname wird in der Benutzeroberfläche angezeigt (Standardwert).</span><span class="sxs-lookup"><span data-stu-id="1f78c-109">Display the page name in the UI (the default).</span></span>  <br/> |<span data-ttu-id="1f78c-110">**visUIVNormal**</span><span class="sxs-lookup"><span data-stu-id="1f78c-110">**visUIVNormal**</span></span> <br/> |
|<span data-ttu-id="1f78c-111">1</span><span class="sxs-lookup"><span data-stu-id="1f78c-111">1</span></span>  <br/> |<span data-ttu-id="1f78c-112">Der Seitenname wird nicht in der Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1f78c-112">Do not display the page name in the UI.</span></span>  <br/> |<span data-ttu-id="1f78c-113">**UIVisibility**</span><span class="sxs-lookup"><span data-stu-id="1f78c-113">**visUIVHidden**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f78c-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1f78c-114">Remarks</span></span>

<span data-ttu-id="1f78c-115">Wenn die Zelle UIVisibility auf **UIVisibility** verhindert die Seite an einer beliebigen Stelle in der Benutzeroberfläche, wo die Zeichenfolge mit dem Namen der Seite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1f78c-115">Setting the UIVisibility cell to **visUIVHidden** prevents the page from appearing anywhere in the UI where the string containing the page name appears.</span></span> <span data-ttu-id="1f78c-116">Beispielsweise wird die Seite nicht als Option im **Zeichnungsexplorer** oder auf den Seitenregisterkarten aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="1f78c-116">For example, the page would not be listed as an option in the **Drawing Explorer** or on the page tabs.</span></span> <span data-ttu-id="1f78c-117">Die Seite weiterhin zugegriffen werden, jedoch bei Verwendung von Automatisierung oder Benutzeroberfläche Pfade, die nicht der Seitenname, beispielsweise den Befehl " **Drucken** " enthalten.</span><span class="sxs-lookup"><span data-stu-id="1f78c-117">The page remains accessible, however, if you use Automation or UI paths that do not include the page name, for example, the **Print** command.</span></span> 
  
 <span data-ttu-id="1f78c-118">Diese Zelle ist für die Verwendung mit Dokumentseiten bestimmt. Es sollte nicht für die Verwendung mit Markup Überlagerung Seiten, auf denen die Zelle UIVisibility standardmäßig auf **UIVisibility** festgelegt haben und sollte nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="1f78c-118">This cell is intended for use with document pages; it is not intended for use with markup overlay pages, which have the UIVisibility cell set to **visUIVHidden** by default and should not be changed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1f78c-119">Um eine Seite des Dokuments **Drucken** Befehl ausblenden möchten, können sie ein Hintergrundblatt (**Type** -Eigenschaft ist **VisTypeBackground** ), die nicht als Hintergrund jeder Seite (Shapes auf Seiten gedruckt werden, wenn eine Seite mit es als Hintergrund Hintergrund verwendet wird gedruckt).</span><span class="sxs-lookup"><span data-stu-id="1f78c-119">To hide a page from the document's **Print** command, make it a background page (**Type** property is **visTypeBackground** ) that is not used as a background by any page (shapes on background pages are printed when a page using it as a background is printed).</span></span> <span data-ttu-id="1f78c-120">Befehl **Drucken** des Dokuments funktioniert nur für indizierte Seiten und Hintergrundblätter werden nicht indiziert.</span><span class="sxs-lookup"><span data-stu-id="1f78c-120">The document's **Print** command only works with indexed pages, and background pages are not indexed.</span></span> 
  
<span data-ttu-id="1f78c-121">Zum Abrufen eines Verweises auf die Zelle UIVisibility nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1f78c-121">To get a reference to the UIVisibility cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1f78c-122">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="1f78c-122">Cell name:</span></span>  <br/> |<span data-ttu-id="1f78c-123">UIVisibility</span><span class="sxs-lookup"><span data-stu-id="1f78c-123">UIVisibility</span></span>  <br/> |
   
<span data-ttu-id="1f78c-124">Wenn Sie einen Verweis auf die Zelle UIVisibility aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="1f78c-124">To get a reference to the UIVisibility cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1f78c-125">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="1f78c-125">Section index:</span></span>  <br/> |<span data-ttu-id="1f78c-126">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1f78c-126">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1f78c-127">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="1f78c-127">Row index:</span></span>  <br/> |<span data-ttu-id="1f78c-128">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="1f78c-128">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="1f78c-129">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="1f78c-129">Cell index:</span></span>  <br/> |<span data-ttu-id="1f78c-130">**visPageUIVisibility**</span><span class="sxs-lookup"><span data-stu-id="1f78c-130">**visPageUIVisibility**</span></span> <br/> |
   

