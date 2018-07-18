---
title: IAddrBookNewEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.NewEntry
api_type:
- COM
ms.assetid: 8d2d786b-e621-456d-b087-3373df6f8ac5
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e9b9ae316749659c6fc6a043bfb72c49010ccc9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792020"
---
# <a name="iaddrbooknewentry"></a><span data-ttu-id="c2225-103">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="c2225-103">IAddrBook::NewEntry</span></span>

  
  
<span data-ttu-id="c2225-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c2225-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c2225-105">Fügt einen neuen Empfänger um eine Adressbuchcontainer oder die Empfängerliste von ausgehenden Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="c2225-105">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>
  
```cpp
HRESULT NewEntry(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cbEIDContainer,
  LPENTRYID lpEIDContainer,
  ULONG cbEIDNewEntryTpl,
  LPENTRYID lpEIDNewEntryTpl,
  ULONG FAR * lpcbEIDNewEntry,
  LPENTRYID FAR * lppEIDNewEntry
);
```

## <a name="parameters"></a><span data-ttu-id="c2225-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2225-106">Parameters</span></span>

 <span data-ttu-id="c2225-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c2225-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="c2225-108">[in] Ein Handle für das übergeordnete Fenster für das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c2225-108">[in] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="c2225-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c2225-109">_ulFlags_</span></span>
  
> <span data-ttu-id="c2225-110">[in] Eine Bitmaske aus Flags, die den Typ des Texts gesteuert, die verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2225-110">[in] A bitmask of flags that controls the type of the text that is used.</span></span> <span data-ttu-id="c2225-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c2225-111">The following flag can be set:</span></span>
    
<span data-ttu-id="c2225-112">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c2225-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c2225-113">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="c2225-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="c2225-114">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="c2225-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="c2225-115">_cbEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="c2225-115">_cbEIDContainer_</span></span>
  
> <span data-ttu-id="c2225-116">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEIDContainer_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="c2225-116">[in] The byte count in the entry identifier pointed to by the  _lpEIDContainer_ parameter.</span></span> 
    
 <span data-ttu-id="c2225-117">_lpEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="c2225-117">_lpEIDContainer_</span></span>
  
> <span data-ttu-id="c2225-118">[in] Ein Zeiger auf die Eintrags-ID des Containers, in der neue Empfänger wird hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2225-118">[in] A pointer to the entry identifier of the container where the new recipient is to be added.</span></span> <span data-ttu-id="c2225-119">Wenn der Parameter _CbEIDContainer_ gleich NULL ist, gibt die **NewEntry** -Methode ein Empfänger Eintrags-ID und eine Liste der Vorlagen, als ob die [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) -Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c2225-119">If the  _cbEIDContainer_ parameter is zero, the **NewEntry** method returns a recipient entry identifier and a list of templates as if the [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) method was called.</span></span> 
    
 <span data-ttu-id="c2225-120">_cbEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="c2225-120">_cbEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="c2225-121">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEIDNewEntryTpl_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="c2225-121">[in] The byte count in the entry identifier pointed to by the  _lpEIDNewEntryTpl_ parameter.</span></span> 
    
 <span data-ttu-id="c2225-122">_lpEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="c2225-122">_lpEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="c2225-123">[in] Ein Zeiger auf eine einmalige Vorlage, die zum Erstellen des neuen Empfängers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2225-123">[in] A pointer to a one-off template that will be used to create the new recipient.</span></span> <span data-ttu-id="c2225-124">Wenn _CbEIDNewEntryTpl_ 0 (null ist) und _LpEIDNewEntryTpl_ NULL ist, zeigt **NewEntry** ein Dialogfeld, mit denen der Benutzer aus einer Liste von Vorlagen für neue Einträge auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="c2225-124">If  _cbEIDNewEntryTpl_ is zero and  _lpEIDNewEntryTpl_ is NULL, **NewEntry** displays a dialog box with which the user can select from a list of templates for adding new entries.</span></span> 
    
 <span data-ttu-id="c2225-125">_lpcbEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="c2225-125">_lpcbEIDNewEntry_</span></span>
  
