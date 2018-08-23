---
title: DeinitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeinitMapiUtil
api_type:
- HeaderDef
ms.assetid: e0b8dc9c-cc46-4d27-9497-7a55a0bfdff5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e84dbc0976f5c438a7e0b5fd7cddcbf1c0659f40
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574797"
---
# <a name="deinitmapiutil"></a><span data-ttu-id="222d8-103">DeinitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="222d8-103">DeinitMapiUtil</span></span>

  
  
<span data-ttu-id="222d8-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="222d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="222d8-105">Hilfsfunktionen explizit aufgerufen werden, von der Funktion [ScInitMapiUtil](scinitmapiutil.md) oder implizit von der Funktion ["MAPIInitialize"](mapiinitialize.md) frei.</span><span class="sxs-lookup"><span data-stu-id="222d8-105">Releases utility functions called explicitly by the [ScInitMapiUtil](scinitmapiutil.md) function or implicitly by the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="222d8-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="222d8-106">Header file:</span></span>  <br/> |<span data-ttu-id="222d8-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="222d8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="222d8-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="222d8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="222d8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="222d8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="222d8-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="222d8-110">Called by:</span></span>  <br/> |<span data-ttu-id="222d8-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="222d8-111">Client applications</span></span>  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a><span data-ttu-id="222d8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="222d8-112">Parameters</span></span>

<span data-ttu-id="222d8-113">Keine</span><span class="sxs-lookup"><span data-stu-id="222d8-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="222d8-114">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="222d8-114">Return value</span></span>

<span data-ttu-id="222d8-115">Keine</span><span class="sxs-lookup"><span data-stu-id="222d8-115">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="222d8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="222d8-116">Remarks</span></span>

<span data-ttu-id="222d8-117">Die **DeinitMapiUtil** -Funktion Freigabefunktionen mit [ScInitMapiUtil](scinitmapiutil.md) oder ["MAPIInitialize"](mapiinitialize.md)initialisiert.</span><span class="sxs-lookup"><span data-stu-id="222d8-117">The **DeinitMapiUtil** function release functions initialized with [ScInitMapiUtil](scinitmapiutil.md) or [MAPIInitialize](mapiinitialize.md).</span></span> 
  
<span data-ttu-id="222d8-118">Nach Abschluss der Verwendung der Funktionen von **ScInitMapiUtil** aufgerufen, muss **DeinitMapiUtil** explizit aufgerufen werden, um diese freigeben.</span><span class="sxs-lookup"><span data-stu-id="222d8-118">When use of the functions called by **ScInitMapiUtil** is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="222d8-119">Im Gegensatz dazu ruft [MAPIUninitialize](mapiuninitialize.md) implizit **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="222d8-119">In contrast, [MAPIUninitialize](mapiuninitialize.md) implicitly calls **DeinitMapiUtil**.</span></span> 
  

