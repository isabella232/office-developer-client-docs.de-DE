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
ms.openlocfilehash: 87f5e3f159542359f614a6ab698e6f06a2faf41a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567916"
---
# <a name="imapisupportregisterpreprocessor"></a><span data-ttu-id="d16f1-103">IMAPISupport::RegisterPreprocessor</span><span class="sxs-lookup"><span data-stu-id="d16f1-103">IMAPISupport::RegisterPreprocessor</span></span>

  
  
<span data-ttu-id="d16f1-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d16f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d16f1-105">Registriert einen Adressbuchhierarchie Präprozessor-Funktion (eine Funktion, die den [PreprocessMessage](preprocessmessage.md) Prototyp entspricht).</span><span class="sxs-lookup"><span data-stu-id="d16f1-105">Registers a transport provider's preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="d16f1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d16f1-106">Parameters</span></span>

 <span data-ttu-id="d16f1-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="d16f1-107">_lpMuid_</span></span>
  
> <span data-ttu-id="d16f1-108">[in] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den Bezeichner enthält, den die Präprozessor-Funktion behandelt.</span><span class="sxs-lookup"><span data-stu-id="d16f1-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the identifier that the preprocessor function handles.</span></span> <span data-ttu-id="d16f1-109">Der Parameter _LpMuid_ kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d16f1-109">The  _lpMuid_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="d16f1-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="d16f1-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="d16f1-111">[in] Ein Zeiger auf den Adresstyp für die Nachrichten wirkt sich die Funktion auf, wie FAX, SMTP oder X500.</span><span class="sxs-lookup"><span data-stu-id="d16f1-111">[in] A pointer to the address type for the messages the function operates on, such as FAX, SMTP, or X500.</span></span> <span data-ttu-id="d16f1-112">Der Parameter _LpszAdrType_ kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d16f1-112">The  _lpszAdrType_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="d16f1-113">_lpszDLLName_</span><span class="sxs-lookup"><span data-stu-id="d16f1-113">_lpszDLLName_</span></span>
  
> <span data-ttu-id="d16f1-114">[in] Ein Zeiger auf den Namen des Dynamic Link Library (DLL), die den Einstiegspunkt für die Präprozessor-Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="d16f1-114">[in] A pointer to the name of the dynamic-link library (DLL) that contains the entry point for the preprocessor function.</span></span>
    
 <span data-ttu-id="d16f1-115">_lpszPreprocess_</span><span class="sxs-lookup"><span data-stu-id="d16f1-115">_lpszPreprocess_</span></span>
  
> <span data-ttu-id="d16f1-116">[in] Ein Zeiger auf den Namen der Präprozessor-Funktion.</span><span class="sxs-lookup"><span data-stu-id="d16f1-116">[in] A pointer to the name of the preprocessor function.</span></span> <span data-ttu-id="d16f1-117">Der Parameter _LpszPreprocess_ kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d16f1-117">The  _lpszPreprocess_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="d16f1-118">_lpszRemovePreprocessInfo_</span><span class="sxs-lookup"><span data-stu-id="d16f1-118">_lpszRemovePreprocessInfo_</span></span>
  
> <span data-ttu-id="d16f1-119">[in] Ein Zeiger auf den Namen der Funktion, die entfernt Präprozessor Informationen (eine Funktion, die den [RemovePreprocessInfo](removepreprocessinfo.md) Prototyp entspricht).</span><span class="sxs-lookup"><span data-stu-id="d16f1-119">[in] A pointer to the name of the function that removes preprocessor information (a function that conforms to the [RemovePreprocessInfo](removepreprocessinfo.md) prototype).</span></span> <span data-ttu-id="d16f1-120">Der Parameter _LpszRemovePreprocessInfo_ kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d16f1-120">The  _lpszRemovePreprocessInfo_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="d16f1-121">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d16f1-121">_ulFlags_</span></span>
  
> <span data-ttu-id="d16f1-122">Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="d16f1-122">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d16f1-123">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="d16f1-123">Return value</span></span>

<span data-ttu-id="d16f1-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="d16f1-124">S_OK</span></span> 
  
> <span data-ttu-id="d16f1-125">Die Präprozessor-Funktion wurde erfolgreich registriert.</span><span class="sxs-lookup"><span data-stu-id="d16f1-125">The preprocessor function was successfully registered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d16f1-126">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="d16f1-126">Remarks</span></span>

