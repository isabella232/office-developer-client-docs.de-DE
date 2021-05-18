---
title: IMAPISupportRegisterPreprocessor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.RegisterPreprocessor
api_type:
- COM
ms.assetid: 9b5659ab-2b49-41ab-92ce-ca343e35d670
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 58215de6cc4e9e68386f8f017839752acc6e1753
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404897"
---
# <a name="imapisupportregisterpreprocessor"></a><span data-ttu-id="72142-103">IMAPISupport::RegisterPreprocessor</span><span class="sxs-lookup"><span data-stu-id="72142-103">IMAPISupport::RegisterPreprocessor</span></span>

  
  
<span data-ttu-id="72142-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72142-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72142-105">Registriert die Preprozessorfunktion eines Transportanbieters (eine Funktion, die dem [PreprocessMessage-Prototyp](preprocessmessage.md) entspricht).</span><span class="sxs-lookup"><span data-stu-id="72142-105">Registers a transport provider's preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> 
  
```cpp
HRESULT RegisterPreprocessor(
LPMAPIUID lpMuid,
LPSTR lpszAdrType,
LPSTR lpszDLLName,
LPSTR lpszPreprocess,
LPSTR lpszRemovePreprocessInfo,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="72142-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="72142-106">Parameters</span></span>

 <span data-ttu-id="72142-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="72142-107">_lpMuid_</span></span>
  
> <span data-ttu-id="72142-108">[in] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den Bezeichner enthält, den die Präprozessorfunktion verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="72142-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the identifier that the preprocessor function handles.</span></span> <span data-ttu-id="72142-109">Der  _lpMuid-Parameter_ kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="72142-109">The  _lpMuid_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="72142-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="72142-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="72142-111">[in] Ein Zeiger auf den Adresstyp für die Nachrichten, für die die Funktion arbeitet, z. B. FAX, SMTP oder X500.</span><span class="sxs-lookup"><span data-stu-id="72142-111">[in] A pointer to the address type for the messages the function operates on, such as FAX, SMTP, or X500.</span></span> <span data-ttu-id="72142-112">Der  _lpszAdrType-Parameter_ kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="72142-112">The  _lpszAdrType_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="72142-113">_lpszDLLName_</span><span class="sxs-lookup"><span data-stu-id="72142-113">_lpszDLLName_</span></span>
  
> <span data-ttu-id="72142-114">[in] Ein Zeiger auf den Namen der Dynamic-Link Library (DLL), die den Einstiegspunkt für die Präprozessorfunktion enthält.</span><span class="sxs-lookup"><span data-stu-id="72142-114">[in] A pointer to the name of the dynamic-link library (DLL) that contains the entry point for the preprocessor function.</span></span>
    
 <span data-ttu-id="72142-115">_lpszPreprocess_</span><span class="sxs-lookup"><span data-stu-id="72142-115">_lpszPreprocess_</span></span>
  
> <span data-ttu-id="72142-116">[in] Ein Zeiger auf den Namen der Präprozessorfunktion.</span><span class="sxs-lookup"><span data-stu-id="72142-116">[in] A pointer to the name of the preprocessor function.</span></span> <span data-ttu-id="72142-117">Der  _lpszPreprocess-Parameter_ kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="72142-117">The  _lpszPreprocess_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="72142-118">_lpszRemovePreprocessInfo_</span><span class="sxs-lookup"><span data-stu-id="72142-118">_lpszRemovePreprocessInfo_</span></span>
  
> <span data-ttu-id="72142-119">[in] Ein Zeiger auf den Namen der Funktion, die Vorverarbeitungsinformationen entfernt (eine Funktion, die dem [RemovePreprocessInfo-Prototyp entspricht).](removepreprocessinfo.md)</span><span class="sxs-lookup"><span data-stu-id="72142-119">[in] A pointer to the name of the function that removes preprocessor information (a function that conforms to the [RemovePreprocessInfo](removepreprocessinfo.md) prototype).</span></span> <span data-ttu-id="72142-120">Der  _lpszRemovePreprocessInfo-Parameter_ kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="72142-120">The  _lpszRemovePreprocessInfo_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="72142-121">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="72142-121">_ulFlags_</span></span>
  
> <span data-ttu-id="72142-122">Reserviert; muss null sein.</span><span class="sxs-lookup"><span data-stu-id="72142-122">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="72142-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72142-123">Return value</span></span>

<span data-ttu-id="72142-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="72142-124">S_OK</span></span> 
  
> <span data-ttu-id="72142-125">Die Preprocessor-Funktion wurde erfolgreich registriert.</span><span class="sxs-lookup"><span data-stu-id="72142-125">The preprocessor function was successfully registered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="72142-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="72142-126">Remarks</span></span>

<span data-ttu-id="72142-127">Die **IMAPISupport::RegisterPreprocessor-Methode** wird nur für Unterstützungsobjekte des Transportanbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="72142-127">The **IMAPISupport::RegisterPreprocessor** method is implemented for transport provider support objects only.</span></span> <span data-ttu-id="72142-128">Transportanbieter rufen **RegisterPreprocessor auf,** um eine Präprozessorfunktion zu registrieren (eine Funktion, die dem [PreprocessMessage-Prototyp](preprocessmessage.md) entspricht).</span><span class="sxs-lookup"><span data-stu-id="72142-128">Transport providers call **RegisterPreprocessor** to register a preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> <span data-ttu-id="72142-129">Eine Präprozessorfunktion muss registriert werden, bevor der MAPI-Spooler sie aufrufen kann.</span><span class="sxs-lookup"><span data-stu-id="72142-129">A preprocessor function must be registered before the MAPI spooler can call it.</span></span> 
  
<span data-ttu-id="72142-130">Die  _Parameter lpszPreprocess,_  _lpszRemovePreprocessInfo_ und  _lpszDLLName_ sollten alle auf Zeichenfolgen verweisen, die zusammen mit Aufrufen der Win32 **GetProcAddress-Funktion** verwendet werden können, sodass der DLL-Einstiegspunkt des Präprozessors ordnungsgemäß aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="72142-130">The  _lpszPreprocess_,  _lpszRemovePreprocessInfo_, and  _lpszDLLName_ parameters should all point to strings that can be used in conjunction with calls to the Win32 **GetProcAddress** function, allowing the preprocessor's DLL entry point to be called correctly.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="72142-131">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="72142-131">Notes to callers</span></span>

<span data-ttu-id="72142-132">Aufrufe an Präprozessoren sind spezifisch für die Reihenfolge des Transportanbieters.</span><span class="sxs-lookup"><span data-stu-id="72142-132">Calls to preprocessors are specific to transport provider order.</span></span> <span data-ttu-id="72142-133">Dies bedeutet, dass, wenn ein anderer Transportanbieter vor Ihrem Anbieter eine Nachricht verarbeiten kann, Ihre Präprozessorfunktion nicht für diese Nachricht aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="72142-133">This means that if another transport provider ahead of your provider is able to handle a message, your preprocessor function will not be called for that message.</span></span> <span data-ttu-id="72142-134">Ihre Präprozessorfunktion wird nur für Nachrichten aufgerufen, die Sie behandeln.</span><span class="sxs-lookup"><span data-stu-id="72142-134">Your preprocessor function will be called only for messages that you will handle.</span></span>
  
<span data-ttu-id="72142-135">Sie können Präprozessorfunktionen schreiben, um entweder einen bestimmten Bezeichner zu verarbeiten, der in einer [MAPIUID-Struktur](mapiuid.md) gespeichert ist, oder einen Adresstyp.</span><span class="sxs-lookup"><span data-stu-id="72142-135">You can write preprocessor functions to handle either a specific identifier stored in a [MAPIUID](mapiuid.md) structure or a type of address.</span></span> <span data-ttu-id="72142-136">Wenn Sie sowohl eine **MAPIUID-Struktur** im  _lpMuid-Parameter_ als auch einen Adresstyp im  _lpszAdrType-Parameter_ angeben, wird Ihre Funktion für Nachrichtenempfänger aufgerufen, die entweder der **MAPIUID** oder dem Adresstyp entsprechen.</span><span class="sxs-lookup"><span data-stu-id="72142-136">If you specify both a **MAPIUID** structure in the  _lpMuid_ parameter and an address type in the  _lpszAdrType_ parameter, your function will be called for message recipients that match either the **MAPIUID** or the address type.</span></span> <span data-ttu-id="72142-137">Wenn _lpMuid_ NULL und _lpszAdrType_ nicht NULL ist, wird Ihre Funktion nur für Empfänger aufgerufen, die eine Adresse haben, die dem Typ entspricht, auf den _lpszAdrType verweist._</span><span class="sxs-lookup"><span data-stu-id="72142-137">If  _lpMuid_ is NULL and  _lpszAdrType_ is non-NULL, your function will be called only for recipients that have an address that matches the type pointed to by  _lpszAdrType_.</span></span> <span data-ttu-id="72142-138">Wenn  _lpMuid_ nicht NULL und  _lpszAdrType_ NULL ist, wird Ihre Funktion für Empfänger aufgerufen, die **MAPIUID** entsprechen, unabhängig vom Adresstyp.</span><span class="sxs-lookup"><span data-stu-id="72142-138">If  _lpMuid_ is non-NULL and  _lpszAdrType_ is NULL, your function will be called for recipients that match **MAPIUID**, regardless of their address type.</span></span> <span data-ttu-id="72142-139">Wenn beide Null sind, wird Ihre Funktion für alle Empfänger der Nachricht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="72142-139">If both are NULL, your function is called for all recipients of the message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="72142-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72142-140">See also</span></span>



[<span data-ttu-id="72142-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="72142-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="72142-142">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="72142-142">PreprocessMessage</span></span>](preprocessmessage.md)
  
[<span data-ttu-id="72142-143">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="72142-143">RemovePreprocessInfo</span></span>](removepreprocessinfo.md)
  
[<span data-ttu-id="72142-144">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="72142-144">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

