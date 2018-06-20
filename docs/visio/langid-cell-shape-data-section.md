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
ms.openlocfilehash: 696c42483390509474eb82bd8cc0046beee345e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797297"
---
# <a name="langid-cell-shape-data-section"></a><span data-ttu-id="1cbc4-103">LangID Cell (Shape Data Section)</span><span class="sxs-lookup"><span data-stu-id="1cbc4-103">LangID Cell (Shape Data Section)</span></span>

<span data-ttu-id="1cbc4-104">Gibt die Sprache an, in der der Wert für die Shape-Daten eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="1cbc4-104">Indicates the language in which the shape data value was entered.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1cbc4-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1cbc4-105">Remarks</span></span>

<span data-ttu-id="1cbc4-106">Eine Liste der von Microsoft Office System-Anwendungen unterstützten Sprachen finden Sie unter der Zelle ["DocLangID](doclangid-cell-document-properties-section.md) " (Abschnitt "Document Properties").</span><span class="sxs-lookup"><span data-stu-id="1cbc4-106">For a list of languages supported by Microsoft Office System applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section).</span></span> 
  
<span data-ttu-id="1cbc4-107">Wenn Sie einen Verweis auf die Zelle LangID nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1cbc4-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1cbc4-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="1cbc4-108">Cell name:</span></span>  <br/> | <span data-ttu-id="1cbc4-109">Eigenschaft.  *Name* . LangID wobei Prop.  *Name* ist der Zeilenname</span><span class="sxs-lookup"><span data-stu-id="1cbc4-109">Prop.  *name*  .LangID            where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="1cbc4-110">Wenn Sie einen Verweis auf die Zelle LangID aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="1cbc4-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1cbc4-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="1cbc4-111">Section index:</span></span>  <br/> |<span data-ttu-id="1cbc4-112">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="1cbc4-112">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="1cbc4-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="1cbc4-113">Row index:</span></span>  <br/> |<span data-ttu-id="1cbc4-114">**VisRowProp** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1cbc4-114">**visRowProp** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="1cbc4-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="1cbc4-115">Cell index:</span></span>  <br/> |<span data-ttu-id="1cbc4-116">**visCustPropsLangID**</span><span class="sxs-lookup"><span data-stu-id="1cbc4-116">**visCustPropsLangID**</span></span> <br/> |
   

