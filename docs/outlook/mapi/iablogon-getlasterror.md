---
title: IABLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetLastError
api_type:
- COM
ms.assetid: d157e29e-7731-4e47-b4a7-e8622b223001
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 311299b00143667b3f2fb22bd7be6c3a52c7141d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434249"
---
# <a name="iablogongetlasterror"></a><span data-ttu-id="6afce-103">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="6afce-103">IABLogon::GetLastError</span></span>

  
  
<span data-ttu-id="6afce-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6afce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6afce-105">Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Adressbuchanbieterfehler enthält.</span><span class="sxs-lookup"><span data-stu-id="6afce-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="6afce-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6afce-106">Parameters</span></span>

 <span data-ttu-id="6afce-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="6afce-107">_hResult_</span></span>
  
> <span data-ttu-id="6afce-108">[in] Ein Handle zum Fehlerwert, der im vorherigen Methodenaufruf generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6afce-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="6afce-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6afce-109">_ulFlags_</span></span>
  
> <span data-ttu-id="6afce-110">[in] Eine Bitmaske mit Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="6afce-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="6afce-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="6afce-111">The following flag can be set:</span></span>
    
<span data-ttu-id="6afce-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6afce-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6afce-113">Die Zeichenfolgen in der **MAPIERROR-Struktur,** die im  _lppMAPIError-Parameter_ zurückgegeben wird, sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="6afce-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="6afce-114">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="6afce-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="6afce-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="6afce-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="6afce-116">[out] Ein Zeiger auf einen Zeiger auf eine **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="6afce-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="6afce-117">Der  _lppMAPIError-Parameter_ kann auf NULL festgelegt werden, wenn der Anbieter keine **MAPIERROR-Struktur** mit entsprechenden Informationen angeben kann.</span><span class="sxs-lookup"><span data-stu-id="6afce-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6afce-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6afce-118">Return value</span></span>

<span data-ttu-id="6afce-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="6afce-119">S_OK</span></span> 
  
> <span data-ttu-id="6afce-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="6afce-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="6afce-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="6afce-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="6afce-122">Entweder wurde MAPI_UNICODE-Flag festgelegt, und der Adressbuchanbieter unterstützt Unicode nicht, oder MAPI_UNICODE nicht festgelegt, und der Adressbuchanbieter unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="6afce-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6afce-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6afce-123">Remarks</span></span>

<span data-ttu-id="6afce-124">Adressbuchanbieter implementieren die **GetLastError-Methode,** um Informationen zu einem vorherigen Methodenaufruf zu liefern, der fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="6afce-124">Address book providers implement the **GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="6afce-125">Anrufer können ihren Benutzern detaillierte Informationen zu dem Fehler bereitstellen, indem sie die Daten aus der **MAPIERROR-Struktur** in ein Dialogfeld eingeben.</span><span class="sxs-lookup"><span data-stu-id="6afce-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6afce-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="6afce-126">Notes to callers</span></span>

<span data-ttu-id="6afce-127">Sie können die **MAPIERROR-Struktur verwenden,** auf die der  _lppMAPIError-Parameter_ verweist, wenn der Adressbuchanbieter die Struktur angibt und nur, wenn **GetLastError** S_OK.</span><span class="sxs-lookup"><span data-stu-id="6afce-127">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if the address book provider supplies the structure and only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="6afce-128">Manchmal kann der Adressbuchanbieter nicht ermitteln, was der letzte Fehler war oder hat nichts mehr über den Fehler zu melden.</span><span class="sxs-lookup"><span data-stu-id="6afce-128">Sometimes the address book provider cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="6afce-129">In diesem Fall gibt der Adressbuchanbieter stattdessen einen Zeiger auf NULL in  _lppMAPIError_ zurück.</span><span class="sxs-lookup"><span data-stu-id="6afce-129">In this situation, the address book provider returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="6afce-130">Weitere Informationen zur **GetLastError-Methode** finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="6afce-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6afce-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6afce-131">See also</span></span>



[<span data-ttu-id="6afce-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="6afce-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="6afce-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="6afce-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="6afce-134">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6afce-134">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

