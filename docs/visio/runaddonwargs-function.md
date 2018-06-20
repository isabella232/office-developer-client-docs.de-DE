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
description: Führt String aus und übergibt die Befehlszeilenargumente für das Programm als Zeichenfolge.
ms.openlocfilehash: 7bc05a0cbf32550d1e39bee39bec83101882cf19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797962"
---
# <a name="runaddonwargs-function"></a><span data-ttu-id="1bbdc-103">RUNADDONWARGS-Funktion</span><span class="sxs-lookup"><span data-stu-id="1bbdc-103">RUNADDONWARGS Function</span></span>

<span data-ttu-id="1bbdc-104">Führt _String_ aus und übergibt die Befehlszeile _Argumente_ an die Anwendung als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1bbdc-104">Runs  _string_ and passes the command line  _arguments_ to the program as a string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1bbdc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bbdc-105">Syntax</span></span>

<span data-ttu-id="1bbdc-106">RUNADDONWARGS ("** *Zeichenfolge* **","** *Argumente* **")</span><span class="sxs-lookup"><span data-stu-id="1bbdc-106">RUNADDONWARGS(" ** *string* ** "," ** *arguments* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1bbdc-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bbdc-107">Parameters</span></span>

|<span data-ttu-id="1bbdc-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="1bbdc-108">**Name**</span></span>|<span data-ttu-id="1bbdc-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="1bbdc-109">**Required/Optional**</span></span>|<span data-ttu-id="1bbdc-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="1bbdc-110">**Data Type**</span></span>|<span data-ttu-id="1bbdc-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1bbdc-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1bbdc-112">_string_</span><span class="sxs-lookup"><span data-stu-id="1bbdc-112">_string_</span></span> <br/> |<span data-ttu-id="1bbdc-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="1bbdc-113">Required</span></span>  <br/> |<span data-ttu-id="1bbdc-114">**String**</span><span class="sxs-lookup"><span data-stu-id="1bbdc-114">**String**</span></span> <br/> | <span data-ttu-id="1bbdc-115">Der Name eines Add-Ons.</span><span class="sxs-lookup"><span data-stu-id="1bbdc-115">The name of an add-on.</span></span>  <br/> |
| <span data-ttu-id="1bbdc-116">_Argumente_</span><span class="sxs-lookup"><span data-stu-id="1bbdc-116">_arguments_</span></span> <br/> |<span data-ttu-id="1bbdc-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="1bbdc-117">Required</span></span>  <br/> |<span data-ttu-id="1bbdc-118">**String**</span><span class="sxs-lookup"><span data-stu-id="1bbdc-118">**String**</span></span> <br/> |<span data-ttu-id="1bbdc-119">Die an das Programm zu übergebenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="1bbdc-119">Arguments to pass to your program.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1bbdc-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1bbdc-120">Remarks</span></span>

<span data-ttu-id="1bbdc-121">In der Praxis sollten für _Arguments_ 50 oder weniger Zeichen werden.</span><span class="sxs-lookup"><span data-stu-id="1bbdc-121">In practice,  _arguments_ should be 50 or fewer characters.</span></span> <span data-ttu-id="1bbdc-122">Verwenden der RUNADDONWARGS-Funktion ein Programm, wie ein Add-on, auf eine Zelle, eine Aktion oder Ereignisse Zelle einzubinden.</span><span class="sxs-lookup"><span data-stu-id="1bbdc-122">Use the RUNADDONWARGS function to bind a program, such as an add-on, to a cell, for example, to an Action or Events cell.</span></span> 
  
<span data-ttu-id="1bbdc-123">RUNADDONWARGS-Funktion kann nur Add-ons ausgeführt werden, die Mitglied der Anwendung **Addons** -Auflistung sind.</span><span class="sxs-lookup"><span data-stu-id="1bbdc-123">The RUNADDONWARGS function can only run add-ons that are members of the application's **Addons** collection.</span></span> <span data-ttu-id="1bbdc-124">In der Auflistung vorhanden sind, muss ein Add-on, eine EXE-Datei oder VSL-Datei, ist:</span><span class="sxs-lookup"><span data-stu-id="1bbdc-124">To be present in that collection, an add-on must be an EXE file or VSL file that is:</span></span> 
  
- <span data-ttu-id="1bbdc-125">In der Anwendung **beim Starten** oder **Addons** Pfad installiert.</span><span class="sxs-lookup"><span data-stu-id="1bbdc-125">Installed in the application's **Startup** or **Addons** path.</span></span> 
    
- <span data-ttu-id="1bbdc-126">Programmgesteuert hinzugefügt mithilfe der **Add** -Methode der **Addons** -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="1bbdc-126">Added programmatically by using the **Add** method of the **Addons** collection.</span></span> 
    
<span data-ttu-id="1bbdc-127">Weitere Informationen zum Ausführen von Code in Visio finden Sie unter [Informationen zu Sicherheitseinstellungen und Ausführen von Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in dieser ShapeSheet-Referenz.</span><span class="sxs-lookup"><span data-stu-id="1bbdc-127">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="1bbdc-p103">In früheren Versionen von Visio wird diese Funktion in der Form _RUNADDONWARGS geschrieben. In Visio, Version 4.0 und höher, können beide Schreibweisen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1bbdc-p103">In earlier versions of Visio, this function appears as _RUNADDONWARGS. Visio application versions 4.0 and later accept either style.</span></span>
  
## <a name="example"></a><span data-ttu-id="1bbdc-130">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1bbdc-130">Example</span></span>

<span data-ttu-id="1bbdc-131">RUNADDONWARGS ("GRAPHMKR. EXE-Datei"," / GraphMaker = Stack ")</span><span class="sxs-lookup"><span data-stu-id="1bbdc-131">RUNADDONWARGS("GRAPHMKR.EXE","/GraphMaker=Stack")</span></span> 
  
<span data-ttu-id="1bbdc-132">Führt das Add-On Graphmkr.exe aus und übergibt diesem das Argument /GraphMaker=Stack.</span><span class="sxs-lookup"><span data-stu-id="1bbdc-132">Launches the add-on Graphmkr.exe and passes it the argument /GraphMaker=Stack.</span></span> 
  

