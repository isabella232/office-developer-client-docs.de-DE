---
title: OPENFILE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251471
localization_priority: Normal
ms.assetid: ff59ab04-a589-cf9e-db3b-20658a7dffdc
description: Öffnet ein Microsoft Visio-Dokument, wenn es noch nicht geöffnet ist, und das Dokumentfenster aktiviert.
ms.openlocfilehash: 7d4778fc4641465e88303b8515365172fd8be0ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797565"
---
# <a name="openfile-function"></a><span data-ttu-id="b40b6-103">OPENFILE-Funktion</span><span class="sxs-lookup"><span data-stu-id="b40b6-103">OPENFILE Function</span></span>

<span data-ttu-id="b40b6-104">Öffnet ein Microsoft Visio-Dokument, wenn es noch nicht geöffnet ist, und das Dokumentfenster aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b40b6-104">Opens a Microsoft Visio document, if it's not already open, and activates the document window.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b40b6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b40b6-105">Syntax</span></span>

 <span data-ttu-id="b40b6-106">**OPENFILE** ( _"Filename"_)</span><span class="sxs-lookup"><span data-stu-id="b40b6-106">**OPENFILE**( _"filename"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="b40b6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b40b6-107">Parameters</span></span>

|<span data-ttu-id="b40b6-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="b40b6-108">**Name**</span></span>|<span data-ttu-id="b40b6-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="b40b6-109">**Required/Optional**</span></span>|<span data-ttu-id="b40b6-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="b40b6-110">**Data Type**</span></span>|<span data-ttu-id="b40b6-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b40b6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b40b6-112">_Dateiname_</span><span class="sxs-lookup"><span data-stu-id="b40b6-112">_filename_</span></span> <br/> |<span data-ttu-id="b40b6-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b40b6-113">Required</span></span>  <br/> |<span data-ttu-id="b40b6-114">**String**</span><span class="sxs-lookup"><span data-stu-id="b40b6-114">**String**</span></span> <br/> |<span data-ttu-id="b40b6-115">Der Name der Datei, einschließlich Dateipfad, den Sie öffnen möchten.</span><span class="sxs-lookup"><span data-stu-id="b40b6-115">The name of the file, including file path, you want to open.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b40b6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b40b6-116">Remarks</span></span>

<span data-ttu-id="b40b6-p101">Es können mehrere OPENFILE-Funktionsaufrufe in eine Warteschlange gestellt und in einer ausgewerteten Reihenfolge ausgeführt werden. Falls das aktuelle Visio-Dokument für die visuelle Bearbeitung innerhalb einer anderen Anwendung geöffnet ist, wird eine neue Visio-Instanz mit dem angeforderten Dateinamen gestartet.</span><span class="sxs-lookup"><span data-stu-id="b40b6-p101">Multiple OPENFILE function calls are queued and executed in order of evaluation. If the current Visio document is activated for visual (in-place) editing, a new Visio instance is launched with the requested file name.</span></span> 
  
<span data-ttu-id="b40b6-119">Diese Funktion gibt immer FALSE zurück.</span><span class="sxs-lookup"><span data-stu-id="b40b6-119">This function always returns FALSE.</span></span> 
  
<span data-ttu-id="b40b6-p102">In früheren Visio-Versionen wird diese Funktion in der Form _OPENFILE angezeigt. Die Visio-Versionen 4.0 und höher nehmen beide Schreibweisen an.</span><span class="sxs-lookup"><span data-stu-id="b40b6-p102">In earlier versions of the Visio application, this function appears as _OPENFILE. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example"></a><span data-ttu-id="b40b6-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b40b6-122">Example</span></span>

 `OPENFILE("C:/MyFile.vsdx")`
  
<span data-ttu-id="b40b6-123">Öffnet die angegebene Datei "MyFile.vsdx" in einem neuen Fenster oder aktiviert das Fenster, wenn die Datei bereits geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="b40b6-123">Opens the specified file "MyFile.vsdx" in a new window, or activates the window if the file is already open.</span></span> 
  

