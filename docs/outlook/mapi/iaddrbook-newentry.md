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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336715"
---
# <a name="iaddrbooknewentry"></a><span data-ttu-id="7a360-103">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="7a360-103">IAddrBook::NewEntry</span></span>

  
  
<span data-ttu-id="7a360-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a360-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a360-105">Fügt einen neuen Empfänger zu einem Adressbuchcontainer oder zur Empfängerliste einer ausgehenden Nachricht hinzu.</span><span class="sxs-lookup"><span data-stu-id="7a360-105">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="7a360-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a360-106">Parameters</span></span>

 <span data-ttu-id="7a360-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7a360-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="7a360-108">in Ein Handle für das übergeordnete Fenster für das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="7a360-108">[in] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="7a360-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7a360-109">_ulFlags_</span></span>
  
> <span data-ttu-id="7a360-110">in Eine Bitmaske von Flags, die den Typ des verwendeten Texts steuert.</span><span class="sxs-lookup"><span data-stu-id="7a360-110">[in] A bitmask of flags that controls the type of the text that is used.</span></span> <span data-ttu-id="7a360-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7a360-111">The following flag can be set:</span></span>
    
<span data-ttu-id="7a360-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7a360-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7a360-113">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="7a360-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="7a360-114">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="7a360-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="7a360-115">_cbEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="7a360-115">_cbEIDContainer_</span></span>
  
> <span data-ttu-id="7a360-116">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEIDContainer_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7a360-116">[in] The byte count in the entry identifier pointed to by the  _lpEIDContainer_ parameter.</span></span> 
    
 <span data-ttu-id="7a360-117">_lpEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="7a360-117">_lpEIDContainer_</span></span>
  
> <span data-ttu-id="7a360-118">in Ein Zeiger auf die Eintrags-ID des Containers, in dem der neue Empfänger hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7a360-118">[in] A pointer to the entry identifier of the container where the new recipient is to be added.</span></span> <span data-ttu-id="7a360-119">Wenn der _cbEIDContainer_ -Parameter 0 (NULL \*\*\*\* ) ist, gibt die neuentry-Methode eine Empfänger Eintrags-ID und eine Liste von Vorlagen zurück, als ob die [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) -Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="7a360-119">If the  _cbEIDContainer_ parameter is zero, the **NewEntry** method returns a recipient entry identifier and a list of templates as if the [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) method was called.</span></span> 
    
 <span data-ttu-id="7a360-120">_cbEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="7a360-120">_cbEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="7a360-121">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEIDNewEntryTpl_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7a360-121">[in] The byte count in the entry identifier pointed to by the  _lpEIDNewEntryTpl_ parameter.</span></span> 
    
 <span data-ttu-id="7a360-122">_lpEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="7a360-122">_lpEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="7a360-123">in Ein Zeiger auf eine einmalige Vorlage, die zum Erstellen des neuen Empfängers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7a360-123">[in] A pointer to a one-off template that will be used to create the new recipient.</span></span> <span data-ttu-id="7a360-124">Wenn _cbEIDNewEntryTpl_ ist und _lpEIDNewEntryTpl_ NULL ist, zeigt der neue **Eintrag** ein Dialogfeld an, in dem der Benutzer aus einer Liste von Vorlagen zum Hinzufügen neuer Einträge auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="7a360-124">If  _cbEIDNewEntryTpl_ is zero and  _lpEIDNewEntryTpl_ is NULL, **NewEntry** displays a dialog box with which the user can select from a list of templates for adding new entries.</span></span> 
    
 <span data-ttu-id="7a360-125">_lpcbEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="7a360-125">_lpcbEIDNewEntry_</span></span>
  
> <span data-ttu-id="7a360-126">Out Ein Zeiger auf die Bytezahl in der Eintrags-ID, auf die durch den _lppEIDNewEntry_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7a360-126">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEIDNewEntry_ parameter.</span></span> 
    
 <span data-ttu-id="7a360-127">_lppEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="7a360-127">_lppEIDNewEntry_</span></span>
  
