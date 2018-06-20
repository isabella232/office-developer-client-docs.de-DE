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
description: Öffnet eine HTML-Hilfedatei mit dem Schlüsselwort angegeben, in das Feld Suchen.
ms.openlocfilehash: 4671b18333bdae953c487662cd880849233df7f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797145"
---
# <a name="help-function"></a><span data-ttu-id="17774-103">HELP Function</span><span class="sxs-lookup"><span data-stu-id="17774-103">HELP Function</span></span>

<span data-ttu-id="17774-104">Öffnet eine HTML-Hilfedatei mit dem angegebenen *Schlüsselwort* im Feld **Suchen** .</span><span class="sxs-lookup"><span data-stu-id="17774-104">Opens an HTML Help file with the specifed  *keyword*  in the **Search** box.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="17774-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="17774-105">Syntax</span></span>

<span data-ttu-id="17774-106">Hilfe ("** *filename.chm!keyword* **")</span><span class="sxs-lookup"><span data-stu-id="17774-106">HELP(" ** *filename.chm!keyword* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="17774-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="17774-107">Parameters</span></span>

|<span data-ttu-id="17774-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="17774-108">**Name**</span></span>|<span data-ttu-id="17774-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="17774-109">**Required/Optional**</span></span>|<span data-ttu-id="17774-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="17774-110">**Data Type**</span></span>|<span data-ttu-id="17774-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="17774-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="17774-112">_filename.chm!Keyword_</span><span class="sxs-lookup"><span data-stu-id="17774-112">_filename.chm!keyword_</span></span> <br/> |<span data-ttu-id="17774-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="17774-113">Required</span></span>  <br/> |<span data-ttu-id="17774-114">**String**</span><span class="sxs-lookup"><span data-stu-id="17774-114">**String**</span></span> <br/> | <span data-ttu-id="17774-115">Der Name der Hilfedatei und das Stichwort, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="17774-115">The filename of the Help file and the keyword to search for.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17774-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17774-116">Remarks</span></span>

<span data-ttu-id="17774-117">Wenn kein *Keyword* angegeben wurde, wird die HELP-Funktion die Inhaltsübersicht der Hilfedatei geöffnet.</span><span class="sxs-lookup"><span data-stu-id="17774-117">If no  *keyword*  is specified, the HELP function opens the contents page of the Help file.</span></span> 
  
## <a name="example"></a><span data-ttu-id="17774-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="17774-118">Example</span></span>

<span data-ttu-id="17774-119">Help("Visio.chm!ShapeSheet")</span><span class="sxs-lookup"><span data-stu-id="17774-119">HELP("visio.chm!shapesheet")</span></span> 
  
<span data-ttu-id="17774-120">Öffnet die Visio-Hilfedatei und zeigt eine Liste der Themen zum Stichwort "Shapesheet" an.</span><span class="sxs-lookup"><span data-stu-id="17774-120">Opens the Visio Help file and displays a list of the topic(s) whose keyword is "shapesheet."</span></span> 
  

