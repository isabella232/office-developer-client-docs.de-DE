---
title: Zelle "LangID" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033771
localization_priority: Normal
ms.assetid: 6bd2781a-d4e7-136f-8996-62ebc5f890ab
description: Gibt die Sprache an, in der der Wert für die Shape-Daten eingegeben wurde.
ms.openlocfilehash: c5a0cca5f71bc5520337ad2bdcf354a2b4affe92
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420325"
---
# <a name="langid-cell-shape-data-section"></a><span data-ttu-id="cc49f-103">Zelle "LangID" (Abschnitt "Shape Data")</span><span class="sxs-lookup"><span data-stu-id="cc49f-103">LangID Cell (Shape Data Section)</span></span>

<span data-ttu-id="cc49f-104">Gibt die Sprache an, in der der Wert für die Shape-Daten eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="cc49f-104">Indicates the language in which the shape data value was entered.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cc49f-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cc49f-105">Remarks</span></span>

<span data-ttu-id="cc49f-106">Eine Liste der von Microsoft Office System-Anwendungen unterstützten Sprachen finden Sie unter [Zelle "DocLangID"](doclangid-cell-document-properties-section.md) (Abschnitt "Document Properties").</span><span class="sxs-lookup"><span data-stu-id="cc49f-106">For a list of languages supported by Microsoft Office System applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section).</span></span> 
  
<span data-ttu-id="cc49f-107">Um einen Verweis auf die LangID-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="cc49f-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cc49f-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="cc49f-108">Cell name:</span></span>  <br/> | <span data-ttu-id="cc49f-109">Prop.  *Name*  . LangID, wobei Prop.  *Name*  ist der Zeilenname</span><span class="sxs-lookup"><span data-stu-id="cc49f-109">Prop.  *name*  .LangID            where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="cc49f-110">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LangID-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="cc49f-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cc49f-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="cc49f-111">Section index:</span></span>  <br/> |<span data-ttu-id="cc49f-112">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="cc49f-112">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="cc49f-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="cc49f-113">Row index:</span></span>  <br/> |<span data-ttu-id="cc49f-114">**visRowProp**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="cc49f-114">**visRowProp** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="cc49f-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="cc49f-115">Cell index:</span></span>  <br/> |<span data-ttu-id="cc49f-116">**visCustPropsLangID**</span><span class="sxs-lookup"><span data-stu-id="cc49f-116">**visCustPropsLangID**</span></span> <br/> |
   

