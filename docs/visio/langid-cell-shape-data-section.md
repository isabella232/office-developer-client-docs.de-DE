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
# <a name="langid-cell-shape-data-section"></a><span data-ttu-id="d7e0c-103">Zelle "LangID" (Abschnitt "Shape Data")</span><span class="sxs-lookup"><span data-stu-id="d7e0c-103">LangID Cell (Shape Data Section)</span></span>

<span data-ttu-id="d7e0c-104">Gibt die Sprache an, in der der Wert für die Shape-Daten eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="d7e0c-104">Indicates the language in which the shape data value was entered.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d7e0c-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7e0c-105">Remarks</span></span>

<span data-ttu-id="d7e0c-106">Eine Liste der von Microsoft Office System-Anwendungen unterstützten Sprachen finden Sie unter [Zelle "DocLangID"](doclangid-cell-document-properties-section.md) (Abschnitt "Document Properties").</span><span class="sxs-lookup"><span data-stu-id="d7e0c-106">For a list of languages supported by Microsoft Office System applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section).</span></span> 
  
<span data-ttu-id="d7e0c-107">Wenn Sie einen Verweis auf die Zelle "lang" aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d7e0c-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d7e0c-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d7e0c-108">Cell name:</span></span>  <br/> | <span data-ttu-id="d7e0c-109">Prop.  *Name* . Lang-Punkt, wobei Prop.  *Name* ist der Name der Zeile</span><span class="sxs-lookup"><span data-stu-id="d7e0c-109">Prop.  *name*  .LangID            where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="d7e0c-110">Wenn Sie einen Verweis auf die Zelle lang aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="d7e0c-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d7e0c-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d7e0c-111">Section index:</span></span>  <br/> |<span data-ttu-id="d7e0c-112">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="d7e0c-112">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="d7e0c-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d7e0c-113">Row index:</span></span>  <br/> |<span data-ttu-id="d7e0c-114">**visRowProp** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d7e0c-114">**visRowProp** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d7e0c-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d7e0c-115">Cell index:</span></span>  <br/> |<span data-ttu-id="d7e0c-116">**visCustPropsLangID**</span><span class="sxs-lookup"><span data-stu-id="d7e0c-116">**visCustPropsLangID**</span></span> <br/> |
   

