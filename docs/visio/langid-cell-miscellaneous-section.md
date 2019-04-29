---
title: Zelle "LangID" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60051
localization_priority: Normal
ms.assetid: 815e0df8-5ebf-ef1b-d620-bce8abb69f1a
description: Gibt die Sprache an, in der Zellformeln erstellt wurden.
ms.openlocfilehash: e1e5b92f01e97bc63003a4b195c159a50f61e77b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406675"
---
# <a name="langid-cell-miscellaneous-section"></a><span data-ttu-id="6f373-103">Zelle "LangID" (Abschnitt "Miscellaneous")</span><span class="sxs-lookup"><span data-stu-id="6f373-103">LangID Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="6f373-104">Gibt die Sprache an, in der Zellformeln erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="6f373-104">Indicates the language in which cell formulas were created.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6f373-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f373-105">Remarks</span></span>

<span data-ttu-id="6f373-106">Eine Liste der von Microsoft Office-Anwendungen unterstützten Sprachen finden Sie im Thema [Zelle "DocLangID"](doclangid-cell-document-properties-section.md) (Abschnitt "Document Properties").</span><span class="sxs-lookup"><span data-stu-id="6f373-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="6f373-107">Wenn Sie einen Verweis auf die Zelle "lang" aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6f373-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6f373-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6f373-108">Cell name:</span></span>  <br/> | <span data-ttu-id="6f373-109">LangID</span><span class="sxs-lookup"><span data-stu-id="6f373-109">LangID</span></span>  <br/> |
   
<span data-ttu-id="6f373-110">Wenn Sie einen Verweis auf die Zelle lang aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="6f373-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6f373-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6f373-111">Section index:</span></span>  <br/> |<span data-ttu-id="6f373-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6f373-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6f373-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6f373-113">Row index:</span></span>  <br/> |<span data-ttu-id="6f373-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="6f373-114">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="6f373-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6f373-115">Cell index:</span></span>  <br/> |<span data-ttu-id="6f373-116">**visObjLangID**</span><span class="sxs-lookup"><span data-stu-id="6f373-116">**visObjLangID**</span></span> <br/> |
   