> <span data-ttu-id="c2225-126">[out] Ein Zeiger auf die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LppEIDNewEntry_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="c2225-126">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEIDNewEntry_ parameter.</span></span> 
    
 <span data-ttu-id="c2225-127">_lppEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="c2225-127">_lppEIDNewEntry_</span></span>
  
> <span data-ttu-id="c2225-128">[out] Ein Zeiger auf einen Zeiger auf den neuen Empfänger Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="c2225-128">[out] A pointer to a pointer to the new recipient's entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c2225-129">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="c2225-129">Return value</span></span>

<span data-ttu-id="c2225-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="c2225-130">S_OK</span></span> 
  
> <span data-ttu-id="c2225-131">Der neuen Adresseintrag Adressbuch wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="c2225-131">The new address book entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c2225-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2225-132">Remarks</span></span>

<span data-ttu-id="c2225-133">Die **NewEntry** -Methode erstellt einen neuen Address Book Eintrag direkt in einem Container hinzugefügt werden soll oder verwendet werden, um eine ausgehende Nachricht zu adressieren.</span><span class="sxs-lookup"><span data-stu-id="c2225-133">The **NewEntry** method creates a new address book entry, to be added directly into a container or to be used to address an outgoing message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c2225-134">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="c2225-134">Notes to callers</span></span>

<span data-ttu-id="c2225-135">Wenn Sie den neuen Eintrag auf einen bestimmten Container hinzugefügt werden soll, legen Sie _LpEIDContainer_ Eintrags-ID und _CbEIDContainer_ , um die Byteanzahl von in die Eintrags-ID des Containers.</span><span class="sxs-lookup"><span data-stu-id="c2225-135">If you want the new entry to be added to a specific container, set  _lpEIDContainer_ to the container's entry identifier and  _cbEIDContainer_ to the byte count in the entry identifier.</span></span> 
  
<span data-ttu-id="c2225-136">Wenn Sie den neuen Eintrag der Empfängerliste von ausgehenden Nachrichten hinzugefügt werden soll, legen Sie _LpEIDContainer_ auf NULL und _CbEIDContainer_ auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c2225-136">If you want the new entry to be added to the recipient list of an outgoing message, set  _lpEIDContainer_ to NULL and  _cbEIDContainer_ to zero.</span></span> 
  
<span data-ttu-id="c2225-137">Wenn den Benutzer von einer Clientanwendung aus, wählen Sie den Typ der Eintrag erstellt werden soll, übergeben Sie NULL in _CbEIDNewEntryTpl_ und NULL in _LpEIDNewEntryTpl_.</span><span class="sxs-lookup"><span data-stu-id="c2225-137">If you want to allow the user of a client application to select the type of entry to be created, pass zero in  _cbEIDNewEntryTpl_ and NULL in  _lpEIDNewEntryTpl_.</span></span> <span data-ttu-id="c2225-138">Die **NewEntry** -Methode der MAPI-einmalige Tabelle, eine Liste der Vorlagen unterstützt durch MAPI und durch jede Adressbuchanbieter in der Sitzung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c2225-138">The **NewEntry** method displays the MAPI one-off table, a list of templates supported by MAPI and by each address book provider in the session.</span></span> <span data-ttu-id="c2225-139">Jede Vorlage kann ein Empfänger Eintrag für einen oder mehrere Adresstypen erstellt.</span><span class="sxs-lookup"><span data-stu-id="c2225-139">Each template can create a recipient entry for one or more address types.</span></span> 
  
