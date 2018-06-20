---
title: Zelle "LangID" (Abschnitt "Annotation")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60048
localization_priority: Normal
ms.assetid: b6f5ea5e-b350-0817-d631-f059b9b95c23
description: Gibt die Sprache an, in der der Kommentar eingegeben wurde.
ms.openlocfilehash: 0de5ed8136a3fb1bbdca9fea0ebb5894e62cf907
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797278"
---
# <a name="langid-cell-annotation-section"></a><span data-ttu-id="c7f0a-103">Zelle "LangID" (Abschnitt "Annotation")</span><span class="sxs-lookup"><span data-stu-id="c7f0a-103">LangID Cell (Annotation Section)</span></span>

<span data-ttu-id="c7f0a-104">Gibt die Sprache an, in der der Kommentar eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c7f0a-104">Indicates the language in which the comment was entered.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c7f0a-105">Diese Zelle wird für Kommentare zur Überwachung nur, wenn eine VSD-Datei in Microsoft Visio 2013 öffnen oder eine vsdx-Datei im VSD-Format speichern.</span><span class="sxs-lookup"><span data-stu-id="c7f0a-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="c7f0a-106">Es wird nicht zum Nachverfolgen von Kommentaren in .vsdx Dokumente in Visio 2013 verwendet.</span><span class="sxs-lookup"><span data-stu-id="c7f0a-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c7f0a-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c7f0a-107">Remarks</span></span>

<span data-ttu-id="c7f0a-108">Dieser Wert ist die Gebietsschema-ID (LCID) der Sprache, die auf der Sprachleiste aktiv ist, wenn der Kommentar eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c7f0a-108">This value is the locale ID (LCID) of the language that is active on the language bar when the comment was entered.</span></span> <span data-ttu-id="c7f0a-109">Eine Liste der von Microsoft Office-Anwendungen unterstützten Sprachen finden Sie unter dem Thema [DocLangID](doclangid-cell-document-properties-section.md) Zelle (Abschnitt "Document Properties").</span><span class="sxs-lookup"><span data-stu-id="c7f0a-109">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="c7f0a-110">Wenn Sie einen Verweis auf die Zelle LangID nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c7f0a-110">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c7f0a-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="c7f0a-111">Cell name:</span></span>  <br/> | <span data-ttu-id="c7f0a-112">Annotation.LangID [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c7f0a-112">Annotation.LangID[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c7f0a-113">Wenn Sie einen Verweis auf die Zelle LangID aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="c7f0a-113">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c7f0a-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="c7f0a-114">Section index:</span></span>  <br/> |<span data-ttu-id="c7f0a-115">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="c7f0a-115">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="c7f0a-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c7f0a-116">Row index:</span></span>  <br/> |<span data-ttu-id="c7f0a-117">**VisRowAnnotation** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c7f0a-117">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c7f0a-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="c7f0a-118">Cell index:</span></span>  <br/> |<span data-ttu-id="c7f0a-119">**visAnnotationLangID**</span><span class="sxs-lookup"><span data-stu-id="c7f0a-119">**visAnnotationLangID**</span></span> <br/> |
   

