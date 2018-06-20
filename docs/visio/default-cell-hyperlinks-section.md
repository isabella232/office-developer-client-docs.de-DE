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
ms.openlocfilehash: a8bfc045559a2c2904ae4a97c489248fb6c446c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796816"
---
# <a name="default-cell-hyperlinks-section"></a><span data-ttu-id="f9cb2-104">Default Cell (Hyperlinks Section)</span><span class="sxs-lookup"><span data-stu-id="f9cb2-104">Default Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="f9cb2-p102">Legt den Standardhyperlink für ein Shape oder eine Seite fest. Setzen Sie den Wert dieser Zelle auf WAHR, um einen Hyperlink als Standardeinstellung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f9cb2-p102">Determines the default hyperlink for a shape or page. Set the value of this cell to TRUE to set a hyperlink as the default.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f9cb2-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9cb2-107">Remarks</span></span>

<span data-ttu-id="f9cb2-108">Sie können den Standardhyperlink auch festlegen, indem ein Shape auswählen, Sie auf der Registerkarte **Einfügen** auf **Hyperlink** klicken, einen Hyperlink auswählen und anschließend auf **Standard**.</span><span class="sxs-lookup"><span data-stu-id="f9cb2-108">You can also set the default hyperlink by selecting a shape, clicking **Hyperlink** on the **Insert** tab, selecting a hyperlink, and then clicking **Default**.</span></span> <span data-ttu-id="f9cb2-109">Der Standardhyperlink wird in Fettschrift angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f9cb2-109">The default hyperlink appears in bold text.</span></span>
  
<span data-ttu-id="f9cb2-110">Wenn Sie einen Verweis auf die Zelle Default nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f9cb2-110">To get a reference to the Default cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f9cb2-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="f9cb2-111">Cell name:</span></span>  <br/> |<span data-ttu-id="f9cb2-112">Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="f9cb2-112">Hyperlink.</span></span> <span data-ttu-id="f9cb2-113">*Name* . Standard, in dem Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="f9cb2-113">*Name*  .Default           where Hyperlink.</span></span> <span data-ttu-id="f9cb2-114">*Name* ist der Zeilenname</span><span class="sxs-lookup"><span data-stu-id="f9cb2-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="f9cb2-115">Wenn Sie einen Verweis auf die Zelle Default aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="f9cb2-115">To get a reference to the Default cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f9cb2-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="f9cb2-116">Section index:</span></span>  <br/> |<span data-ttu-id="f9cb2-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="f9cb2-117">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="f9cb2-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="f9cb2-118">Row index:</span></span>  <br/> |<span data-ttu-id="f9cb2-119">**visRow1stHyperlink** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f9cb2-119">**visRow1stHyperlink** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="f9cb2-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="f9cb2-120">Cell index:</span></span>  <br/> |<span data-ttu-id="f9cb2-121">**visHLinkDefault**</span><span class="sxs-lookup"><span data-stu-id="f9cb2-121">**visHLinkDefault**</span></span> <br/> |
   

