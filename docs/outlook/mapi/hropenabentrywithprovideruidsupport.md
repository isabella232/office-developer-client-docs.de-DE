---
title: HrOpenABEntryWithProviderUIDSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1fafc810-7cf3-4c8c-bf21-055ae34da690
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: da40e240b60fa42c48185600b74c6162a966e6f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409545"
---
# <a name="hropenabentrywithprovideruidsupport"></a><span data-ttu-id="a2879-103">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="a2879-103">HrOpenABEntryWithProviderUIDSupport</span></span>

  
  
<span data-ttu-id="a2879-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2879-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2879-105">Führt die gleiche Funktion wie die [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) -Funktion aus, mit der Ausnahme, dass die **HrOpenABEntryWithProviderUIDSupport** -Funktion den Eintrag mit dem angegebenen Support Objekt öffnet, statt die Sitzung und das Adressbuch zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a2879-105">Performs the same function as the [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) function except that the **HrOpenABEntryWithProviderUIDSupport** function opens the entry using the given support object instead of using the session and the address book.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a2879-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a2879-106">Header file:</span></span>  <br/> |<span data-ttu-id="a2879-107">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="a2879-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="a2879-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a2879-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a2879-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a2879-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a2879-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a2879-110">Called by:</span></span>  <br/> |<span data-ttu-id="a2879-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="a2879-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="a2879-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2879-112">Parameters</span></span>

 <span data-ttu-id="a2879-113">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="a2879-113">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="a2879-114">in Ein Zeiger auf einen _emsabpUID_ -Parameter, der den Exchange-Adressbuchanbieter identifiziert, der von dieser Funktion verwendet werden soll, um Details zur Eintrags-ID anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a2879-114">[in] A pointer to an  _emsabpUID_ parameter that identifies the Exchange address book provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="a2879-115">Wenn die ID des eingehenden Eintrags kein Exchange-Adressbuchanbieter ist, wird dieser Parameter ignoriert, und der Funktionsaufruf wirkt genau wie [IAddrBook::D ails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="a2879-115">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="a2879-116">Wenn dieser Parameter NULL oder eine NULL-MAPIUID ist, wirkt sich diese Funktion auch genau wie [IAddrBook::D ails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="a2879-116">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="a2879-117">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="a2879-117">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="a2879-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a2879-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="a2879-119">in Die Bytezahl der vom _lpEntryID_ -Parameter angegebenen Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="a2879-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a2879-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="a2879-120">_lpEntryID_</span></span>
  
> <span data-ttu-id="a2879-121">in Ein Zeiger auf die Eintrags-ID, die den zu öffnenden Adressbucheintrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="a2879-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="a2879-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a2879-122">_lpInterface_</span></span>
  
> <span data-ttu-id="a2879-123">in Ein Zeiger auf die Schnittstellen-ID (IID) der Schnittstelle, die für den Zugriff auf den geöffneten Eintrag verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2879-123">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="a2879-124">Beim Übergeben von NULL wird die Standardschnittstelle des Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a2879-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="a2879-125">Für Messagingbenutzer ist die Standardschnittstelle [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="a2879-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="a2879-126">Für Verteilerlisten ist es [IDistList: IMAPIContainer](idistlistimapicontainer.md), und für Container ist es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="a2879-126">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="a2879-127">Anrufer können _lpInterface_ auf die entsprechende Standardschnittstelle oder eine Schnittstelle in der Vererbungshierarchie festlegen.</span><span class="sxs-lookup"><span data-stu-id="a2879-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="a2879-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a2879-128">_ulFlags_</span></span>
  
> <span data-ttu-id="a2879-129">in Eine Bitmaske von Flags, die den Texttyp für den _lpszButtonText_ -Parameter steuert.</span><span class="sxs-lookup"><span data-stu-id="a2879-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="a2879-130">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="a2879-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="a2879-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="a2879-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="a2879-132">Gibt an, dass Details TRUE zurückgegeben werden, wenn tatsächlich Änderungen an der Adresse vorgenommen werden. Andernfalls gibt Details FALSE zurück.</span><span class="sxs-lookup"><span data-stu-id="a2879-132">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="a2879-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="a2879-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="a2879-134">Zeigt die modale Version des Dialogfelds allgemeine Adresse an.</span><span class="sxs-lookup"><span data-stu-id="a2879-134">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="a2879-135">Dieses Flag ist mit DIALOG_SDI gegenseitig ausschließen.</span><span class="sxs-lookup"><span data-stu-id="a2879-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="a2879-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="a2879-136">DIALOG_SDI</span></span>
  
> <span data-ttu-id="a2879-137">Zeigt die nicht modale Version des Dialogfelds allgemeine Adresse an.</span><span class="sxs-lookup"><span data-stu-id="a2879-137">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="a2879-138">Dieses Flag ist mit DIALOG_MODAL gegenseitig ausschließen.</span><span class="sxs-lookup"><span data-stu-id="a2879-138">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="a2879-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a2879-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="a2879-140">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="a2879-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="a2879-141">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="a2879-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="a2879-142">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="a2879-142">_lpulObjType_</span></span>
  
> <span data-ttu-id="a2879-143">Out Ein Zeiger auf den Typ des geöffneten Eintrags.</span><span class="sxs-lookup"><span data-stu-id="a2879-143">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="a2879-144">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="a2879-144">_lppUnk_</span></span>
  
> <span data-ttu-id="a2879-145">Out Ein Zeiger auf einen Zeiger des geöffneten Eintrags.</span><span class="sxs-lookup"><span data-stu-id="a2879-145">[out] A pointer to a pointer of the opened entry.</span></span>
    

