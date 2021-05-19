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
# <a name="subaddress-cell-hyperlinks-section"></a><span data-ttu-id="2813f-103">Zelle "SubAddress" (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="2813f-103">SubAddress Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="2813f-104">Gibt eine Position im Zieldokument an, mit der eine Verknüpfung hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2813f-104">Specifies a location within the target document to link to.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2813f-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2813f-105">Remarks</span></span>

<span data-ttu-id="2813f-106">Wenn die Zelle Address beispielsweise "Drawing1.vsdx" ist, kann die Zelle SubAddress einen Seitennamen wie "Page-3" angeben.</span><span class="sxs-lookup"><span data-stu-id="2813f-106">For example, if the Address cell is "Drawing1.vsdx", the SubAddress cell can specify a page name such as "Page-3".</span></span> <span data-ttu-id="2813f-107">Wenn die Zelle Address die Microsoft Excel "Samples.xlsx" ist, kann der Wert dieser Zelle ein Arbeitsblatt oder ein Bereich innerhalb eines Arbeitsblatts sein, z. B. "Worksheet Functions" oder "Sheet1! A1:D10".</span><span class="sxs-lookup"><span data-stu-id="2813f-107">If the Address cell is the Microsoft Excel file "Samples.xlsx", the value of this cell can be a worksheet or range within a worksheet, such as "Worksheet Functions" or "Sheet1!A1:D10".</span></span> <span data-ttu-id="2813f-108">Wenn die Zelle Address den Wert " hat, kann der Wert dieser Zelle ein benannter Anker im Dokument sein, z. B. https://www.microsoft.com/office/ "lösungen".</span><span class="sxs-lookup"><span data-stu-id="2813f-108">If the Address cell is "https://www.microsoft.com/office/", the value of this cell can be a named anchor within the document, such as "solutions".</span></span>
  
<span data-ttu-id="2813f-109">Sie können den Wert dieser Zelle auch im Dialogfeld **Hyperlinks** festlegen (klicken Sie dazu auf der Registerkarte **Einfügen** in der Gruppe **Hyperlinks** auf **Hyperlink**).</span><span class="sxs-lookup"><span data-stu-id="2813f-109">You can also set the value of this cell in the **Hyperlinks** dialog box (in the **Links** group on the **Insert** tab, click **Hyperlink**).</span></span>
  
<span data-ttu-id="2813f-110">Verwenden Sie zum Erhalten eines Verweises auf die Zelle SubAddress anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="2813f-110">To get a reference to the SubAddress cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2813f-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2813f-111">Cell name:</span></span>  <br/> | <span data-ttu-id="2813f-112">Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="2813f-112">Hyperlink.</span></span>  <span data-ttu-id="2813f-113">*Name*  . SubAddress, wobei Hyperlink  *.name*  der Zeilenname ist</span><span class="sxs-lookup"><span data-stu-id="2813f-113">*name*  .SubAddress where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="2813f-114">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle SubAddress** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="2813f-114">To get a reference to the **SubAddress** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2813f-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2813f-115">Section index:</span></span>  <br/> |<span data-ttu-id="2813f-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="2813f-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="2813f-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2813f-117">Row index:</span></span>  <br/> |<span data-ttu-id="2813f-118">**visRow1stHyperlink**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2813f-118">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2813f-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2813f-119">Cell index:</span></span>  <br/> |<span data-ttu-id="2813f-120">**visHLinkSubAddress**</span><span class="sxs-lookup"><span data-stu-id="2813f-120">**visHLinkSubAddress**</span></span> <br/> |
   

