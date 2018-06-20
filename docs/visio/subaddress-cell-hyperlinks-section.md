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
ms.openlocfilehash: 0509b9b6a708924b5aeb69f16f3f4cd99573cc0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798218"
---
# <a name="subaddress-cell-hyperlinks-section"></a><span data-ttu-id="8291b-103">SubAddress Cell (Hyperlinks Section)</span><span class="sxs-lookup"><span data-stu-id="8291b-103">SubAddress Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="8291b-104">Gibt eine Position im Zieldokument an, mit der eine Verknüpfung hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8291b-104">Specifies a location within the target document to link to.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8291b-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8291b-105">Remarks</span></span>

<span data-ttu-id="8291b-106">Angenommen, wenn die Zelle Address "Drawing1.vsdx" ist, kann die Zelle SubAddress ein Seitenname wie "Seite 3" angeben.</span><span class="sxs-lookup"><span data-stu-id="8291b-106">For example, if the Address cell is "Drawing1.vsdx", the SubAddress cell can specify a page name such as "Page-3".</span></span> <span data-ttu-id="8291b-107">Wenn die Zelle Address der Microsoft Excel-Datei "Samples.xlsx" ist, kann der Wert dieser Zelle ein Arbeitsblatt oder einen Bereich in einem Arbeitsblatt, z. B. "Microsoft Excel-Arbeitsblattfunktionen" oder "Sheet1! sein A1: D10 ".</span><span class="sxs-lookup"><span data-stu-id="8291b-107">If the Address cell is the Microsoft Excel file "Samples.xlsx", the value of this cell can be a worksheet or range within a worksheet, such as "Worksheet Functions" or "Sheet1!A1:D10".</span></span> <span data-ttu-id="8291b-108">Wenn die Zelle Address "http://www.microsoft.com/office/", kann der Wert dieser Zelle einen benannten Anker innerhalb des Dokuments, z. B. "Solutions" sein.</span><span class="sxs-lookup"><span data-stu-id="8291b-108">If the Address cell is "http://www.microsoft.com/office/", the value of this cell can be a named anchor within the document, such as "solutions".</span></span>
  
<span data-ttu-id="8291b-109">Sie können den Wert dieser Zelle auch im Dialogfeld **Hyperlinks** festlegen (klicken Sie in der Gruppe **Hyperlinks** auf der Registerkarte **Einfügen** auf **Hyperlink**).</span><span class="sxs-lookup"><span data-stu-id="8291b-109">You can also set the value of this cell in the **Hyperlinks** dialog box (in the **Links** group on the **Insert** tab, click **Hyperlink**).</span></span>
  
<span data-ttu-id="8291b-110">Wenn Sie einen Verweis auf die Zelle SubAddress nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8291b-110">To get a reference to the SubAddress cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8291b-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="8291b-111">Cell name:</span></span>  <br/> | <span data-ttu-id="8291b-112">Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="8291b-112">Hyperlink.</span></span>  <span data-ttu-id="8291b-113">*Name* . SubAddress, in dem Hyperlink *.name* der Zeilenname ist</span><span class="sxs-lookup"><span data-stu-id="8291b-113">*name*  .SubAddress where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="8291b-114">Wenn Sie einen Verweis auf die Zelle **SubAddress** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="8291b-114">To get a reference to the **SubAddress** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8291b-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="8291b-115">Section index:</span></span>  <br/> |<span data-ttu-id="8291b-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="8291b-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="8291b-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="8291b-117">Row index:</span></span>  <br/> |<span data-ttu-id="8291b-118">**visRow1stHyperlink** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8291b-118">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8291b-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="8291b-119">Cell index:</span></span>  <br/> |<span data-ttu-id="8291b-120">**visHLinkSubAddress**</span><span class="sxs-lookup"><span data-stu-id="8291b-120">**visHLinkSubAddress**</span></span> <br/> |
   