<span data-ttu-id="c2225-140">Wenn Sie die Eintrags-ID des neuen Eintrags beibehalten möchten, übergeben Sie die Parameter _LpcbEIDNewEntry_ und _LppEIDNewEntry_ gültige Zeiger.</span><span class="sxs-lookup"><span data-stu-id="c2225-140">If you want to retain the entry identifier of the new entry, pass valid pointers in the  _lpcbEIDNewEntry_ and  _lppEIDNewEntry_ parameters.</span></span> <span data-ttu-id="c2225-141">Sie sind verantwortlich für das Freigeben von dieses Eintrags-ID, wenn Sie mit ihm fertig sind, durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c2225-141">You are responsible for freeing this entry identifier when you are finished with it by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="c2225-142">Um eine bestimmte Vorlage verwenden, um einen neuen Eintrag einem änderbare Container hinzuzufügen, verwenden Sie die folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="c2225-142">To use a particular template to add a new entry to a modifiable container, use the following procedure:</span></span>
  
1. <span data-ttu-id="c2225-143">Rufen Sie die [IMAPISession::OpenEntry](imapisession-openentry.md) -Methode zum Öffnen den Zielcontainer, und legen Sie den Parameter _LpEntryID_ auf die Eintrags-ID des Containers.</span><span class="sxs-lookup"><span data-stu-id="c2225-143">Call the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open the destination container, and set the  _lpEntryID_ parameter to the entry identifier of the container.</span></span> 
    
2. <span data-ttu-id="c2225-144">Rufen Sie das Ziel des Containers [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode, und legen Sie den Parameter _UlPropTag_ **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) und der Parameter _Lpiid_ auf IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="c2225-144">Call the destination container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, and set the  _ulPropTag_ parameter to **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) and the  _lpiid_ parameter to IID_IMAPITable.</span></span> <span data-ttu-id="c2225-145">Der Container gibt eine einmalige Tabelle zurück, die alle Vorlagen aufgeführt werden, die sie zum Erstellen neuer Einträge unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c2225-145">The container will return a one-off table that lists all the templates that it supports for creating new entries.</span></span> 
    
3. <span data-ttu-id="c2225-146">Rufen Sie die Zeile, die die Vorlage für den angegebenen Typ des Eintrags darstellt, den Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="c2225-146">Retrieve the row that represents the template for the particular type of entry you want to create.</span></span> <span data-ttu-id="c2225-147">Die **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))-Spalte gibt den Typ der Adresse, der von der Vorlage unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="c2225-147">The **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column indicates the address type that is supported by the template.</span></span>
    
4. <span data-ttu-id="c2225-148">Rufen Sie die **NewEntry** -Methode, und legen Sie _LpEIDNewEntryTpl_ die Eintrags-ID der ausgewählten Vorlage.</span><span class="sxs-lookup"><span data-stu-id="c2225-148">Call the **NewEntry** method, and set  _lpEIDNewEntryTpl_ to the entry identifier of the selected template.</span></span> <span data-ttu-id="c2225-149">Die Eintrags-ID wird die Spalte **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) aus der Vorlage Zeile in der Tabelle "einmal" sein.</span><span class="sxs-lookup"><span data-stu-id="c2225-149">The entry identifier will be the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column from the template's row in the one-off table.</span></span> <span data-ttu-id="c2225-150">Übergeben Sie NULL in _CbEIDContainer_ und NULL in _LpEIDContainer_.</span><span class="sxs-lookup"><span data-stu-id="c2225-150">Pass zero in  _cbEIDContainer_ and NULL in  _lpEIDContainer_.</span></span> <span data-ttu-id="c2225-151">Übergeben Sie einen gültigen Zeiger im _LppEIDNewEntry_ -Parameter, wenn Sie den neuen Eintrag Eintrags-ID beibehalten möchten.</span><span class="sxs-lookup"><span data-stu-id="c2225-151">Pass a valid pointer in the  _lppEIDNewEntry_ parameter if you want to retain the new entry's entry identifier.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c2225-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2225-152">See also</span></span>



[<span data-ttu-id="c2225-153">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c2225-153">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="c2225-154">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="c2225-154">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="c2225-155">PidTagCreateTemplates (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c2225-155">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="c2225-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c2225-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

