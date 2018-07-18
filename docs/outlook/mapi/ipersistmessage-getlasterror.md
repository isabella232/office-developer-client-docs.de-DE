---
title: IPersistMessageGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetLastError
api_type:
- COM
ms.assetid: 32cc3a1f-1310-4788-b0f4-93c1e4940f37
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 16f091f4d9527cd82ebc1d1eadee2fb55b481929
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792738"
---
# <a name="ipersistmessagegetlasterror"></a><span data-ttu-id="619ca-103">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="619ca-103">IPersistMessage::GetLastError</span></span>

  
  
<span data-ttu-id="619ca-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="619ca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="619ca-105">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen zu den vorherigen Fehler in das Form-Objekt enthält, zurück.</span><span class="sxs-lookup"><span data-stu-id="619ca-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="619ca-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="619ca-106">Parameters</span></span>

 <span data-ttu-id="619ca-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="619ca-107">_hResult_</span></span>
  
> <span data-ttu-id="619ca-108">[in] Ein HRESULT-Datentyp, der den im vorherigen Methodenaufruf generierten Fehlerwert enthält.</span><span class="sxs-lookup"><span data-stu-id="619ca-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="619ca-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="619ca-109">_ulFlags_</span></span>
  
> <span data-ttu-id="619ca-110">[in] Eine Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="619ca-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="619ca-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="619ca-111">The following flag can be set:</span></span>
    
<span data-ttu-id="619ca-112">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="619ca-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="619ca-113">Die Zeichenfolgen in der [MAPIERROR](mapierror.md) -Struktur zurückgegeben, die im Parameter _LppMAPIError_ sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="619ca-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="619ca-114">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="619ca-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="619ca-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="619ca-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="619ca-116">[out] Ein Zeiger auf einen Zeiger auf eine **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="619ca-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="619ca-117">Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn das Formular für eine Struktur **MAPIERROR** entsprechende Informationen angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="619ca-117">The  _lppMAPIError_ parameter can be set to NULL if the form cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="619ca-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="619ca-118">Return value</span></span>

<span data-ttu-id="619ca-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="619ca-119">S_OK</span></span> 
  
> <span data-ttu-id="619ca-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="619ca-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="619ca-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="619ca-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="619ca-122">Entweder die Option MAPI_UNICODE festgelegt wurde und die Adressbuchanbieter unterstützt keine Unicode oder Parameter MAPI_UNICODE wurde nicht festgelegt und die Adressbuchanbieter unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="619ca-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="619ca-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="619ca-123">Remarks</span></span>

<span data-ttu-id="619ca-124">Formular-Objekte implementieren Sie die **IPersistMessage::GetLastError** -Methode, um Informationen zu einem vorherigen Methodenaufruf angeben, die nicht erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="619ca-124">Form objects implement the **IPersistMessage::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="619ca-125">Formular Viewer können die Benutzer detaillierte Informationen zu dem Fehler einschließlich der Daten aus der [MAPIERROR](mapierror.md) -Struktur in einem Dialogfeld bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="619ca-125">Form viewers can provide their users with detailed information about the error by including the data from the [MAPIERROR](mapierror.md) structure in a dialog box.</span></span> 
  
<span data-ttu-id="619ca-126">Ein Aufruf von **GetLastError** wirkt sich nicht auf den Status des Formulars aus.</span><span class="sxs-lookup"><span data-stu-id="619ca-126">A call to **GetLastError** does not affect the state of the form.</span></span> <span data-ttu-id="619ca-127">Wenn **GetLastError** zurückgegeben wird, bleibt das Formular in den Status, die vor der Anruf getätigt wurde.</span><span class="sxs-lookup"><span data-stu-id="619ca-127">When **GetLastError** returns, the form remains in the state that it was in before the call was made.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="619ca-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="619ca-128">Notes to callers</span></span>

<span data-ttu-id="619ca-129">Sie können die Struktur **MAPIERROR** verwenden, wenn das Formular ein einziges, der durch den Parameter _LppMAPIError bereitstellt_ auf gezeigt wird, nur, wenn **GetLastError** gibt S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="619ca-129">You can use the **MAPIERROR** structure, if the form supplies one, that is pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="619ca-130">In einigen Fällen kann nicht das Formular zu bestimmen, was letzten Fehlers wurde oder nicht mehr zu dem Fehler gemeldet wurde.</span><span class="sxs-lookup"><span data-stu-id="619ca-130">Sometimes the form cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="619ca-131">In diesem Fall gibt das Formular einen Zeiger auf NULL in _LppMAPIError_ stattdessen.</span><span class="sxs-lookup"><span data-stu-id="619ca-131">In this situation, the form returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="619ca-132">Weitere Informationen über die **GetLastError** -Methode finden Sie unter [Extended MAPI-Fehler](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="619ca-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="619ca-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="619ca-133">See also</span></span>



[<span data-ttu-id="619ca-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="619ca-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="619ca-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="619ca-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="619ca-136">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="619ca-136">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

