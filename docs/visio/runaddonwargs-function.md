---
title: RUNADDONWARGS-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251493
localization_priority: Normal
ms.assetid: c154413f-c366-a66b-94e3-ed71ad23f325
description: Führt eine Zeichenfolge aus und übergibt die Befehlszeilenargumente als Zeichenfolge an das Programm.
ms.openlocfilehash: bc05a4480438875c348373059f57bf04f82c9eca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408705"
---
# <a name="runaddonwargs-function"></a><span data-ttu-id="5b1a2-103">RUNADDONWARGS Function</span><span class="sxs-lookup"><span data-stu-id="5b1a2-103">RUNADDONWARGS Function</span></span>

<span data-ttu-id="5b1a2-104">Führt eine _Zeichenfolge_ aus und übergibt die Befehlszeilen _Argumente_ als Zeichenfolge an das Programm.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-104">Runs  _string_ and passes the command line  _arguments_ to the program as a string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5b1a2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b1a2-105">Syntax</span></span>

<span data-ttu-id="5b1a2-106">RUNADDONWARGS ("\* \* *String* \* *", "* \* *Argumente* \* \*")</span><span class="sxs-lookup"><span data-stu-id="5b1a2-106">RUNADDONWARGS(" \*\* *string* \*\* "," \*\* *arguments* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5b1a2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b1a2-107">Parameters</span></span>

|<span data-ttu-id="5b1a2-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="5b1a2-108">**Name**</span></span>|<span data-ttu-id="5b1a2-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="5b1a2-109">**Required/Optional**</span></span>|<span data-ttu-id="5b1a2-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="5b1a2-110">**Data Type**</span></span>|<span data-ttu-id="5b1a2-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b1a2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5b1a2-112">_Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="5b1a2-112">_string_</span></span> <br/> |<span data-ttu-id="5b1a2-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5b1a2-113">Required</span></span>  <br/> |<span data-ttu-id="5b1a2-114">**String**</span><span class="sxs-lookup"><span data-stu-id="5b1a2-114">**String**</span></span> <br/> | <span data-ttu-id="5b1a2-115">Der Name eines Add-Ons.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-115">The name of an add-on.</span></span>  <br/> |
| <span data-ttu-id="5b1a2-116">_Argumente_</span><span class="sxs-lookup"><span data-stu-id="5b1a2-116">_arguments_</span></span> <br/> |<span data-ttu-id="5b1a2-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5b1a2-117">Required</span></span>  <br/> |<span data-ttu-id="5b1a2-118">**String**</span><span class="sxs-lookup"><span data-stu-id="5b1a2-118">**String**</span></span> <br/> |<span data-ttu-id="5b1a2-119">Die an das Programm zu übergebenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-119">Arguments to pass to your program.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b1a2-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b1a2-120">Remarks</span></span>

<span data-ttu-id="5b1a2-121">In der Praxis sollten _argumente_ 50 oder weniger Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-121">In practice,  _arguments_ should be 50 or fewer characters.</span></span> <span data-ttu-id="5b1a2-122">Verwenden Sie die RUNADDONWARGS-Funktion, um ein Programm wie ein Add-on an eine Zelle zu binden, beispielsweise an eine Aktions-oder Ereignis Zelle.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-122">Use the RUNADDONWARGS function to bind a program, such as an add-on, to a cell, for example, to an Action or Events cell.</span></span> 
  
<span data-ttu-id="5b1a2-123">Mit der RUNADDONWARGS-Funktion können nur Add-Ons ausgeführt werden, die Elemente der **Addons**-Auflistung der Anwendung sind.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-123">The RUNADDONWARGS function can only run add-ons that are members of the application's **Addons** collection.</span></span> <span data-ttu-id="5b1a2-124">Add-Ons in dieser Auflistung müssen EXE- oder VSL-Dateien sein, für die Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="5b1a2-124">To be present in that collection, an add-on must be an EXE file or VSL file that is:</span></span> 
  
- <span data-ttu-id="5b1a2-125">Sie müssen im Verzeichnis **Startup** bzw. **Addons** der Anwendung installiert sein.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-125">Installed in the application's **Startup** or **Addons** path.</span></span> 
    
- <span data-ttu-id="5b1a2-126">Sie müssen programmgesteuert mithilfe der **Add**-Methode der **Addons**-Auflistung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-126">Added programmatically by using the **Add** method of the **Addons** collection.</span></span> 
    
<span data-ttu-id="5b1a2-127">Weitere Informationen zum Ausführen von Code in Visio finden Sie unter [Informationen zu Sicherheitseinstellungen und zum Ausführen von Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in dieser ShapeSheet-Referenz.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-127">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="5b1a2-p103">In früheren Versionen von Visio wird diese Funktion in der Form _RUNADDONWARGS geschrieben. In Visio, Version 4.0 und höher, können beide Schreibweisen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-p103">In earlier versions of Visio, this function appears as _RUNADDONWARGS. Visio application versions 4.0 and later accept either style.</span></span>
  
## <a name="example"></a><span data-ttu-id="5b1a2-130">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5b1a2-130">Example</span></span>

<span data-ttu-id="5b1a2-131">RUNADDONWARGS ("GRAPHMKR. EXE ","/GraphMaker = Stack ")</span><span class="sxs-lookup"><span data-stu-id="5b1a2-131">RUNADDONWARGS("GRAPHMKR.EXE","/GraphMaker=Stack")</span></span> 
  
<span data-ttu-id="5b1a2-132">Führt das Add-On Graphmkr.exe aus und übergibt diesem das Argument /GraphMaker=Stack.</span><span class="sxs-lookup"><span data-stu-id="5b1a2-132">Launches the add-on Graphmkr.exe and passes it the argument /GraphMaker=Stack.</span></span> 
  

