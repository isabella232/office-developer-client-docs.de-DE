---
title: Zelle "Default" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251545
localization_priority: Normal
ms.assetid: 0edea0ea-58dd-15da-6d4f-185d40133452
description: Legt den Standardhyperlink für ein Shape oder eine Seite fest. Setzen Sie den Wert dieser Zelle auf WAHR, um einen Hyperlink als Standardeinstellung festzulegen.
ms.openlocfilehash: 9991bd0e241c5dfd4fda65aeff8b6cc203ad3458
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360277"
---
# <a name="default-cell-hyperlinks-section"></a><span data-ttu-id="cfced-104">Zelle "Default" (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="cfced-104">Default Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="cfced-p102">Legt den Standardhyperlink für ein Shape oder eine Seite fest. Setzen Sie den Wert dieser Zelle auf WAHR, um einen Hyperlink als Standardeinstellung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="cfced-p102">Determines the default hyperlink for a shape or page. Set the value of this cell to TRUE to set a hyperlink as the default.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cfced-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfced-107">Remarks</span></span>

<span data-ttu-id="cfced-p103">Sie können den Standardhyperlink auch festlegen, indem Sie ein Shape auswählen, auf der Registerkarte **Einfügen** auf **Hyperlink** klicken, einen Hyperlink auswählen und anschließend auf **Standard** klicken. Der Standardhyperlink wird fett angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cfced-p103">You can also set the default hyperlink by selecting a shape, clicking **Hyperlink** on the **Insert** tab, selecting a hyperlink, and then clicking **Default**. The default hyperlink appears in bold text.</span></span>
  
<span data-ttu-id="cfced-110">Wenn Sie einen Verweis auf die Standardzelle nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="cfced-110">To get a reference to the Default cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cfced-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="cfced-111">Cell name:</span></span>  <br/> |<span data-ttu-id="cfced-112">Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="cfced-112">Hyperlink.</span></span> <span data-ttu-id="cfced-113">*Name* . Standard, wobei Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="cfced-113">*Name*  .Default           where Hyperlink.</span></span> <span data-ttu-id="cfced-114">*Name* ist der Name der Zeile</span><span class="sxs-lookup"><span data-stu-id="cfced-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="cfced-115">Wenn Sie einen Verweis auf die Zelle Default aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="cfced-115">To get a reference to the Default cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cfced-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="cfced-116">Section index:</span></span>  <br/> |<span data-ttu-id="cfced-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="cfced-117">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="cfced-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="cfced-118">Row index:</span></span>  <br/> |<span data-ttu-id="cfced-119">**visRow1stHyperlink** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="cfced-119">**visRow1stHyperlink** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="cfced-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="cfced-120">Cell index:</span></span>  <br/> |<span data-ttu-id="cfced-121">**visHLinkDefault**</span><span class="sxs-lookup"><span data-stu-id="cfced-121">**visHLinkDefault**</span></span> <br/> |
   

