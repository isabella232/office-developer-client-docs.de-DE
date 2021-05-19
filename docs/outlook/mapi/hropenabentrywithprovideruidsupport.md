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
# <a name="hropenabentrywithprovideruidsupport"></a><span data-ttu-id="8d709-103">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="8d709-103">HrOpenABEntryWithProviderUIDSupport</span></span>

  
  
<span data-ttu-id="8d709-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d709-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d709-105">Führt dieselbe Funktion wie die [HrOpenABEntryWithProviderUID-Funktion](hropenabentrywithprovideruid.md) aus, mit der Ausnahme, dass die **HrOpenABEntryWithProviderUIDSupport-Funktion** den Eintrag mithilfe des angegebenen Supportobjekts öffnet, anstatt die Sitzung und das Adressbuch zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d709-105">Performs the same function as the [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) function except that the **HrOpenABEntryWithProviderUIDSupport** function opens the entry using the given support object instead of using the session and the address book.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8d709-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="8d709-106">Header file:</span></span>  <br/> |<span data-ttu-id="8d709-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="8d709-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="8d709-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="8d709-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8d709-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8d709-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8d709-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="8d709-110">Called by:</span></span>  <br/> |<span data-ttu-id="8d709-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="8d709-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="8d709-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d709-112">Parameters</span></span>

 <span data-ttu-id="8d709-113">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="8d709-113">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="8d709-114">[in] Ein Zeiger auf einen _emsabpUID-Parameter,_ der den Exchange identifiziert, den diese Funktion zum Anzeigen von Details zur Eintrags-ID verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="8d709-114">[in] A pointer to an  _emsabpUID_ parameter that identifies the Exchange address book provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="8d709-115">Wenn der Bezeichner für eingehende Eingaben kein eintragsbezeichner Exchange Adressbuchanbieter ist, wird dieser Parameter ignoriert, und der Funktionsaufruf verhält sich genau wie [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="8d709-115">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="8d709-116">Wenn dieser Parameter NULL oder null MAPIUID ist, funktioniert diese Funktion auch genau wie [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="8d709-116">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="8d709-117">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="8d709-117">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="8d709-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="8d709-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="8d709-119">[in] Die Byteanzahl des Eintragsbezeichners, der durch den  _lpEntryID-Parameter angegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="8d709-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="8d709-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="8d709-120">_lpEntryID_</span></span>
  
> <span data-ttu-id="8d709-121">[in] Ein Zeiger auf den Eintragsbezeichner, der den zu öffnende Adressbucheintrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="8d709-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="8d709-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="8d709-122">_lpInterface_</span></span>
  
> <span data-ttu-id="8d709-123">[in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID) der Schnittstelle, die für den Zugriff auf den geöffneten Eintrag verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8d709-123">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="8d709-124">Durch Übergeben von NULL wird die Standardschnittstelle des Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8d709-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="8d709-125">Für Messagingbenutzer ist die Standardschnittstelle [IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="8d709-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="8d709-126">Für Verteilerlisten ist [IDistList : IMAPIContainer](idistlistimapicontainer.md)und für Container [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="8d709-126">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="8d709-127">Anrufer können  _lpInterface_ auf die entsprechende Standardschnittstelle oder eine Schnittstelle in der Vererbungshierarchie festlegen.</span><span class="sxs-lookup"><span data-stu-id="8d709-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="8d709-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8d709-128">_ulFlags_</span></span>
  
> <span data-ttu-id="8d709-129">[in] Eine Bitmaske mit Flags, die den Texttyp für den  _lpszButtonText-Parameter_ steuert.</span><span class="sxs-lookup"><span data-stu-id="8d709-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="8d709-130">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="8d709-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="8d709-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="8d709-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="8d709-132">Gibt an, dass Details TRUE zurückgibt, wenn tatsächlich Änderungen an der Adresse vorgenommen werden. Andernfalls gibt Details FALSE zurück.</span><span class="sxs-lookup"><span data-stu-id="8d709-132">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="8d709-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="8d709-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="8d709-134">Zeigt die modale Version des Dialogfelds allgemeine Adresse an.</span><span class="sxs-lookup"><span data-stu-id="8d709-134">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="8d709-135">Dieses Flag schließen sich gegenseitig mit DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="8d709-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="8d709-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="8d709-136">DIALOG_SDI</span></span>
  
> <span data-ttu-id="8d709-137">Zeigt die moduslose Version des Dialogfelds allgemeine Adresse an.</span><span class="sxs-lookup"><span data-stu-id="8d709-137">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="8d709-138">Dieses Flag schließen sich gegenseitig mit DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="8d709-138">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="8d709-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8d709-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="8d709-140">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="8d709-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="8d709-141">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="8d709-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="8d709-142">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="8d709-142">_lpulObjType_</span></span>
  
> <span data-ttu-id="8d709-143">[out] Ein Zeiger auf den Typ des geöffneten Eintrags.</span><span class="sxs-lookup"><span data-stu-id="8d709-143">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="8d709-144">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="8d709-144">_lppUnk_</span></span>
  
> <span data-ttu-id="8d709-145">[out] Ein Zeiger auf einen Zeiger des geöffneten Eintrags.</span><span class="sxs-lookup"><span data-stu-id="8d709-145">[out] A pointer to a pointer of the opened entry.</span></span>
    

