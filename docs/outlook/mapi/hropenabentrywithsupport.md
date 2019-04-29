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
ms.openlocfilehash: b8574264bdb470906cc097cec56b39a943937d11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417644"
---
# <a name="hropenabentrywithsupport"></a><span data-ttu-id="267d3-103">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="267d3-103">HrOpenABEntryWithSupport</span></span>

  
  
<span data-ttu-id="267d3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="267d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="267d3-105">Verwenden Sie diese Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="267d3-105">Do not use this function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="267d3-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="267d3-106">Header file:</span></span>  <br/> |<span data-ttu-id="267d3-107">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="267d3-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="267d3-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="267d3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="267d3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="267d3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="267d3-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="267d3-110">Called by:</span></span>  <br/> |<span data-ttu-id="267d3-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="267d3-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="267d3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="267d3-112">Parameters</span></span>

 <span data-ttu-id="267d3-113">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="267d3-113">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="267d3-114">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="267d3-114">_cbEntryID_</span></span>
  
> <span data-ttu-id="267d3-115">in Die Bytezahl der vom _lpEntryID_ -Parameter angegebenen Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="267d3-115">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="267d3-116">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="267d3-116">_lpEntryID_</span></span>
  
> <span data-ttu-id="267d3-117">in Ein Zeiger auf die Eintrags-ID, die den zu öffnenden Adressbucheintrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="267d3-117">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="267d3-118">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="267d3-118">_lpInterface_</span></span>
  
>  <span data-ttu-id="267d3-119">in Ein Zeiger auf die Schnittstellen-ID (IID) der Schnittstelle, die für den Zugriff auf den geöffneten Eintrag verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="267d3-119">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="267d3-120">Beim Übergeben von NULL wird die Standardschnittstelle des Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="267d3-120">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="267d3-121">Für Messagingbenutzer ist die Standardschnittstelle [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="267d3-121">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="267d3-122">Für Verteilerlisten ist es [IDistList: IMAPIContainer](idistlistimapicontainer.md), und für Container ist es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="267d3-122">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="267d3-123">Anrufer können _lpInterface_ auf die entsprechende Standardschnittstelle oder eine Schnittstelle in der Vererbungshierarchie festlegen.</span><span class="sxs-lookup"><span data-stu-id="267d3-123">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="267d3-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="267d3-124">_ulFlags_</span></span>
  
> <span data-ttu-id="267d3-125">in Eine Bitmaske von Flags, die den Texttyp für den _lpszButtonText_ -Parameter steuert.</span><span class="sxs-lookup"><span data-stu-id="267d3-125">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="267d3-126">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="267d3-126">The following flags can be set:</span></span> 
    
<span data-ttu-id="267d3-127">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="267d3-127">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="267d3-128">Gibt an, dass Details TRUE zurückgegeben werden, wenn tatsächlich Änderungen an der Adresse vorgenommen werden. Andernfalls gibt Details FALSE zurück.</span><span class="sxs-lookup"><span data-stu-id="267d3-128">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="267d3-129">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="267d3-129">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="267d3-130">Zeigt die modale Version des Dialogfelds allgemeine Adresse an.</span><span class="sxs-lookup"><span data-stu-id="267d3-130">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="267d3-131">Dieses Flag ist mit DIALOG_SDI gegenseitig ausschließen.</span><span class="sxs-lookup"><span data-stu-id="267d3-131">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="267d3-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="267d3-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="267d3-133">Zeigt die nicht modale Version des Dialogfelds allgemeine Adresse an.</span><span class="sxs-lookup"><span data-stu-id="267d3-133">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="267d3-134">Dieses Flag ist mit DIALOG_MODAL gegenseitig ausschließen.</span><span class="sxs-lookup"><span data-stu-id="267d3-134">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="267d3-135">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="267d3-135">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="267d3-136">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="267d3-136">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="267d3-137">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="267d3-137">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="267d3-138">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="267d3-138">_lpulObjType_</span></span>
  
> <span data-ttu-id="267d3-139">Out Ein Zeiger auf den Typ des geöffneten Eintrags.</span><span class="sxs-lookup"><span data-stu-id="267d3-139">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="267d3-140">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="267d3-140">_lppUnk_</span></span>
  
> <span data-ttu-id="267d3-141">Out Ein Zeiger auf einen Zeiger des geöffneten Eintrags.</span><span class="sxs-lookup"><span data-stu-id="267d3-141">[out] A pointer to a pointer of the opened entry.</span></span>
    

