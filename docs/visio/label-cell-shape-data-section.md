---
title: Zelle "Label" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm510
localization_priority: Normal
ms.assetid: 6d328b1c-8d92-eb1a-7317-7dd85c674ff9
description: Legt die Beschriftung fest, die Benutzern im Fenster Shape-Daten angezeigt wird. Eine Beschriftung besteht aus alphanumerischen Zeichen, einschließlich dem Unterstrich (_).
ms.openlocfilehash: d341acfbd47446a5b6dbee51ed821d1e1f34e15d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420178"
---
# <a name="label-cell-shape-data-section"></a><span data-ttu-id="17bef-104">Zelle "Label" (Abschnitt "Shape Data")</span><span class="sxs-lookup"><span data-stu-id="17bef-104">Label Cell (Shape Data Section)</span></span>

<span data-ttu-id="17bef-p102">Legt die Beschriftung fest, die Benutzern im Fenster **Shape-Daten** angezeigt wird. Eine Beschriftung besteht aus alphanumerischen Zeichen, einschließlich dem Unterstrich (_).</span><span class="sxs-lookup"><span data-stu-id="17bef-p102">Specifies the label that appears to users in the **Shape Data** window. A label consists of alphanumeric characters, including the underscore (_) character.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="17bef-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="17bef-107">Remarks</span></span>

<span data-ttu-id="17bef-108">Die Anwendung schließt die Beschriftungszeichenfolge in der Zelle automatisch in Anführungszeichen ein, doch diese Anführungszeichen werden im Fenster **Shape-Daten** nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17bef-108">The application automatically encloses the Label string in quotation marks in the cell, but the quotation marks are not displayed in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="17bef-109">Wenn kein Beschriftungstext gefunden wird, Visio der Zeilenname (Prop.Row) im **Fenster Shape Data angezeigt.**</span><span class="sxs-lookup"><span data-stu-id="17bef-109">If no label text is found, Visio displays the row name (Prop.Row) in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="17bef-110">Verwenden Sie zum Erhalten eines Verweises auf die Zelle Label anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="17bef-110">To get a reference to the Label cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="17bef-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="17bef-111">Cell name:</span></span>  <br/> |<span data-ttu-id="17bef-112">Prop. *Name*  . Bezeichnung, an der Prop.  *Name*  ist der Zeilenname</span><span class="sxs-lookup"><span data-stu-id="17bef-112">Prop. *Name*  .Label where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="17bef-113">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Label nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="17bef-113">To get a reference to the Label cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="17bef-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="17bef-114">Section index:</span></span>  <br/> |<span data-ttu-id="17bef-115">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="17bef-115">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="17bef-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="17bef-116">Row index:</span></span>  <br/> |<span data-ttu-id="17bef-117">**visRowProp**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="17bef-117">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="17bef-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="17bef-118">Cell index:</span></span>  <br/> |<span data-ttu-id="17bef-119">**visCustPropsLabel**</span><span class="sxs-lookup"><span data-stu-id="17bef-119">**visCustPropsLabel**</span></span> <br/> |
   

