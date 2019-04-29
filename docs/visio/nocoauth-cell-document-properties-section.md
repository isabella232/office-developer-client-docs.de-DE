---
title: NoCoauth Cell (Document Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Legt fest, ob ein auf einem Microsoft SharePoint 2013-Server oder einem Microsoft OneDrive gespeichertes Dokument von mehreren Autoren gleichzeitig in einer gemeinsamen Sitzung bearbeitet werden kann.
ms.openlocfilehash: a76e2d3b2c3cf6e99e37596b016f448b0be56fd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420514"
---
# <a name="nocoauth-cell-document-properties-section"></a><span data-ttu-id="17d7d-103">NoCoauth Cell (Document Properties section)</span><span class="sxs-lookup"><span data-stu-id="17d7d-103">NoCoauth Cell (Document Properties Section)</span></span>

<span data-ttu-id="17d7d-104">Legt fest, ob ein auf einem Microsoft SharePoint 2013-Server oder einem Microsoft OneDrive gespeichertes Dokument von mehreren Autoren gleichzeitig in einer gemeinsamen Sitzung bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="17d7d-104">Sets whether a document stored on a Microsoft SharePoint 2013 server or Microsoft OneDrive can be edited by multiple authors simultaneously in a coauthoring session.</span></span>
  
|<span data-ttu-id="17d7d-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="17d7d-105">**Value**</span></span>|<span data-ttu-id="17d7d-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="17d7d-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="17d7d-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="17d7d-107">TRUE</span></span>  <br/> |<span data-ttu-id="17d7d-108">Das Dokument kann nicht gemeinsam erstellt werden und ist für die Bearbeitung gesperrt, wenn es geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="17d7d-108">The document cannot be coauthored and is locked for editing when open.</span></span>  <br/> |
|<span data-ttu-id="17d7d-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="17d7d-109">FALSE</span></span>  <br/> |<span data-ttu-id="17d7d-110">Das Dokument kann gemeinsam erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="17d7d-110">The document can be coauthored.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17d7d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17d7d-111">Remarks</span></span>

<span data-ttu-id="17d7d-112">Wenn Sie einen Verweis auf die Zelle **NoCoauth** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="17d7d-112">To get a reference to the **NoCoauth** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17d7d-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="17d7d-113">Cell name:</span></span>  <br/> | <span data-ttu-id="17d7d-114">NoCoauth</span><span class="sxs-lookup"><span data-stu-id="17d7d-114">NoCoauth</span></span>  <br/> |
   
<span data-ttu-id="17d7d-115">Wenn Sie einen Verweis auf die Zelle **NoCoauth** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="17d7d-115">To get a reference to the **NoCoauth** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17d7d-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="17d7d-116">Section index:</span></span>  <br/> |<span data-ttu-id="17d7d-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="17d7d-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="17d7d-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="17d7d-118">Row index:</span></span>  <br/> |<span data-ttu-id="17d7d-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="17d7d-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="17d7d-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="17d7d-120">Cell index:</span></span>  <br/> |<span data-ttu-id="17d7d-121">**visDocNoCoauth**</span><span class="sxs-lookup"><span data-stu-id="17d7d-121">**visDocNoCoauth**</span></span> <br/> |
   

