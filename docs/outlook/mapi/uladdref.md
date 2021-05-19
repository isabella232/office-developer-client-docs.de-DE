---
title: UlAddRef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlAddRef
api_type:
- COM
ms.assetid: 9b897cbc-90b2-4c60-b5f1-dc78e7e7952d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f9e55153830dbe41a2b4a48454157c900d96cf90
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432835"
---
# <a name="uladdref"></a><span data-ttu-id="3f692-103">UlAddRef</span><span class="sxs-lookup"><span data-stu-id="3f692-103">UlAddRef</span></span>

  
  
<span data-ttu-id="3f692-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f692-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f692-105">Bietet eine alternative Möglichkeit zum Aufrufen der OLE-Methode **IUnknown::AddRef**.</span><span class="sxs-lookup"><span data-stu-id="3f692-105">Provides an alternative way to invoke the OLE method **IUnknown::AddRef**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3f692-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="3f692-106">Header file:</span></span>  <br/> |<span data-ttu-id="3f692-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3f692-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3f692-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="3f692-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3f692-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3f692-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3f692-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="3f692-110">Called by:</span></span>  <br/> |<span data-ttu-id="3f692-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="3f692-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="3f692-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f692-112">Parameters</span></span>

 <span data-ttu-id="3f692-113">_punk_</span><span class="sxs-lookup"><span data-stu-id="3f692-113">_punk_</span></span>
  
> <span data-ttu-id="3f692-114">[in] Zeiger auf eine Schnittstelle, die von der **IUnknown-Schnittstelle** abgeleitet ist, d. h. auf eine beliebige MAPI-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3f692-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3f692-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f692-115">Return value</span></span>

<span data-ttu-id="3f692-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="3f692-116">S_OK</span></span> 
  
> <span data-ttu-id="3f692-117">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="3f692-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="3f692-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="3f692-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="3f692-119">Ein Fehler mit unerwartetem oder unbekanntem Ursprung verhinderte den Abschluss des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="3f692-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3f692-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3f692-120">Remarks</span></span>

 <span data-ttu-id="3f692-121">**UlAddRef gibt** den von der **IUnknown::AddRef-Methode** zurückgegebenen Wert zurück, der der neue Wert der Referenzanzahl für die Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="3f692-121">**UlAddRef** returns the value returned by the **IUnknown::AddRef** method, which is the new value of the reference count for the interface.</span></span> <span data-ttu-id="3f692-122">Der Wert ist ungleich Null.</span><span class="sxs-lookup"><span data-stu-id="3f692-122">The value is nonzero.</span></span> 
  
<span data-ttu-id="3f692-123">Weitere Informationen zu **IUnknown::AddRef** finden Sie unter [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span><span class="sxs-lookup"><span data-stu-id="3f692-123">For more information about **IUnknown::AddRef**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

