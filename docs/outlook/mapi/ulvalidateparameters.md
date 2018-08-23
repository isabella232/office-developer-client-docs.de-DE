---
title: UlValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParameters
api_type:
- COM
ms.assetid: fb9050c9-5797-44f0-8bf5-6264f4e6d7c3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 297b5a516f8275b236092f9f385afcb673c95de0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585241"
---
# <a name="ulvalidateparameters"></a><span data-ttu-id="b425e-103">UlValidateParameters</span><span class="sxs-lookup"><span data-stu-id="b425e-103">UlValidateParameters</span></span>

  
  
<span data-ttu-id="b425e-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b425e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b425e-105">Ruft eine interne Funktion, um zu überprüfen, dass die Parameter-Clientanwendungen zu Dienstanbietern und MAPI-vergangen sind.</span><span class="sxs-lookup"><span data-stu-id="b425e-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b425e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b425e-106">Header file:</span></span>  <br/> |<span data-ttu-id="b425e-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="b425e-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="b425e-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="b425e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b425e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b425e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b425e-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="b425e-110">Called by:</span></span>  <br/> |<span data-ttu-id="b425e-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="b425e-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="b425e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b425e-112">Parameters</span></span>

 <span data-ttu-id="b425e-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="b425e-113">_eMethod_</span></span>
  
> <span data-ttu-id="b425e-114">[in] Gibt den-Enumeration zurück, die-Methode, um zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b425e-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="b425e-115">_Erster_</span><span class="sxs-lookup"><span data-stu-id="b425e-115">_First_</span></span>
  
> <span data-ttu-id="b425e-116">[in] Zeiger auf das erste Argument im Stapel.</span><span class="sxs-lookup"><span data-stu-id="b425e-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b425e-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="b425e-117">Return value</span></span>

<span data-ttu-id="b425e-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="b425e-118">S_OK</span></span> 
  
> <span data-ttu-id="b425e-119">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="b425e-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="b425e-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="b425e-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="b425e-121">Ein Fehler unerwartete oder unbekannten Ursprungs verhindert den Abschluss des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="b425e-121">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b425e-122">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="b425e-122">Remarks</span></span>

<span data-ttu-id="b425e-123">Das Makro **UlValidateParameters** wurde durch das Makro [UlValidateParms](ulvalidateparms.md) ersetzt.</span><span class="sxs-lookup"><span data-stu-id="b425e-123">The **UlValidateParameters** macro has been superseded by the [UlValidateParms](ulvalidateparms.md) macro.</span></span> <span data-ttu-id="b425e-124">**UlValidateParameters** funktioniert nicht ordnungsgemäß auf RISC-Plattformen und wird nun auf diese zu kompilieren verhindert.</span><span class="sxs-lookup"><span data-stu-id="b425e-124">**UlValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="b425e-125">Immer noch kompiliert und auf Intel-Plattformen ordnungsgemäß funktioniert, aber **UlValidateParms** wird auf allen Plattformen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="b425e-125">It still compiles and works correctly on Intel platforms, but **UlValidateParms** is recommended on all platforms.</span></span> 
  

