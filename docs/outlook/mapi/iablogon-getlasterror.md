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
ms.openlocfilehash: bead72ab2b394634217c9ae219a03a98752ef27d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791958"
---
# <a name="iablogongetlasterror"></a><span data-ttu-id="2c19e-103">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="2c19e-103">IABLogon::GetLastError</span></span>

  
  
<span data-ttu-id="2c19e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2c19e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2c19e-105">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Address Book Anbieterfehler enthält.</span><span class="sxs-lookup"><span data-stu-id="2c19e-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="2c19e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c19e-106">Parameters</span></span>

 <span data-ttu-id="2c19e-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="2c19e-107">_hResult_</span></span>
  
> <span data-ttu-id="2c19e-108">[in] Ein Handle für den Fehlerwert in der vorherigen Aufruf-Methode generiert.</span><span class="sxs-lookup"><span data-stu-id="2c19e-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="2c19e-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2c19e-109">_ulFlags_</span></span>
  
> <span data-ttu-id="2c19e-110">[in] Eine Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="2c19e-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="2c19e-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="2c19e-111">The following flag can be set:</span></span>
    
<span data-ttu-id="2c19e-112">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2c19e-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2c19e-113">Die Zeichenfolgen in der **MAPIERROR** -Struktur zurückgegeben, die im Parameter _LppMAPIError_ sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="2c19e-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="2c19e-114">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="2c19e-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="2c19e-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="2c19e-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="2c19e-116">[out] Ein Zeiger auf einen Zeiger auf eine **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="2c19e-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="2c19e-117">Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn der Anbieter eine **MAPIERROR** -Struktur mit den entsprechenden Informationen angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="2c19e-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2c19e-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c19e-118">Return value</span></span>

<span data-ttu-id="2c19e-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="2c19e-119">S_OK</span></span> 
  
> <span data-ttu-id="2c19e-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="2c19e-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="2c19e-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="2c19e-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="2c19e-122">Entweder die Option MAPI_UNICODE festgelegt wurde und die Adressbuchanbieter unterstützt keine Unicode oder Parameter MAPI_UNICODE wurde nicht festgelegt und die Adressbuchanbieter unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="2c19e-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2c19e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c19e-123">Remarks</span></span>

<span data-ttu-id="2c19e-124">Von adressbuchanbietern implementierte implementieren die **GetLastError** -Methode, um Informationen zu einem vorherigen Methodenaufruf angeben, die nicht erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="2c19e-124">Address book providers implement the **GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="2c19e-125">Anrufer können die Benutzer einschließlich der Daten aus der **MAPIERROR** -Struktur in einem Dialogfeld mit ausführlichen Informationen zu dem Fehler bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2c19e-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2c19e-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="2c19e-126">Notes to callers</span></span>

<span data-ttu-id="2c19e-127">Sie können die **MAPIERROR** -Struktur, die auf den der _LppMAPIError_ -Parameter, wenn die Adressbuchanbieter die Struktur bereitstellt und **GetLastError** gibt S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="2c19e-127">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if the address book provider supplies the structure and only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="2c19e-128">In einigen Fällen kann die Adressbuchanbieter was letzten Fehlers wurde oder nicht mehr zu dem Fehler gemeldet wurde nicht ermitteln.</span><span class="sxs-lookup"><span data-stu-id="2c19e-128">Sometimes the address book provider cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="2c19e-129">In diesem Fall gibt die Adressbuchanbieter einen Zeiger auf NULL in _LppMAPIError_ stattdessen.</span><span class="sxs-lookup"><span data-stu-id="2c19e-129">In this situation, the address book provider returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="2c19e-130">Weitere Informationen über die **GetLastError** -Methode finden Sie unter [Extended MAPI-Fehler](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="2c19e-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2c19e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c19e-131">See also</span></span>



[<span data-ttu-id="2c19e-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="2c19e-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="2c19e-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2c19e-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="2c19e-134">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2c19e-134">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

