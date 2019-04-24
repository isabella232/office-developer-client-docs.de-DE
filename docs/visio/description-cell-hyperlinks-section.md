---
title: Zelle "Description" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm230
localization_priority: Normal
ms.assetid: 2f571c65-6b7a-5a3a-c075-3c52d3ab989b
description: Stellt eine beschreibende Textzeichenfolge für einen Hyperlink dar.
ms.openlocfilehash: b58e6dc3ec2fc3b64db00e0f19e0718fe897aaa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360242"
---
# <a name="description-cell-hyperlinks-section"></a><span data-ttu-id="83330-103">Zelle "Description" (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="83330-103">Description Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="83330-104">Stellt eine beschreibende Textzeichenfolge für einen Hyperlink dar.</span><span class="sxs-lookup"><span data-stu-id="83330-104">Represents a descriptive text string for a hyperlink.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="83330-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83330-105">Remarks</span></span>

<span data-ttu-id="83330-106">Verwenden Sie diese Zelle, um Kommentare zum Hyperlink zu speichern. Beispiel: "Link zu unserer Preis-Website".</span><span class="sxs-lookup"><span data-stu-id="83330-106">Use this cell to store comments about the hyperlink; for example, "Link to our pricing website."</span></span>
  
<span data-ttu-id="83330-107">Sie können den Wert dieser Zelle auch im Dialogfeld **Hyperlinks** festlegen (klicken Sie dazu auf der Registerkarte **Einfügen** auf **Hyperlink**).</span><span class="sxs-lookup"><span data-stu-id="83330-107">You can also set the value of this cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="83330-108">Wenn Sie einen Verweis auf die Zelle Description aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="83330-108">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="83330-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="83330-109">Cell name:</span></span>  <br/> | <span data-ttu-id="83330-110">Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="83330-110">Hyperlink.</span></span>  <span data-ttu-id="83330-111">*Name* . Beschreibung des Hyperlinks.</span><span class="sxs-lookup"><span data-stu-id="83330-111">*Name*  .Description where Hyperlink.</span></span>  <span data-ttu-id="83330-112">*Name* ist der Name der Hyperlink-Zeile.</span><span class="sxs-lookup"><span data-stu-id="83330-112">*Name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="83330-113">Wenn Sie einen Verweis auf die Zelle Description aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="83330-113">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="83330-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="83330-114">Section index:</span></span>  <br/> |<span data-ttu-id="83330-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="83330-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="83330-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="83330-116">Row index:</span></span>  <br/> |<span data-ttu-id="83330-117">**visRow1stHyperlink** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="83330-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="83330-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="83330-118">Cell index:</span></span>  <br/> |<span data-ttu-id="83330-119">**visHLinkDescription**</span><span class="sxs-lookup"><span data-stu-id="83330-119">**visHLinkDescription**</span></span> <br/> |
   

