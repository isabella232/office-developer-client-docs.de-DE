---
title: Zelle "SubAddress" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm985
localization_priority: Normal
ms.assetid: 949448fd-0f85-b56a-945e-1da0e48609e8
description: Gibt eine Position im Zieldokument an, mit der eine Verknüpfung hergestellt werden kann.
ms.openlocfilehash: 092a53bd7c9d5adb77ed35f3e2ef53888bd6ebea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349322"
---
# <a name="subaddress-cell-hyperlinks-section"></a><span data-ttu-id="64073-103">Zelle "SubAddress" (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="64073-103">SubAddress Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="64073-104">Gibt eine Position im Zieldokument an, mit der eine Verknüpfung hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="64073-104">Specifies a location within the target document to link to.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="64073-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64073-105">Remarks</span></span>

<span data-ttu-id="64073-106">Wenn die Zelle Address beispielsweise "Zeichnung1. vsdx" ist, kann die Zelle unter Adresse einen Seitennamen wie "page-3" angeben.</span><span class="sxs-lookup"><span data-stu-id="64073-106">For example, if the Address cell is "Drawing1.vsdx", the SubAddress cell can specify a page name such as "Page-3".</span></span> <span data-ttu-id="64073-107">Wenn die Zelle address die Microsoft Excel-Datei Samples. xlsx ist, kann der Wert dieser Zelle ein Arbeitsblatt oder ein Bereich innerhalb eines Arbeitsblatts sein, beispielsweise "Arbeitsblattfunktionen" oder "Sheet1! A1: D10 ".</span><span class="sxs-lookup"><span data-stu-id="64073-107">If the Address cell is the Microsoft Excel file "Samples.xlsx", the value of this cell can be a worksheet or range within a worksheet, such as "Worksheet Functions" or "Sheet1!A1:D10".</span></span> <span data-ttu-id="64073-108">Wenn die Zelle Address "https://www.microsoft.com/office/" ist, kann der Wert dieser Zelle ein benannter Anker innerhalb des Dokuments sein, beispielsweise "Lösungen".</span><span class="sxs-lookup"><span data-stu-id="64073-108">If the Address cell is "https://www.microsoft.com/office/", the value of this cell can be a named anchor within the document, such as "solutions".</span></span>
  
<span data-ttu-id="64073-109">Sie können den Wert dieser Zelle auch im Dialogfeld **Hyperlinks** festlegen (klicken Sie dazu auf der Registerkarte **Einfügen** in der Gruppe **Hyperlinks** auf **Hyperlink**).</span><span class="sxs-lookup"><span data-stu-id="64073-109">You can also set the value of this cell in the **Hyperlinks** dialog box (in the **Links** group on the **Insert** tab, click **Hyperlink**).</span></span>
  
<span data-ttu-id="64073-110">Wenn Sie einen Verweis auf die Zelle subAddress aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="64073-110">To get a reference to the SubAddress cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="64073-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="64073-111">Cell name:</span></span>  <br/> | <span data-ttu-id="64073-112">Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="64073-112">Hyperlink.</span></span>  <span data-ttu-id="64073-113">*Name* . Unter Adresse, bei der Hyperlink *. Name* der Zeilenname ist</span><span class="sxs-lookup"><span data-stu-id="64073-113">*name*  .SubAddress where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="64073-114">Wenn Sie einen Verweis auf die \*\*\*\* Zelle SubAddress aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="64073-114">To get a reference to the **SubAddress** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="64073-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="64073-115">Section index:</span></span>  <br/> |<span data-ttu-id="64073-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="64073-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="64073-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="64073-117">Row index:</span></span>  <br/> |<span data-ttu-id="64073-118">**visRow1stHyperlink** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="64073-118">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="64073-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="64073-119">Cell index:</span></span>  <br/> |<span data-ttu-id="64073-120">**visHLinkSubAddress**</span><span class="sxs-lookup"><span data-stu-id="64073-120">**visHLinkSubAddress**</span></span> <br/> |
   

