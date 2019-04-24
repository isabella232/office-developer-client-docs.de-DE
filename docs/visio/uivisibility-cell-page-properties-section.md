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
ms.openlocfilehash: 51ccd34cb40c286fe6b61818aea5a6b9c0b6d1a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357218"
---
# <a name="uivisibility-cell-page-properties-section"></a><span data-ttu-id="14ce5-103">Zelle "UIVisibility" (Abschnitt "Page Properties")</span><span class="sxs-lookup"><span data-stu-id="14ce5-103">UIVisibility Cell (Page Properties Section)</span></span>

<span data-ttu-id="14ce5-104">Bestimmt, ob der Seitenname auf der Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="14ce5-104">Determines whether the page name is exposed in the user interface (UI).</span></span>
  
|<span data-ttu-id="14ce5-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="14ce5-105">**Value**</span></span>|<span data-ttu-id="14ce5-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="14ce5-106">**Description**</span></span>|<span data-ttu-id="14ce5-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="14ce5-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="14ce5-108">0</span><span class="sxs-lookup"><span data-stu-id="14ce5-108">0</span></span>  <br/> |<span data-ttu-id="14ce5-109">Der Seitenname wird in der Benutzeroberfläche angezeigt (Standardwert).</span><span class="sxs-lookup"><span data-stu-id="14ce5-109">Display the page name in the UI (the default).</span></span>  <br/> |<span data-ttu-id="14ce5-110">**visUIVNormal**</span><span class="sxs-lookup"><span data-stu-id="14ce5-110">**visUIVNormal**</span></span> <br/> |
|<span data-ttu-id="14ce5-111">1</span><span class="sxs-lookup"><span data-stu-id="14ce5-111">1</span></span>  <br/> |<span data-ttu-id="14ce5-112">Der Seitenname wird nicht in der Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="14ce5-112">Do not display the page name in the UI.</span></span>  <br/> |<span data-ttu-id="14ce5-113">**visUIVHidden**</span><span class="sxs-lookup"><span data-stu-id="14ce5-113">**visUIVHidden**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14ce5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14ce5-114">Remarks</span></span>

<span data-ttu-id="14ce5-115">Das Festlegen der "UIVisibility-Zelle auf **visUIVHidden** verhindert, dass die Seite an einer beliebigen Stelle in der Benutzeroberfläche angezeigt wird, auf der die Zeichenfolge mit dem Seitennamen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="14ce5-115">Setting the UIVisibility cell to **visUIVHidden** prevents the page from appearing anywhere in the UI where the string containing the page name appears.</span></span> <span data-ttu-id="14ce5-116">Die Seite wäre beispielsweise nicht als Option im **Zeichnungs-Explorer** oder auf den Seitenregisterkarten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="14ce5-116">For example, the page would not be listed as an option in the **Drawing Explorer** or on the page tabs.</span></span> <span data-ttu-id="14ce5-117">Auf die Seite kann jedoch zugegriffen werden, wenn Sie Automatisierungs-oder UI-Pfade verwenden, die nicht den Seitennamen, beispielsweise den **Druck** Befehl, aufweisen.</span><span class="sxs-lookup"><span data-stu-id="14ce5-117">The page remains accessible, however, if you use Automation or UI paths that do not include the page name, for example, the **Print** command.</span></span> 
  
 <span data-ttu-id="14ce5-118">Diese Zelle ist für die Verwendung mit Dokumentseiten vorgesehen. Es ist nicht für die Verwendung mit Markup Überlagerungs Seiten vorgesehen, bei denen die "UIVisibility-Zelle standardmäßig auf **visUIVHidden** festgelegt ist und nicht geändert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="14ce5-118">This cell is intended for use with document pages; it is not intended for use with markup overlay pages, which have the UIVisibility cell set to **visUIVHidden** by default and should not be changed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="14ce5-119">Wenn Sie eine Seite aus dem **Druck** Befehl des Dokuments ausblenden möchten, legen Sie Sie als Hintergrundseite fest (**Type** -Eigenschaft ist **visTypeBackground** ), die von keiner Seite als Hintergrund verwendet wird (Shapes auf Hintergrundseiten werden gedruckt, wenn eine Seite, die es als Hintergrund verwendet, gedruckt).</span><span class="sxs-lookup"><span data-stu-id="14ce5-119">To hide a page from the document's **Print** command, make it a background page (**Type** property is **visTypeBackground** ) that is not used as a background by any page (shapes on background pages are printed when a page using it as a background is printed).</span></span> <span data-ttu-id="14ce5-120">Der **Druck** Befehl des Dokuments funktioniert nur mit indizierten Seiten, und Hintergrundseiten werden nicht indiziert.</span><span class="sxs-lookup"><span data-stu-id="14ce5-120">The document's **Print** command only works with indexed pages, and background pages are not indexed.</span></span> 
  
<span data-ttu-id="14ce5-121">Wenn Sie einen Verweis auf die Zelle "UIVisibility aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="14ce5-121">To get a reference to the UIVisibility cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="14ce5-122">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="14ce5-122">Cell name:</span></span>  <br/> |<span data-ttu-id="14ce5-123">"UIVisibility</span><span class="sxs-lookup"><span data-stu-id="14ce5-123">UIVisibility</span></span>  <br/> |
   
<span data-ttu-id="14ce5-124">Wenn Sie einen Verweis auf die Zelle "UIVisibility aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="14ce5-124">To get a reference to the UIVisibility cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="14ce5-125">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="14ce5-125">Section index:</span></span>  <br/> |<span data-ttu-id="14ce5-126">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="14ce5-126">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="14ce5-127">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="14ce5-127">Row index:</span></span>  <br/> |<span data-ttu-id="14ce5-128">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="14ce5-128">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="14ce5-129">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="14ce5-129">Cell index:</span></span>  <br/> |<span data-ttu-id="14ce5-130">**visPageUIVisibility**</span><span class="sxs-lookup"><span data-stu-id="14ce5-130">**visPageUIVisibility**</span></span> <br/> |
   

