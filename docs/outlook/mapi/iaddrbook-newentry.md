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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 285da82d143524d2b2cf73ed3e5f1e3aeef6f9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405100"
---
# <a name="iaddrbooknewentry"></a><span data-ttu-id="26a75-103">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="26a75-103">IAddrBook::NewEntry</span></span>

  
  
<span data-ttu-id="26a75-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26a75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26a75-105">Fügt einem Adressbuchcontainer oder der Empfängerliste einer ausgehenden Nachricht einen neuen Empfänger hinzu.</span><span class="sxs-lookup"><span data-stu-id="26a75-105">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="26a75-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="26a75-106">Parameters</span></span>

 <span data-ttu-id="26a75-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="26a75-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="26a75-108">[in] Ein Handle zum übergeordneten Fenster für das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="26a75-108">[in] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="26a75-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="26a75-109">_ulFlags_</span></span>
  
> <span data-ttu-id="26a75-110">[in] Eine Bitmaske mit Flags, die den Texttyp steuert, der verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="26a75-110">[in] A bitmask of flags that controls the type of the text that is used.</span></span> <span data-ttu-id="26a75-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="26a75-111">The following flag can be set:</span></span>
    
<span data-ttu-id="26a75-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="26a75-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="26a75-113">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="26a75-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="26a75-114">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="26a75-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="26a75-115">_cbEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="26a75-115">_cbEIDContainer_</span></span>
  
> <span data-ttu-id="26a75-116">[in] Die Byteanzahl in der Eintrags-ID, auf die der  _lpEIDContainer-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="26a75-116">[in] The byte count in the entry identifier pointed to by the  _lpEIDContainer_ parameter.</span></span> 
    
 <span data-ttu-id="26a75-117">_lpEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="26a75-117">_lpEIDContainer_</span></span>
  
