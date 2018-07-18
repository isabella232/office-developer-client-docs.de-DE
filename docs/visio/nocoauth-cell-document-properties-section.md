---
title: NoCoauth Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Legt fest, ob ein Dokument gespeichert, die auf einem Microsoft SharePoint 2013-Server oder Microsoft OneDrive von mehreren Autoren gleichzeitig in einer Sitzung beim Entwicklersupport bearbeitet werden kann.
ms.openlocfilehash: a20c3a5aa1392e0e6c3bef124f536b91b9642f47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797548"
---
# <a name="nocoauth-cell-document-properties-section"></a><span data-ttu-id="267e3-103">NoCoauth Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="267e3-103">NoCoauth Cell (Document Properties Section)</span></span>

<span data-ttu-id="267e3-104">Legt fest, ob ein Dokument gespeichert, die auf einem Microsoft SharePoint 2013-Server oder Microsoft OneDrive von mehreren Autoren gleichzeitig in einer Sitzung beim Entwicklersupport bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="267e3-104">Sets whether a document stored on a Microsoft SharePoint 2013 server or Microsoft OneDrive can be edited by multiple authors simultaneously in a coauthoring session.</span></span>
  
|<span data-ttu-id="267e3-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="267e3-105">**Value**</span></span>|<span data-ttu-id="267e3-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="267e3-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="267e3-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="267e3-107">TRUE</span></span>  <br/> |<span data-ttu-id="267e3-108">Das Dokument kann nicht Mitautor werden und für die Bearbeitung beim Öffnen gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="267e3-108">The document cannot be coauthored and is locked for editing when open.</span></span>  <br/> |
|<span data-ttu-id="267e3-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="267e3-109">FALSE</span></span>  <br/> |<span data-ttu-id="267e3-110">Das Dokument kann Mitautor sein.</span><span class="sxs-lookup"><span data-stu-id="267e3-110">The document can be coauthored.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="267e3-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="267e3-111">Remarks</span></span>

<span data-ttu-id="267e3-112">Wenn Sie einen Verweis auf die Zelle **NoCoauth** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="267e3-112">To get a reference to the **NoCoauth** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="267e3-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="267e3-113">Cell name:</span></span>  <br/> | <span data-ttu-id="267e3-114">NoCoauth</span><span class="sxs-lookup"><span data-stu-id="267e3-114">NoCoauth</span></span>  <br/> |
   
<span data-ttu-id="267e3-115">Wenn Sie einen Verweis auf die Zelle **NoCoauth** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="267e3-115">To get a reference to the **NoCoauth** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="267e3-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="267e3-116">Section index:</span></span>  <br/> |<span data-ttu-id="267e3-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="267e3-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="267e3-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="267e3-118">Row index:</span></span>  <br/> |<span data-ttu-id="267e3-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="267e3-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="267e3-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="267e3-120">Cell index:</span></span>  <br/> |<span data-ttu-id="267e3-121">**visDocNoCoauth**</span><span class="sxs-lookup"><span data-stu-id="267e3-121">**visDocNoCoauth**</span></span> <br/> |
   