<span data-ttu-id="d16f1-127">Die **IMAPISupport::RegisterPreprocessor** -Methode wird für nur Unterstützungsobjekte der Transport-Anbieter implementiert.</span><span class="sxs-lookup"><span data-stu-id="d16f1-127">The **IMAPISupport::RegisterPreprocessor** method is implemented for transport provider support objects only.</span></span> <span data-ttu-id="d16f1-128">Transportanbieter Aufrufen **RegisterPreprocessor** zum Registrieren einer Präprozessor-Funktion (eine Funktion, die den [PreprocessMessage](preprocessmessage.md) Prototyp entspricht).</span><span class="sxs-lookup"><span data-stu-id="d16f1-128">Transport providers call **RegisterPreprocessor** to register a preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> <span data-ttu-id="d16f1-129">Eine Funktion Präprozessor muss registriert werden, bevor die MAPI-Warteschlange aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="d16f1-129">A preprocessor function must be registered before the MAPI spooler can call it.</span></span> 
  
<span data-ttu-id="d16f1-130">Der Parameter _LpszPreprocess_, _LpszRemovePreprocessInfo_und _LpszDLLName_ sollten alle in Zeichenfolgen verweisen, die in Verbindung mit der Aufrufe der Win32 **GetProcAddress** -Funktion, die der Präprozessor DLL zulassen verwendet werden können Einstiegspunkt ordnungsgemäß aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d16f1-130">The  _lpszPreprocess_,  _lpszRemovePreprocessInfo_, and  _lpszDLLName_ parameters should all point to strings that can be used in conjunction with calls to the Win32 **GetProcAddress** function, allowing the preprocessor's DLL entry point to be called correctly.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d16f1-131">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="d16f1-131">Notes to callers</span></span>

<span data-ttu-id="d16f1-132">Anrufe an Präprozessoren sind für Transport Reihenfolge der Anbieter spezifisch.</span><span class="sxs-lookup"><span data-stu-id="d16f1-132">Calls to preprocessors are specific to transport provider order.</span></span> <span data-ttu-id="d16f1-133">Dies bedeutet, dass wenn eine andere Adressbuchhierarchie vor Ihrem Anbieter um eine Nachricht zu verarbeiten kann, Ihre Funktion Präprozessor für diese Nachricht nicht aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d16f1-133">This means that if another transport provider ahead of your provider is able to handle a message, your preprocessor function will not be called for that message.</span></span> <span data-ttu-id="d16f1-134">Nur für Nachrichten, die Sie behandelt, wird Ihre Präprozessor Funktion aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d16f1-134">Your preprocessor function will be called only for messages that you will handle.</span></span>
  
<span data-ttu-id="d16f1-135">Sie können Präprozessor Funktionen zur Verarbeitung von entweder eines bestimmten Bezeichners in eine [MAPIUID](mapiuid.md) Struktur oder einen Adresstyp gespeichert schreiben.</span><span class="sxs-lookup"><span data-stu-id="d16f1-135">You can write preprocessor functions to handle either a specific identifier stored in a [MAPIUID](mapiuid.md) structure or a type of address.</span></span> <span data-ttu-id="d16f1-136">Wenn Sie eine **MAPIUID** -Struktur in der _LpMuid_ -Parameter und einen Adresstyp im _LpszAdrType_ -Parameter angeben, wird die Funktion für Empfänger der Nachricht aufgerufen werden, die die **MAPIUID** oder den Adresstyp entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d16f1-136">If you specify both a **MAPIUID** structure in the  _lpMuid_ parameter and an address type in the  _lpszAdrType_ parameter, your function will be called for message recipients that match either the **MAPIUID** or the address type.</span></span> <span data-ttu-id="d16f1-137">Wenn _LpMuid_ NULL ist, und _LpszAdrType_ ungleich NULL ist, wird Ihre Funktion nur für Empfänger aufgerufen, der Adresse, die den Typ auf den _LpszAdrType_entspricht.</span><span class="sxs-lookup"><span data-stu-id="d16f1-137">If  _lpMuid_ is NULL and  _lpszAdrType_ is non-NULL, your function will be called only for recipients that have an address that matches the type pointed to by  _lpszAdrType_.</span></span> <span data-ttu-id="d16f1-138">Wenn _LpMuid_ ungleich NULL ist, und _LpszAdrType_ NULL ist, wird Ihre Funktion für Empfänger aufgerufen werden, die mit **MAPIUID**, unabhängig von deren Adresstyp übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="d16f1-138">If  _lpMuid_ is non-NULL and  _lpszAdrType_ is NULL, your function will be called for recipients that match **MAPIUID**, regardless of their address type.</span></span> <span data-ttu-id="d16f1-139">Wenn beide NULL sind, wird die Funktion für alle Empfänger der Nachricht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d16f1-139">If both are NULL, your function is called for all recipients of the message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d16f1-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d16f1-140">See also</span></span>



[<span data-ttu-id="d16f1-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="d16f1-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="d16f1-142">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="d16f1-142">PreprocessMessage</span></span>](preprocessmessage.md)
  
[<span data-ttu-id="d16f1-143">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="d16f1-143">RemovePreprocessInfo</span></span>](removepreprocessinfo.md)
  
[<span data-ttu-id="d16f1-144">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d16f1-144">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

