---
title: MapStorageSCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MapStorageSCode
api_type:
- COM
ms.assetid: f686a2bc-aba5-4ea3-9963-76d0e96eab50
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ab892513348541ec9de3c071a12268afa9337465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793170"
---
# <a name="mapstoragescode"></a><span data-ttu-id="c1b9d-103">MapStorageSCode</span><span class="sxs-lookup"><span data-stu-id="c1b9d-103">MapStorageSCode</span></span>

  
  
<span data-ttu-id="c1b9d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c1b9d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c1b9d-105">Maps SCODE zurück-Wert aus einem OLE-Speicher-Objekt in einen Typ HRESULT.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-105">Maps an SCODE return value from an OLE storage object to an HRESULT type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c1b9d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c1b9d-106">Header file:</span></span>  <br/> |<span data-ttu-id="c1b9d-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="c1b9d-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="c1b9d-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="c1b9d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c1b9d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c1b9d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c1b9d-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="c1b9d-110">Called by:</span></span>  <br/> |<span data-ttu-id="c1b9d-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="c1b9d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a><span data-ttu-id="c1b9d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1b9d-112">Parameters</span></span>

 <span data-ttu-id="c1b9d-113">_StgSCode_</span><span class="sxs-lookup"><span data-stu-id="c1b9d-113">_StgSCode_</span></span>
  
> <span data-ttu-id="c1b9d-114">[in] MAPI SCODE zurück-Wert, aus einem OLE-Speicher-Objekt ein HRESULT-Wert zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-114">[in] MAPI SCODE return value from an OLE storage object to be mapped to a HRESULT value.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c1b9d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1b9d-115">Return value</span></span>

<span data-ttu-id="c1b9d-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="c1b9d-116">S_OK</span></span> 
  
> <span data-ttu-id="c1b9d-117">Der Aufruf erfolgreich ausgeführt und der erwartete Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-117">The call succeeded and returned the expected value.</span></span>
    
<span data-ttu-id="c1b9d-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="c1b9d-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="c1b9d-119">Die Funktion kann einen übereinstimmenden Wert nicht finden.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-119">The function cannot find a matching value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c1b9d-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1b9d-120">Remarks</span></span>

<span data-ttu-id="c1b9d-121">MAPI bietet die **MapStorageSCode** -Funktion für die interne Verwendung von MAPI-Komponenten, die ihre Nachricht Implementierungen für die Nachricht DLL basieren soll.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-121">MAPI provides the **MapStorageSCode** function for the internal use of MAPI components that base their message implementations on the message DLL.</span></span> <span data-ttu-id="c1b9d-122">Da diese Komponenten OLE Remotespeicher selbst zu öffnen, müssen sie zuordnen Fehlerwerte für Probleme mit OLE-Speicher an ein HRESULT-Wert zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-122">Because these components open OLE storage themselves, they must be able to map error values returned for problems with OLE storage to an HRESULT value.</span></span> 
  
<span data-ttu-id="c1b9d-123">Weitere Informationen finden Sie unter [Strukturierte Storage](structured-storage-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="c1b9d-123">For more information, see [Structured Storage](structured-storage-in-mapi.md).</span></span> 
  