> <span data-ttu-id="26a75-118">[in] Ein Zeiger auf die Eintrags-ID des Containers, in dem der neue Empfänger hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="26a75-118">[in] A pointer to the entry identifier of the container where the new recipient is to be added.</span></span> <span data-ttu-id="26a75-119">Wenn der  _cbEIDContainer-Parameter_ null ist, gibt die **NewEntry-Methode** einen Empfängereintragsbezeichner und eine Liste von Vorlagen zurück, als ob die [IAddrBook::CreateOneOff-Methode](iaddrbook-createoneoff.md) aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="26a75-119">If the  _cbEIDContainer_ parameter is zero, the **NewEntry** method returns a recipient entry identifier and a list of templates as if the [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) method was called.</span></span> 
    
 <span data-ttu-id="26a75-120">_cbEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="26a75-120">_cbEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="26a75-121">[in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEIDNewEntryTpl-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="26a75-121">[in] The byte count in the entry identifier pointed to by the  _lpEIDNewEntryTpl_ parameter.</span></span> 
    
 <span data-ttu-id="26a75-122">_lpEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="26a75-122">_lpEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="26a75-123">[in] Ein Zeiger auf eine einmal verwendete Vorlage, die zum Erstellen des neuen Empfängers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="26a75-123">[in] A pointer to a one-off template that will be used to create the new recipient.</span></span> <span data-ttu-id="26a75-124">Wenn  _cbEIDNewEntryTpl_ null und  _lpEIDNewEntryTpl_ NULL ist, zeigt **NewEntry** ein Dialogfeld an, mit dem der Benutzer aus einer Liste von Vorlagen zum Hinzufügen neuer Einträge auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="26a75-124">If  _cbEIDNewEntryTpl_ is zero and  _lpEIDNewEntryTpl_ is NULL, **NewEntry** displays a dialog box with which the user can select from a list of templates for adding new entries.</span></span> 
    
 <span data-ttu-id="26a75-125">_lpcbEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="26a75-125">_lpcbEIDNewEntry_</span></span>
  
> <span data-ttu-id="26a75-126">[out] Ein Zeiger auf die Byteanzahl im Eintragsbezeichner, auf den der  _lppEIDNewEntry-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="26a75-126">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEIDNewEntry_ parameter.</span></span> 
    
 <span data-ttu-id="26a75-127">_lppEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="26a75-127">_lppEIDNewEntry_</span></span>
  
> <span data-ttu-id="26a75-128">[out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID des neuen Empfängers.</span><span class="sxs-lookup"><span data-stu-id="26a75-128">[out] A pointer to a pointer to the new recipient's entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="26a75-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26a75-129">Return value</span></span>

<span data-ttu-id="26a75-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="26a75-130">S_OK</span></span> 
  
> <span data-ttu-id="26a75-131">Der neue Adressbucheintrag wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="26a75-131">The new address book entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="26a75-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="26a75-132">Remarks</span></span>

<span data-ttu-id="26a75-133">Die **NewEntry-Methode** erstellt einen neuen Adressbucheintrag, der direkt zu einem Container hinzugefügt oder für die Adresseingabe einer ausgehenden Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="26a75-133">The **NewEntry** method creates a new address book entry, to be added directly into a container or to be used to address an outgoing message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="26a75-134">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="26a75-134">Notes to callers</span></span>

<span data-ttu-id="26a75-135">Wenn der neue Eintrag einem bestimmten Container hinzugefügt werden soll, legen Sie  _lpEIDContainer_ auf den Eintragsbezeichner des Containers und  _cbEIDContainer_ auf die Byteanzahl in der Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="26a75-135">If you want the new entry to be added to a specific container, set  _lpEIDContainer_ to the container's entry identifier and  _cbEIDContainer_ to the byte count in the entry identifier.</span></span> 
  
<span data-ttu-id="26a75-136">Wenn der neue Eintrag der Empfängerliste einer ausgehenden Nachricht hinzugefügt werden soll, legen Sie  _lpEIDContainer_ auf NULL und  _cbEIDContainer_ auf Null.</span><span class="sxs-lookup"><span data-stu-id="26a75-136">If you want the new entry to be added to the recipient list of an outgoing message, set  _lpEIDContainer_ to NULL and  _cbEIDContainer_ to zero.</span></span> 
  
<span data-ttu-id="26a75-137">Wenn Sie dem Benutzer einer Clientanwendung die Auswahl des zu erstellenden Eintragstyps ermöglichen möchten, übergeben Sie null in  _cbEIDNewEntryTpl_ und NULL in  _lpEIDNewEntryTpl_.</span><span class="sxs-lookup"><span data-stu-id="26a75-137">If you want to allow the user of a client application to select the type of entry to be created, pass zero in  _cbEIDNewEntryTpl_ and NULL in  _lpEIDNewEntryTpl_.</span></span> <span data-ttu-id="26a75-138">Die **NewEntry-Methode** zeigt die one-off-Tabelle MAPI an, eine Liste von Vorlagen, die von MAPI und von jedem Adressbuchanbieter in der Sitzung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="26a75-138">The **NewEntry** method displays the MAPI one-off table, a list of templates supported by MAPI and by each address book provider in the session.</span></span> <span data-ttu-id="26a75-139">Jede Vorlage kann einen Empfängereintrag für einen oder mehrere Adresstypen erstellen.</span><span class="sxs-lookup"><span data-stu-id="26a75-139">Each template can create a recipient entry for one or more address types.</span></span> 
  
<span data-ttu-id="26a75-140">Wenn Sie den Eintragsbezeichner des neuen Eintrags beibehalten möchten, übergeben Sie gültige Zeiger in den _Parametern lpcbEIDNewEntry_ und _lppEIDNewEntry._</span><span class="sxs-lookup"><span data-stu-id="26a75-140">If you want to retain the entry identifier of the new entry, pass valid pointers in the  _lpcbEIDNewEntry_ and  _lppEIDNewEntry_ parameters.</span></span> <span data-ttu-id="26a75-141">Sie sind dafür verantwortlich, diese Eintrags-ID frei zu machen, wenn Sie damit fertig sind, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="26a75-141">You are responsible for freeing this entry identifier when you are finished with it by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="26a75-142">Um eine bestimmte Vorlage zum Hinzufügen eines neuen Eintrags zu einem veränderbaren Container zu verwenden, verwenden Sie das folgende Verfahren:</span><span class="sxs-lookup"><span data-stu-id="26a75-142">To use a particular template to add a new entry to a modifiable container, use the following procedure:</span></span>
  
1. <span data-ttu-id="26a75-143">Rufen Sie [die IMAPISession::OpenEntry-Methode](imapisession-openentry.md) auf, um den Zielcontainer zu öffnen, und legen Sie den  _lpEntryID-Parameter_ auf den Eintragsbezeichner des Containers fest.</span><span class="sxs-lookup"><span data-stu-id="26a75-143">Call the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open the destination container, and set the  _lpEntryID_ parameter to the entry identifier of the container.</span></span> 
    
2. <span data-ttu-id="26a75-144">Rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des Zielcontainers auf, und legen Sie den  _ulPropTag-Parameter_ auf **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) und den  _lpiid-Parameter_ auf IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="26a75-144">Call the destination container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, and set the  _ulPropTag_ parameter to **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) and the  _lpiid_ parameter to IID_IMAPITable.</span></span> <span data-ttu-id="26a75-145">Der Container gibt eine einmal aufgeführte Tabelle zurück, in der alle Vorlagen aufgeführt sind, die er zum Erstellen neuer Einträge unterstützt.</span><span class="sxs-lookup"><span data-stu-id="26a75-145">The container will return a one-off table that lists all the templates that it supports for creating new entries.</span></span> 
    
