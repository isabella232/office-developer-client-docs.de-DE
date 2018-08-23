---
title: HrOpenABEntryWithSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eaa988ea-aee1-4066-8c78-2b6c28def5e0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 58a6249295810e32c0a0f845e4830b8f393885ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579382"
---
# <a name="hropenabentrywithsupport"></a><span data-ttu-id="36bfc-103">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="36bfc-103">HrOpenABEntryWithSupport</span></span>

  
  
<span data-ttu-id="36bfc-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36bfc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36bfc-105">Verwenden Sie diese Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="36bfc-105">Do not use this function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="36bfc-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="36bfc-106">Header file:</span></span>  <br/> |<span data-ttu-id="36bfc-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="36bfc-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="36bfc-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="36bfc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="36bfc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="36bfc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="36bfc-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="36bfc-110">Called by:</span></span>  <br/> |<span data-ttu-id="36bfc-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="36bfc-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithSupport(
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID  lpInterface,
  ULONG  ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="36bfc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="36bfc-112">Parameters</span></span>

 <span data-ttu-id="36bfc-113">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="36bfc-113">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="36bfc-114">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="36bfc-114">_cbEntryID_</span></span>
  
> <span data-ttu-id="36bfc-115">[in] Die Byteanzahl des Eintrags-ID, die durch den Parameter _LpEntryID_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="36bfc-115">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="36bfc-116">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="36bfc-116">_lpEntryID_</span></span>
  
> <span data-ttu-id="36bfc-117">[in] Ein Zeiger auf die Eintrags-ID, die den Adresseintrag Adressbuch öffnen darstellt.</span><span class="sxs-lookup"><span data-stu-id="36bfc-117">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="36bfc-118">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="36bfc-118">_lpInterface_</span></span>
  
>  <span data-ttu-id="36bfc-119">[in] Ein Zeiger auf die Schnittstelle-ID (IID) der Schnittstelle, greifen Sie auf den Eintrag open verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="36bfc-119">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="36bfc-120">Übergeben von NULL gibt die standard-Schnittstelle des Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="36bfc-120">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="36bfc-121">Für die messaging-Benutzer ist der standard-Benutzeroberfläche [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="36bfc-121">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="36bfc-122">Verteilerlisten, ist es [IDistList: IMAPIContainer](idistlistimapicontainer.md), und für Container, es ist [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="36bfc-122">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="36bfc-123">Anrufer können auf die entsprechende standard-Schnittstelle oder eine Schnittstelle in der Vererbungshierarchie _LpInterface_ festlegen.</span><span class="sxs-lookup"><span data-stu-id="36bfc-123">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="36bfc-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="36bfc-124">_ulFlags_</span></span>
  
> <span data-ttu-id="36bfc-125">[in] Eine Bitmaske aus Flags, die den Typ des Texts für den Parameter _LpszButtonText_ steuert.</span><span class="sxs-lookup"><span data-stu-id="36bfc-125">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="36bfc-126">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="36bfc-126">The following flags can be set:</span></span> 
    
<span data-ttu-id="36bfc-127">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="36bfc-127">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="36bfc-128">Gibt an, dass Details gibt TRUE zurück, wenn die Adresse tatsächlich geändert werden. Details andernfalls FALSE.</span><span class="sxs-lookup"><span data-stu-id="36bfc-128">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="36bfc-129">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="36bfc-129">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="36bfc-130">Zeigt die modale Version im Dialogfeld allgemeine Adresse.</span><span class="sxs-lookup"><span data-stu-id="36bfc-130">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="36bfc-131">Dieses Kennzeichen ist mit DIALOG_SDI gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="36bfc-131">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="36bfc-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="36bfc-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="36bfc-133">Zeigt die allgemeine Adresse im Dialogfeld ohne Modus Version.</span><span class="sxs-lookup"><span data-stu-id="36bfc-133">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="36bfc-134">Dieses Kennzeichen ist mit DIALOG_MODAL gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="36bfc-134">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="36bfc-135">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="36bfc-135">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="36bfc-136">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="36bfc-136">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="36bfc-137">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="36bfc-137">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="36bfc-138">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="36bfc-138">_lpulObjType_</span></span>
  
> <span data-ttu-id="36bfc-139">[out] Ein Zeiger auf den Typ des Eintrags geöffnet.</span><span class="sxs-lookup"><span data-stu-id="36bfc-139">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="36bfc-140">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="36bfc-140">_lppUnk_</span></span>
  
> <span data-ttu-id="36bfc-141">[out] Ein Zeiger auf einen Zeiger des Eintrags geöffnet.</span><span class="sxs-lookup"><span data-stu-id="36bfc-141">[out] A pointer to a pointer of the opened entry.</span></span>
    

