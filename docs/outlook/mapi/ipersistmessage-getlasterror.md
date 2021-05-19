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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2189a39e115236e6c2ec9de8a263ce3982d8b8e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426709"
---
# <a name="ipersistmessagegetlasterror"></a><span data-ttu-id="b4852-103">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b4852-103">IPersistMessage::GetLastError</span></span>

  
  
<span data-ttu-id="b4852-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4852-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4852-105">Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler im Formularobjekt enthält.</span><span class="sxs-lookup"><span data-stu-id="b4852-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="b4852-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4852-106">Parameters</span></span>

 <span data-ttu-id="b4852-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="b4852-107">_hResult_</span></span>
  
> <span data-ttu-id="b4852-108">[in] Ein HRESULT-Datentyp, der den im vorherigen Methodenaufruf generierten Fehlerwert enthält.</span><span class="sxs-lookup"><span data-stu-id="b4852-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="b4852-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b4852-109">_ulFlags_</span></span>
  
> <span data-ttu-id="b4852-110">[in] Eine Bitmaske mit Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="b4852-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="b4852-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b4852-111">The following flag can be set:</span></span>
    
<span data-ttu-id="b4852-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b4852-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b4852-113">Die Zeichenfolgen in der [MAPIERROR-Struktur,](mapierror.md) die im  _lppMAPIError-Parameter_ zurückgegeben wird, sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="b4852-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="b4852-114">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="b4852-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="b4852-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="b4852-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="b4852-116">[out] Ein Zeiger auf einen Zeiger auf eine **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="b4852-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="b4852-117">Der  _lppMAPIError-Parameter_ kann auf NULL festgelegt werden, wenn das Formular keine geeigneten Informationen für eine **MAPIERROR-Struktur liefern** kann.</span><span class="sxs-lookup"><span data-stu-id="b4852-117">The  _lppMAPIError_ parameter can be set to NULL if the form cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b4852-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b4852-118">Return value</span></span>

<span data-ttu-id="b4852-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b4852-119">S_OK</span></span> 
  
> <span data-ttu-id="b4852-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="b4852-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b4852-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="b4852-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="b4852-122">Entweder wurde MAPI_UNICODE-Flag festgelegt, und der Adressbuchanbieter unterstützt Unicode nicht, oder MAPI_UNICODE nicht festgelegt, und der Adressbuchanbieter unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="b4852-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b4852-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b4852-123">Remarks</span></span>

<span data-ttu-id="b4852-124">Form-Objekte implementieren die **IPersistMessage::GetLastError-Methode,** um Informationen zu einem vorherigen Methodenaufruf zu liefern, der fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="b4852-124">Form objects implement the **IPersistMessage::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="b4852-125">Formularbetrachter können ihren Benutzern detaillierte Informationen zum Fehler bereitstellen, indem sie die Daten aus der [MAPIERROR-Struktur](mapierror.md) in ein Dialogfeld eingeben.</span><span class="sxs-lookup"><span data-stu-id="b4852-125">Form viewers can provide their users with detailed information about the error by including the data from the [MAPIERROR](mapierror.md) structure in a dialog box.</span></span> 
  
<span data-ttu-id="b4852-126">Ein Aufruf von **GetLastError** wirkt sich nicht auf den Status des Formulars aus.</span><span class="sxs-lookup"><span data-stu-id="b4852-126">A call to **GetLastError** does not affect the state of the form.</span></span> <span data-ttu-id="b4852-127">Wenn **GetLastError zurückgegeben** wird, verbleibt das Formular in dem Zustand, in dem es sich vor dem Aufruf auf dem Formular begnnen hat.</span><span class="sxs-lookup"><span data-stu-id="b4852-127">When **GetLastError** returns, the form remains in the state that it was in before the call was made.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b4852-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b4852-128">Notes to callers</span></span>

<span data-ttu-id="b4852-129">Sie können die **MAPIERROR-Struktur** verwenden, wenn das Formular eine angibt, auf die der  _lppMAPIError-Parameter_ nur verweist, wenn **GetLastError** eine S_OK.</span><span class="sxs-lookup"><span data-stu-id="b4852-129">You can use the **MAPIERROR** structure, if the form supplies one, that is pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="b4852-130">Manchmal kann das Formular nicht bestimmen, was der letzte Fehler war oder hat nichts mehr über den Fehler zu melden.</span><span class="sxs-lookup"><span data-stu-id="b4852-130">Sometimes the form cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="b4852-131">In diesem Fall gibt das Formular stattdessen einen Zeiger auf NULL in  _lppMAPIError_ zurück.</span><span class="sxs-lookup"><span data-stu-id="b4852-131">In this situation, the form returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="b4852-132">Weitere Informationen zur **GetLastError-Methode** finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="b4852-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b4852-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4852-133">See also</span></span>



[<span data-ttu-id="b4852-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="b4852-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="b4852-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b4852-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b4852-136">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b4852-136">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