> <span data-ttu-id="7a360-128">Out Ein Zeiger auf einen Zeiger auf die Eintrags-ID des neuen Empfängers.</span><span class="sxs-lookup"><span data-stu-id="7a360-128">[out] A pointer to a pointer to the new recipient's entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7a360-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a360-129">Return value</span></span>

<span data-ttu-id="7a360-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a360-130">S_OK</span></span> 
  
> <span data-ttu-id="7a360-131">Der neue Adressbucheintrag wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="7a360-131">The new address book entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7a360-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a360-132">Remarks</span></span>

<span data-ttu-id="7a360-133">Mit \*\*\*\* der neuentry-Methode wird ein neuer Adressbucheintrag erstellt, der direkt zu einem Container hinzugefügt oder zur Behebung einer ausgehenden Nachricht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7a360-133">The **NewEntry** method creates a new address book entry, to be added directly into a container or to be used to address an outgoing message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7a360-134">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="7a360-134">Notes to callers</span></span>

<span data-ttu-id="7a360-135">Wenn der neue Eintrag einem bestimmten Container hinzugefügt werden soll, legen Sie _lpEIDContainer_ auf die Eintrags-ID des Containers und _cbEIDContainer_ auf die Bytezahl in der Eintrags-ID fest.</span><span class="sxs-lookup"><span data-stu-id="7a360-135">If you want the new entry to be added to a specific container, set  _lpEIDContainer_ to the container's entry identifier and  _cbEIDContainer_ to the byte count in the entry identifier.</span></span> 
  
<span data-ttu-id="7a360-136">Wenn der neue Eintrag der Empfängerliste einer ausgehenden Nachricht hinzugefügt werden soll, legen Sie _lpEIDContainer_ auf NULL und _cbEIDContainer_ auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="7a360-136">If you want the new entry to be added to the recipient list of an outgoing message, set  _lpEIDContainer_ to NULL and  _cbEIDContainer_ to zero.</span></span> 
  
<span data-ttu-id="7a360-137">Wenn Sie dem Benutzer einer Clientanwendung erlauben möchten, den Typ des zu erstellenden Eintrags auszuwählen, überschreiten Sie NULL in _cbEIDNewEntryTpl_ und NULL in _lpEIDNewEntryTpl_.</span><span class="sxs-lookup"><span data-stu-id="7a360-137">If you want to allow the user of a client application to select the type of entry to be created, pass zero in  _cbEIDNewEntryTpl_ and NULL in  _lpEIDNewEntryTpl_.</span></span> <span data-ttu-id="7a360-138">Die \*\*\*\* Posteingangs Methode zeigt die MAPI-einmalige Tabelle, eine Liste der von MAPI unterstützten Vorlagen und jedes Adressbuch Anbieters in der Sitzung an.</span><span class="sxs-lookup"><span data-stu-id="7a360-138">The **NewEntry** method displays the MAPI one-off table, a list of templates supported by MAPI and by each address book provider in the session.</span></span> <span data-ttu-id="7a360-139">Jede Vorlage kann einen Empfängereintrag für einen oder mehrere Adresstypen erstellen.</span><span class="sxs-lookup"><span data-stu-id="7a360-139">Each template can create a recipient entry for one or more address types.</span></span> 
  
<span data-ttu-id="7a360-140">Wenn Sie die Eintrags-ID des neuen Eintrags behalten möchten, übergeben Sie gültige Zeiger in den Parametern _lpcbEIDNewEntry_ und _lppEIDNewEntry_ .</span><span class="sxs-lookup"><span data-stu-id="7a360-140">If you want to retain the entry identifier of the new entry, pass valid pointers in the  _lpcbEIDNewEntry_ and  _lppEIDNewEntry_ parameters.</span></span> <span data-ttu-id="7a360-141">Sie sind für die Freigabe dieser Eintrags-ID verantwortlich, wenn Sie damit fertig sind, indem Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7a360-141">You are responsible for freeing this entry identifier when you are finished with it by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="7a360-142">Gehen Sie folgendermaßen vor, um eine bestimmte Vorlage zum Hinzufügen eines neuen Eintrags zu einem änderbaren Container zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="7a360-142">To use a particular template to add a new entry to a modifiable container, use the following procedure:</span></span>
  
