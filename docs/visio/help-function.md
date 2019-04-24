---
title: HELP-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251436
localization_priority: Normal
ms.assetid: 5b358c38-6ed1-3fbe-c1d1-1a56ebbaa870
description: Öffnet eine HTML-Hilfedatei mit dem Schlüsselwort angegebene im Suchfeld.
ms.openlocfilehash: 639d10bf489d1ad09aef1522d3cbc743bbe66f6f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329974"
---
# <a name="help-function"></a><span data-ttu-id="b8f7c-103">HELP-Funktion</span><span class="sxs-lookup"><span data-stu-id="b8f7c-103">HELP Function</span></span>

<span data-ttu-id="b8f7c-104">Öffnet eine HTML-Hilfedatei mit dem *Schlüsselwort* angegebene im **Suchfeld** .</span><span class="sxs-lookup"><span data-stu-id="b8f7c-104">Opens an HTML Help file with the specifed  *keyword*  in the **Search** box.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b8f7c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8f7c-105">Syntax</span></span>

<span data-ttu-id="b8f7c-106">HELP ("\* \* *filename. chm!-Schlüsselwort* \* \*")</span><span class="sxs-lookup"><span data-stu-id="b8f7c-106">HELP(" \*\* *filename.chm!keyword* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b8f7c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8f7c-107">Parameters</span></span>

|<span data-ttu-id="b8f7c-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="b8f7c-108">**Name**</span></span>|<span data-ttu-id="b8f7c-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="b8f7c-109">**Required/Optional**</span></span>|<span data-ttu-id="b8f7c-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="b8f7c-110">**Data Type**</span></span>|<span data-ttu-id="b8f7c-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b8f7c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b8f7c-112">_filename. chm!-Schlüsselwort_</span><span class="sxs-lookup"><span data-stu-id="b8f7c-112">_filename.chm!keyword_</span></span> <br/> |<span data-ttu-id="b8f7c-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b8f7c-113">Required</span></span>  <br/> |<span data-ttu-id="b8f7c-114">**String**</span><span class="sxs-lookup"><span data-stu-id="b8f7c-114">**String**</span></span> <br/> | <span data-ttu-id="b8f7c-115">Der Name der Hilfedatei und das Stichwort, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8f7c-115">The filename of the Help file and the keyword to search for.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8f7c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8f7c-116">Remarks</span></span>

<span data-ttu-id="b8f7c-117">Wenn kein *Schlüsselwort* angegeben wird, wird die Seite Inhalt der Hilfedatei geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b8f7c-117">If no  *keyword*  is specified, the HELP function opens the contents page of the Help file.</span></span> 
  
## <a name="example"></a><span data-ttu-id="b8f7c-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b8f7c-118">Example</span></span>

<span data-ttu-id="b8f7c-119">Hilfe ("Visio. chm! ShapeSheet")</span><span class="sxs-lookup"><span data-stu-id="b8f7c-119">HELP("visio.chm!shapesheet")</span></span> 
  
<span data-ttu-id="b8f7c-120">Öffnet die Visio-Hilfedatei und zeigt eine Liste der Themen zum Stichwort "Shapesheet" an.</span><span class="sxs-lookup"><span data-stu-id="b8f7c-120">Opens the Visio Help file and displays a list of the topic(s) whose keyword is "shapesheet."</span></span> 
  

