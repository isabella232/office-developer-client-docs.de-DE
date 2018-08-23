---
title: CheckParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParameters
api_type:
- COM
ms.assetid: ba33866a-c9c4-454a-9549-72455c61ee97
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f01d0ad7e7e6b1ad7a5e4c4838bb46ca143e0968
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567055"
---
# <a name="checkparameters"></a><span data-ttu-id="9a76d-103">CheckParameters</span><span class="sxs-lookup"><span data-stu-id="9a76d-103">CheckParameters</span></span>

  
  
<span data-ttu-id="9a76d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a76d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a76d-105">Ruft eine interne Funktion zum debugging Parameter für Webdienstmethoden aufgerufen von MAPI-Anbieter zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9a76d-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9a76d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9a76d-106">Header file:</span></span>  <br/> |<span data-ttu-id="9a76d-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="9a76d-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="9a76d-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="9a76d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9a76d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9a76d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9a76d-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="9a76d-110">Called by:</span></span>  <br/> |<span data-ttu-id="9a76d-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="9a76d-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="9a76d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a76d-112">Parameters</span></span>

 <span data-ttu-id="9a76d-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="9a76d-113">_eMethod_</span></span>
  
> <span data-ttu-id="9a76d-114">[in] Gibt den-Enumeration zurück, die-Methode, um zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9a76d-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="9a76d-115">_Erster_</span><span class="sxs-lookup"><span data-stu-id="9a76d-115">_First_</span></span>
  
> <span data-ttu-id="9a76d-116">[in] Zeiger auf das erste Argument im Stapel.</span><span class="sxs-lookup"><span data-stu-id="9a76d-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9a76d-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="9a76d-117">Return value</span></span>

<span data-ttu-id="9a76d-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="9a76d-118">S_OK</span></span> 
  
> <span data-ttu-id="9a76d-119">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9a76d-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9a76d-120">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="9a76d-120">Remarks</span></span>

<span data-ttu-id="9a76d-121">Das Makro **CheckParameters** wurde durch das Makro [CheckParms](checkparms.md) ersetzt.</span><span class="sxs-lookup"><span data-stu-id="9a76d-121">The **CheckParameters** macro has been superseded by the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="9a76d-122">**CheckParms** wird auf allen Plattformen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="9a76d-122">**CheckParms** is recommended on all platforms.</span></span> 
  