1. <span data-ttu-id="7a360-143">Rufen Sie die [IMAPISession:: OpenEntry](imapisession-openentry.md) -Methode auf, um den Zielcontainer zu öffnen, und legen Sie den Parameter _lpEntryID_ auf den Eintragsbezeichner des Containers fest.</span><span class="sxs-lookup"><span data-stu-id="7a360-143">Call the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open the destination container, and set the  _lpEntryID_ parameter to the entry identifier of the container.</span></span> 
    
2. <span data-ttu-id="7a360-144">Rufen Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode des Zielcontainers auf, und legen Sie den Parameter _ulPropTag_ auf **PR_CREATE_TEMPLATES** ([pidtagcreatetemplates (](pidtagcreatetemplates-canonical-property.md)) und den _lpIID_ -Parameter auf IID_IMAPITable fest.</span><span class="sxs-lookup"><span data-stu-id="7a360-144">Call the destination container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, and set the  _ulPropTag_ parameter to **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) and the  _lpiid_ parameter to IID_IMAPITable.</span></span> <span data-ttu-id="7a360-145">Der Container gibt eine einmalige Tabelle zurück, in der alle Vorlagen aufgeführt sind, die für das Erstellen neuer Einträge unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7a360-145">The container will return a one-off table that lists all the templates that it supports for creating new entries.</span></span> 
    
3. <span data-ttu-id="7a360-146">Rufen Sie die Zeile ab, die die Vorlage für den jeweiligen Eintragstyp darstellt, den Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="7a360-146">Retrieve the row that represents the template for the particular type of entry you want to create.</span></span> <span data-ttu-id="7a360-147">Die **PR_ADDRTYPE** ([pidtagaddresstype (](pidtagaddresstype-canonical-property.md)) gibt den von der Vorlage unterstützten Adresstyp an.</span><span class="sxs-lookup"><span data-stu-id="7a360-147">The **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column indicates the address type that is supported by the template.</span></span>
    
4. <span data-ttu-id="7a360-148">Rufen Sie \*\*\*\* die neuentry-Methode auf, und legen Sie _lpEIDNewEntryTpl_ auf die Eintrags-ID der ausgewählten Vorlage fest.</span><span class="sxs-lookup"><span data-stu-id="7a360-148">Call the **NewEntry** method, and set  _lpEIDNewEntryTpl_ to the entry identifier of the selected template.</span></span> <span data-ttu-id="7a360-149">Die Eintrags-ID ist die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Spalte aus der Zeile der Vorlage in der einmaligen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7a360-149">The entry identifier will be the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column from the template's row in the one-off table.</span></span> <span data-ttu-id="7a360-150">NULL in _cbEIDContainer_ und NULL in _lpEIDContainer_.</span><span class="sxs-lookup"><span data-stu-id="7a360-150">Pass zero in  _cbEIDContainer_ and NULL in  _lpEIDContainer_.</span></span> <span data-ttu-id="7a360-151">Übergeben Sie einen gültigen Zeiger im _lppEIDNewEntry_ -Parameter, wenn Sie die Eintrags-ID des neuen Eintrags aufbewahren möchten.</span><span class="sxs-lookup"><span data-stu-id="7a360-151">Pass a valid pointer in the  _lppEIDNewEntry_ parameter if you want to retain the new entry's entry identifier.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7a360-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a360-152">See also</span></span>



[<span data-ttu-id="7a360-153">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="7a360-153">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="7a360-154">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="7a360-154">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="7a360-155">Kanonische Pidtagcreatetemplates (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7a360-155">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="7a360-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7a360-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