3. <span data-ttu-id="26a75-146">Rufen Sie die Zeile ab, die die Vorlage für den bestimmten Eintragstyp darstellt, den Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="26a75-146">Retrieve the row that represents the template for the particular type of entry you want to create.</span></span> <span data-ttu-id="26a75-147">Die **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) gibt den Adresstyp an, der von der Vorlage unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="26a75-147">The **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column indicates the address type that is supported by the template.</span></span>
    
4. <span data-ttu-id="26a75-148">Rufen Sie **die NewEntry-Methode** auf, und legen Sie  _lpEIDNewEntryTpl_ auf den Eintragsbezeichner der ausgewählten Vorlage.</span><span class="sxs-lookup"><span data-stu-id="26a75-148">Call the **NewEntry** method, and set  _lpEIDNewEntryTpl_ to the entry identifier of the selected template.</span></span> <span data-ttu-id="26a75-149">Der Eintragsbezeichner ist die **spalte PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) aus der Zeile der Vorlage in der Einmaltabelle.</span><span class="sxs-lookup"><span data-stu-id="26a75-149">The entry identifier will be the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column from the template's row in the one-off table.</span></span> <span data-ttu-id="26a75-150">Übergeben Sie null in  _cbEIDContainer_ und NULL in  _lpEIDContainer_.</span><span class="sxs-lookup"><span data-stu-id="26a75-150">Pass zero in  _cbEIDContainer_ and NULL in  _lpEIDContainer_.</span></span> <span data-ttu-id="26a75-151">Übergeben Sie einen gültigen Zeiger im  _lppEIDNewEntry-Parameter,_ wenn Sie den Eintragsbezeichner des neuen Eintrags beibehalten möchten.</span><span class="sxs-lookup"><span data-stu-id="26a75-151">Pass a valid pointer in the  _lppEIDNewEntry_ parameter if you want to retain the new entry's entry identifier.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="26a75-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26a75-152">See also</span></span>



[<span data-ttu-id="26a75-153">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="26a75-153">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="26a75-154">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="26a75-154">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="26a75-155">PidTagCreateTemplates (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="26a75-155">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="26a75-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="26a75-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

