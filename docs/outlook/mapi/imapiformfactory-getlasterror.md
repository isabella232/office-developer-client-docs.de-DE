---
title: IMAPIFormFactoryGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.GetLastError
api_type:
- COM
ms.assetid: 4b1d85f6-7996-4839-b985-abf83e305651
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2c83f7788d9c01ab02f1a2bc39a35abe2c5a21c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342147"
---
# <a name="imapiformfactorygetlasterror"></a><span data-ttu-id="e6d35-103">IMAPIFormFactory::GetLastError</span><span class="sxs-lookup"><span data-stu-id="e6d35-103">IMAPIFormFactory::GetLastError</span></span>

  
  
<span data-ttu-id="e6d35-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6d35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6d35-105">Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Fehler enthält, der für das Form Factory-Objekt auftritt.</span><span class="sxs-lookup"><span data-stu-id="e6d35-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="e6d35-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6d35-106">Parameters</span></span>

 <span data-ttu-id="e6d35-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="e6d35-107">_hResult_</span></span>
  
> <span data-ttu-id="e6d35-108">in Ein HRESULT-Datentyp, der den im vorherigen Methodenaufruf generierten Fehlerwert enthält.</span><span class="sxs-lookup"><span data-stu-id="e6d35-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="e6d35-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e6d35-109">_ulFlags_</span></span>
  
> <span data-ttu-id="e6d35-110">in Eine Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="e6d35-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="e6d35-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="e6d35-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="e6d35-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e6d35-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e6d35-113">Die Zeichenfolgen in der **MAPIERROR** -Struktur, die im _lppMAPIError_ -Parameter zurückgegeben werden, sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="e6d35-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="e6d35-114">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="e6d35-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="e6d35-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="e6d35-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="e6d35-116">Out Ein Zeiger auf einen Zeiger auf die zurückgegebene **MAPIERROR** -Struktur, die Versions-, Komponenten-und Kontextinformationen für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="e6d35-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="e6d35-117">Dieser Parameter kann auf NULL festgelegt werden, wenn keine **MAPIERROR** -Struktur zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="e6d35-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e6d35-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6d35-118">Return value</span></span>

<span data-ttu-id="e6d35-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6d35-119">S_OK</span></span> 
  
> <span data-ttu-id="e6d35-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="e6d35-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="e6d35-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="e6d35-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="e6d35-122">Entweder wurde das MAPI_UNICODE-Flag festgelegt, und **getlasterroraufzurufen** unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und **getlasterroraufzurufen** unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="e6d35-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e6d35-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6d35-123">Remarks</span></span>

<span data-ttu-id="e6d35-124">Die **IMAPIFormFactory:: getlasterroraufzurufen** -Methode liefert Informationen zu einem vorherigen Methodenaufruf, der fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="e6d35-124">The **IMAPIFormFactory::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="e6d35-125">Aufrufer können Ihren Benutzern detaillierte Informationen zum Fehler bereitstellen, indem Sie die Daten aus der **MAPIERROR** -Struktur in ein Dialogfeld einschließen.</span><span class="sxs-lookup"><span data-stu-id="e6d35-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e6d35-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="e6d35-126">Notes to callers</span></span>

<span data-ttu-id="e6d35-127">Sie können die **MAPIERROR** -Struktur verwenden, auf die durch den _lppMAPIError_ -Parameter verwiesen wird, wenn MAPI nur dann bereitstellt, wenn **getlasterroraufzurufen** S_OK zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e6d35-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="e6d35-128">Manchmal kann MAPI nicht ermitteln, was der letzte Fehler war oder nicht mehr über den Fehler berichtet hat.</span><span class="sxs-lookup"><span data-stu-id="e6d35-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="e6d35-129">In dieser Situation wird stattdessen ein Zeiger auf NULL in _lppMAPIError_ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e6d35-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="e6d35-130">Weitere Informationen zur **getlasterroraufzurufen** -Methode finden Sie unter [using Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="e6d35-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e6d35-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6d35-131">See also</span></span>



[<span data-ttu-id="e6d35-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="e6d35-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="e6d35-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e6d35-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e6d35-134">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e6d35-134">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

