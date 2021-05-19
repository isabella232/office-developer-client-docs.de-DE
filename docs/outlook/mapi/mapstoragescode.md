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
ms.openlocfilehash: 5dce5de820c07e1fa7b25b87d87993a30961b3f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416524"
---
# <a name="mapstoragescode"></a><span data-ttu-id="b5c88-103">MapStorageSCode</span><span class="sxs-lookup"><span data-stu-id="b5c88-103">MapStorageSCode</span></span>

  
  
<span data-ttu-id="b5c88-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5c88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5c88-105">Karten einen SCODE-Rückgabewert aus einem OLE-Speicherobjekt in einen HRESULT-Typ.</span><span class="sxs-lookup"><span data-stu-id="b5c88-105">Maps an SCODE return value from an OLE storage object to an HRESULT type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b5c88-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b5c88-106">Header file:</span></span>  <br/> |<span data-ttu-id="b5c88-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="b5c88-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="b5c88-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="b5c88-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b5c88-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b5c88-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b5c88-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="b5c88-110">Called by:</span></span>  <br/> |<span data-ttu-id="b5c88-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="b5c88-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a><span data-ttu-id="b5c88-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5c88-112">Parameters</span></span>

 <span data-ttu-id="b5c88-113">_StgSCode_</span><span class="sxs-lookup"><span data-stu-id="b5c88-113">_StgSCode_</span></span>
  
> <span data-ttu-id="b5c88-114">[in] MAPI-SCODE-Rückgabewert aus einem OLE-Speicherobjekt, das einem HRESULT-Wert zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b5c88-114">[in] MAPI SCODE return value from an OLE storage object to be mapped to a HRESULT value.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b5c88-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5c88-115">Return value</span></span>

<span data-ttu-id="b5c88-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="b5c88-116">S_OK</span></span> 
  
> <span data-ttu-id="b5c88-117">Der Aufruf ist erfolgreich und hat den erwarteten Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b5c88-117">The call succeeded and returned the expected value.</span></span>
    
<span data-ttu-id="b5c88-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="b5c88-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="b5c88-119">Die Funktion kann keinen übereinstimmenden Wert finden.</span><span class="sxs-lookup"><span data-stu-id="b5c88-119">The function cannot find a matching value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b5c88-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b5c88-120">Remarks</span></span>

<span data-ttu-id="b5c88-121">MAPI stellt die **MapStorageSCode-Funktion** für die interne Verwendung von MAPI-Komponenten zur Verfügung, die ihre Nachrichtenimplementierung auf der Nachrichten-DLL erstellen.</span><span class="sxs-lookup"><span data-stu-id="b5c88-121">MAPI provides the **MapStorageSCode** function for the internal use of MAPI components that base their message implementations on the message DLL.</span></span> <span data-ttu-id="b5c88-122">Da diese Komponenten den OLE-Speicher selbst öffnen, müssen sie Fehlerwerte, die für Probleme mit dem OLE-Speicher zurückgegeben werden, einem HRESULT-Wert zuordnungen können.</span><span class="sxs-lookup"><span data-stu-id="b5c88-122">Because these components open OLE storage themselves, they must be able to map error values returned for problems with OLE storage to an HRESULT value.</span></span> 
  
<span data-ttu-id="b5c88-123">Weitere Informationen finden Sie unter [Structured Storage](structured-storage-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="b5c88-123">For more information, see [Structured Storage](structured-storage-in-mapi.md).</span></span> 
  

