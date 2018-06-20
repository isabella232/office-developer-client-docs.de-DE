---
title: HrOpenABEntryWithProviderUIDSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1fafc810-7cf3-4c8c-bf21-055ae34da690
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bd42fcd34042c2f9579497f164c4a67f6ba97e35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791961"
---
# <a name="hropenabentrywithprovideruidsupport"></a><span data-ttu-id="97599-103">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="97599-103">HrOpenABEntryWithProviderUIDSupport</span></span>

  
  
<span data-ttu-id="97599-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="97599-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="97599-105">Führt die gleiche Funktion wie die [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) -Funktion, mit der Ausnahme, dass die **HrOpenABEntryWithProviderUIDSupport** -Funktion den Eintrag mithilfe des angegebenen Support-Objekts statt der Sitzung und das Adressbuch wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="97599-105">Performs the same function as the [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) function except that the **HrOpenABEntryWithProviderUIDSupport** function opens the entry using the given support object instead of using the session and the address book.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="97599-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="97599-106">Header file:</span></span>  <br/> |<span data-ttu-id="97599-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="97599-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="97599-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="97599-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="97599-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="97599-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="97599-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="97599-110">Called by:</span></span>  <br/> |<span data-ttu-id="97599-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="97599-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUIDSupport(
  const MAPIUID *pEmsabpUID,
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="97599-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="97599-112">Parameters</span></span>

 <span data-ttu-id="97599-113">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="97599-113">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="97599-114">[in] Ein Zeiger auf ein _EmsabpUID_ -Parameter, der die Exchange-Adressbuchanbieter identifiziert, die diese Funktion zum Anzeigen von Details auf die Eintrags-ID verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="97599-114">[in] A pointer to an  _emsabpUID_ parameter that identifies the Exchange address book provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="97599-115">Wenn eingehende Eintrags-ID nicht um ein Exchange Address Book Anbieter Eintrags-ID ist, dieser Parameter wird ignoriert, und die Funktion Anruf-verhält sich genau wie [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="97599-115">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="97599-116">Wenn dieser Parameter auf NULL oder eine MAPIUID NULL ist, verhält sich diese Funktion auch genau wie [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="97599-116">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="97599-117">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="97599-117">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="97599-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="97599-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="97599-119">[in] Die Byteanzahl des Eintrags-ID, die durch den Parameter _LpEntryID_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="97599-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="97599-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="97599-120">_lpEntryID_</span></span>
  
> <span data-ttu-id="97599-121">[in] Ein Zeiger auf die Eintrags-ID, die den Adresseintrag Adressbuch öffnen darstellt.</span><span class="sxs-lookup"><span data-stu-id="97599-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="97599-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="97599-122">_lpInterface_</span></span>
  
> <span data-ttu-id="97599-123">[in] Ein Zeiger auf die Schnittstelle-ID (IID) der Schnittstelle, greifen Sie auf den Eintrag open verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="97599-123">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="97599-124">Übergeben von NULL gibt die standard-Schnittstelle des Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="97599-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="97599-125">Für die messaging-Benutzer ist der standard-Benutzeroberfläche [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="97599-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="97599-126">Wird für es Verteilerlisten [IDistList: IMAPIContainer](idistlistimapicontainer.md), und für Container ist [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="97599-126">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="97599-127">Anrufer können auf die entsprechende standard-Schnittstelle oder eine Schnittstelle in der Vererbungshierarchie _LpInterface_ festlegen.</span><span class="sxs-lookup"><span data-stu-id="97599-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="97599-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="97599-128">_ulFlags_</span></span>
  
> <span data-ttu-id="97599-129">[in] Eine Bitmaske aus Flags, die den Typ des Texts für den Parameter _LpszButtonText_ steuert.</span><span class="sxs-lookup"><span data-stu-id="97599-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="97599-130">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="97599-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="97599-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="97599-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="97599-132">Gibt an, dass Details gibt TRUE zurück, wenn die Adresse tatsächlich geändert werden. Details andernfalls FALSE.</span><span class="sxs-lookup"><span data-stu-id="97599-132">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="97599-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="97599-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="97599-134">Zeigt die modale Version im Dialogfeld allgemeine Adresse.</span><span class="sxs-lookup"><span data-stu-id="97599-134">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="97599-135">Dieses Kennzeichen ist mit DIALOG_SDI gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="97599-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="97599-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="97599-136">DIALOG_SDI</span></span>
  
> <span data-ttu-id="97599-137">Zeigt die allgemeine Adresse im Dialogfeld ohne Modus Version.</span><span class="sxs-lookup"><span data-stu-id="97599-137">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="97599-138">Dieses Kennzeichen ist mit DIALOG_MODAL gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="97599-138">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="97599-139">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="97599-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="97599-140">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="97599-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="97599-141">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="97599-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="97599-142">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="97599-142">_lpulObjType_</span></span>
  
> <span data-ttu-id="97599-143">[out] Ein Zeiger auf den Typ des Eintrags geöffnet.</span><span class="sxs-lookup"><span data-stu-id="97599-143">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="97599-144">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="97599-144">_lppUnk_</span></span>
  
> <span data-ttu-id="97599-145">[out] Ein Zeiger auf einen Zeiger des Eintrags geöffnet.</span><span class="sxs-lookup"><span data-stu-id="97599-145">[out] A pointer to a pointer of the opened entry.</span></span>
    

