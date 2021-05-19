---
title: Zelle "LangID" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033769
localization_priority: Normal
ms.assetid: c68289b8-ef45-9e1e-12ae-6613587e4990
description: Gibt die Sprache an, in der der Text eingegeben wurde.
ms.openlocfilehash: e1f244d6d8e31201576a9a88ace9701814b0e0a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419282"
---
# <a name="langid-cell-character-section"></a><span data-ttu-id="84aab-103">Zelle "LangID" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="84aab-103">LangID Cell (Character Section)</span></span>

<span data-ttu-id="84aab-104">Gibt die Sprache an, in der der Text eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="84aab-104">Indicates the language in which the text was entered.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="84aab-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="84aab-105">Remarks</span></span>

<span data-ttu-id="84aab-106">Eine Liste der von Microsoft Office-Anwendungen unterstützten Sprachen finden Sie im Thema [Zelle "DocLangID"](doclangid-cell-document-properties-section.md) (Abschnitt "Document Properties").</span><span class="sxs-lookup"><span data-stu-id="84aab-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="84aab-107">Um einen Verweis auf die LangID-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="84aab-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="84aab-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="84aab-108">Cell name:</span></span>  <br/> | <span data-ttu-id="84aab-109">Char.LangID[  *i*  ] wobei  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="84aab-109">Char.LangID[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="84aab-110">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LangID-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="84aab-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="84aab-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="84aab-111">Section index:</span></span>  <br/> |<span data-ttu-id="84aab-112">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="84aab-112">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="84aab-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="84aab-113">Row index:</span></span>  <br/> |<span data-ttu-id="84aab-114">**visRowCharacter**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="84aab-114">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="84aab-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="84aab-115">Cell index:</span></span>  <br/> |<span data-ttu-id="84aab-116">**visCharacterLangID**</span><span class="sxs-lookup"><span data-stu-id="84aab-116">**visCharacterLangID**</span></span> <br/> |
   

