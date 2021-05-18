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
ms.openlocfilehash: b3b2cba3d0a04f75ef2d87f0ee8dcd1f8115e15e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422257"
---
# <a name="langid-cell-annotation-section"></a><span data-ttu-id="13abd-103">Zelle "LangID" (Abschnitt "Annotation")</span><span class="sxs-lookup"><span data-stu-id="13abd-103">LangID Cell (Annotation Section)</span></span>

<span data-ttu-id="13abd-104">Gibt die Sprache an, in der der Kommentar eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="13abd-104">Indicates the language in which the comment was entered.</span></span>
  
> [!NOTE]
> <span data-ttu-id="13abd-105">Diese Zelle wird nur zum Nachverfolgen von Kommentaren verwendet, wenn Sie eine VSD-Datei in Microsoft Visio 2013 öffnen oder eine VSDX-Datei im VSD-Dateiformat speichern.</span><span class="sxs-lookup"><span data-stu-id="13abd-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="13abd-106">Es wird nicht zum Nachverfolgen von Kommentaren in VSDX-Dokumenten in Visio 2013 verwendet.</span><span class="sxs-lookup"><span data-stu-id="13abd-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="13abd-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="13abd-107">Remarks</span></span>

<span data-ttu-id="13abd-p102">Bei diesem Wert handelt es sich um den Gebietsschemabezeichner der Sprache, die bei Eingabe des Kommentars auf der Eingabegebietsschema-Leiste aktiv ist. Eine Liste der von Microsoft Office-Anwendungen unterstützten Sprachen finden Sie unter [Zelle "DocLangID"](doclangid-cell-document-properties-section.md) (Abschnitt "Document Properties").</span><span class="sxs-lookup"><span data-stu-id="13abd-p102">This value is the locale ID (LCID) of the language that is active on the language bar when the comment was entered. For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="13abd-110">Um einen Verweis auf die LangID-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="13abd-110">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="13abd-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="13abd-111">Cell name:</span></span>  <br/> | <span data-ttu-id="13abd-112">Annotation.LangID[  *i*  ] wobei  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="13abd-112">Annotation.LangID[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="13abd-113">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LangID-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="13abd-113">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="13abd-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="13abd-114">Section index:</span></span>  <br/> |<span data-ttu-id="13abd-115">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="13abd-115">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="13abd-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="13abd-116">Row index:</span></span>  <br/> |<span data-ttu-id="13abd-117">**visRowAnnotation**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="13abd-117">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="13abd-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="13abd-118">Cell index:</span></span>  <br/> |<span data-ttu-id="13abd-119">**visAnnotationLangID**</span><span class="sxs-lookup"><span data-stu-id="13abd-119">**visAnnotationLangID**</span></span> <br/> |
   

