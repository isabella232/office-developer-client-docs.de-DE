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
description: Öffnet ein Microsoft Visio Dokument, wenn es noch nicht geöffnet ist, und aktiviert das Dokumentfenster.
ms.openlocfilehash: 5a89a658e560d144007ec19796de82b9949bea82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419576"
---
# <a name="openfile-function"></a><span data-ttu-id="a0273-103">OPENFILE Function</span><span class="sxs-lookup"><span data-stu-id="a0273-103">OPENFILE Function</span></span>

<span data-ttu-id="a0273-104">Öffnet ein Microsoft Visio Dokument, wenn es noch nicht geöffnet ist, und aktiviert das Dokumentfenster.</span><span class="sxs-lookup"><span data-stu-id="a0273-104">Opens a Microsoft Visio document, if it's not already open, and activates the document window.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a0273-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0273-105">Syntax</span></span>

 <span data-ttu-id="a0273-106">**OPENFILE**( _"filename"_)</span><span class="sxs-lookup"><span data-stu-id="a0273-106">**OPENFILE**( _"filename"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="a0273-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0273-107">Parameters</span></span>

|<span data-ttu-id="a0273-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="a0273-108">**Name**</span></span>|<span data-ttu-id="a0273-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="a0273-109">**Required/Optional**</span></span>|<span data-ttu-id="a0273-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a0273-110">**Data Type**</span></span>|<span data-ttu-id="a0273-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a0273-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a0273-112">_filename_</span><span class="sxs-lookup"><span data-stu-id="a0273-112">_filename_</span></span> <br/> |<span data-ttu-id="a0273-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a0273-113">Required</span></span>  <br/> |<span data-ttu-id="a0273-114">**String**</span><span class="sxs-lookup"><span data-stu-id="a0273-114">**String**</span></span> <br/> |<span data-ttu-id="a0273-115">Der Name der Datei, einschließlich des Dateipfads, den Sie öffnen möchten.</span><span class="sxs-lookup"><span data-stu-id="a0273-115">The name of the file, including file path, you want to open.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0273-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a0273-116">Remarks</span></span>

<span data-ttu-id="a0273-p101">Es können mehrere OPENFILE-Funktionsaufrufe in eine Warteschlange gestellt und in einer ausgewerteten Reihenfolge ausgeführt werden. Falls das aktuelle Visio-Dokument für die visuelle Bearbeitung innerhalb einer anderen Anwendung geöffnet ist, wird eine neue Visio-Instanz mit dem angeforderten Dateinamen gestartet.</span><span class="sxs-lookup"><span data-stu-id="a0273-p101">Multiple OPENFILE function calls are queued and executed in order of evaluation. If the current Visio document is activated for visual (in-place) editing, a new Visio instance is launched with the requested file name.</span></span> 
  
<span data-ttu-id="a0273-119">Diese Funktion gibt immer FALSE zurück.</span><span class="sxs-lookup"><span data-stu-id="a0273-119">This function always returns FALSE.</span></span> 
  
<span data-ttu-id="a0273-p102">In früheren Visio-Versionen wird diese Funktion in der Form _OPENFILE angezeigt. Die Visio-Versionen 4.0 und höher nehmen beide Schreibweisen an.</span><span class="sxs-lookup"><span data-stu-id="a0273-p102">In earlier versions of the Visio application, this function appears as _OPENFILE. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a0273-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a0273-122">Example</span></span>

 `OPENFILE("C:/MyFile.vsdx")`
  
<span data-ttu-id="a0273-123">Öffnet die angegebene Datei "MyFile.vsdx" in einem neuen Fenster oder aktiviert das Fenster, wenn die Datei bereits geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="a0273-123">Opens the specified file "MyFile.vsdx" in a new window, or activates the window if the file is already open.</span></span> 
  

