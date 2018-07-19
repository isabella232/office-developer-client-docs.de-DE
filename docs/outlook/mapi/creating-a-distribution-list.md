---
title: Erstellen einer Verteilerliste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b63a6024-910d-4569-a3b4-c3ebf0b32c3d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 82fa28f021dbb839c7bb05974682f0bb24174bb2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791475"
---
# <a name="creating-a-distribution-list"></a><span data-ttu-id="31898-103">Erstellen einer Verteilerliste</span><span class="sxs-lookup"><span data-stu-id="31898-103">Creating a distribution list</span></span>

<span data-ttu-id="31898-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="31898-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="31898-105">Clients können direkt in einem Container geändert werden wie das persönliche Adressbuch (PAB) erstellt eine Verteilerliste zu.</span><span class="sxs-lookup"><span data-stu-id="31898-105">Clients can create a distribution list directly into a modifiable container such as the personal address book (PAB).</span></span>
  
<span data-ttu-id="31898-106">**Erstellt eine Verteilerliste in PAB**</span><span class="sxs-lookup"><span data-stu-id="31898-106">**To create a distribution list in the PAB**</span></span>
  
1. <span data-ttu-id="31898-107">Erstellen Sie ein Array-Größe Eigenschaft Tag mit einer Eigenschaftentag, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) wie folgt:</span><span class="sxs-lookup"><span data-stu-id="31898-107">Create a sized property tag array with one property tag, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), as follows:</span></span>
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. <span data-ttu-id="31898-108">Rufen Sie [IAddrBook::GetPAB](iaddrbook-getpab.md) , um die Eintrags-ID des PAB abzurufen.</span><span class="sxs-lookup"><span data-stu-id="31898-108">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> <span data-ttu-id="31898-109">Wenn ein Fehler aufgetreten ist, oder **GetPAB** 0 (null) oder NULL gibt, fahren Sie fort.</span><span class="sxs-lookup"><span data-stu-id="31898-109">If there is an error or **GetPAB** returns zero or NULL, do not continue.</span></span> 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. <span data-ttu-id="31898-110">Rufen Sie [IAddrBook::OpenEntry](iaddrbook-openentry.md) , um die PAB zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="31898-110">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the PAB.</span></span> <span data-ttu-id="31898-111">Der _UlObjType_ Output-Parameter sollte auf MAPI_ABCONT festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="31898-111">The  _ulObjType_ output parameter should be set to MAPI_ABCONT.</span></span> 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. <span data-ttu-id="31898-112">Rufen Sie die PAB [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen der PR_DEF_CREATE_DL-Eigenschaft, die Vorlage, der zum Erstellen einer Verteilerliste verwendet.</span><span class="sxs-lookup"><span data-stu-id="31898-112">Call the PAB's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the PR_DEF_CREATE_DL property, the template that it uses to create a distribution list.</span></span> 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. <span data-ttu-id="31898-113">Wenn **GetProps** ein Fehler auftritt:</span><span class="sxs-lookup"><span data-stu-id="31898-113">If **GetProps** fails:</span></span> 
    
   1. <span data-ttu-id="31898-114">Rufen Sie die PAB [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode zum Öffnen der **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md))-Eigenschaft mit der **IMAPITable** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="31898-114">Call the PAB's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> 
      
   2. <span data-ttu-id="31898-115">Erstellen Sie eine Eigenschaft Beschränkung Suche nach der Zeile mit der **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) Spalte gleich "MAPIPDL."</span><span class="sxs-lookup"><span data-stu-id="31898-115">Create a property restriction to search for the row with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column equal to "MAPIPDL."</span></span> 
      
   3. <span data-ttu-id="31898-116">Rufen Sie [IMAPITable](imapitable-findrow.md) , um diese Zeile zu suchen.</span><span class="sxs-lookup"><span data-stu-id="31898-116">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate this row.</span></span> 
    
6. <span data-ttu-id="31898-117">Speichern Sie die Eintrags-ID von **GetProps** oder **FindRow**zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="31898-117">Save the entry identifier returned by either **GetProps** or **FindRow**.</span></span>
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. <span data-ttu-id="31898-118">Rufen Sie die PAB [IABContainer::CreateEntry](iabcontainer-createentry.md) -Methode, um einen neuen Eintrag mit der Vorlage, dargestellt durch die gespeicherte Eintrags-ID zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="31898-118">Call the PAB's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new entry using the template represented by the saved entry identifier.</span></span> <span data-ttu-id="31898-119">Gehen Sie nicht, dass das zurückgegebene Objekt eine Verteilerliste, statt ein messaging-Benutzer werden wird, wenn dieses Anrufs Remote übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="31898-119">Do not assume that the object returned will be a distribution list rather than a messaging user when this call is remoted.</span></span> <span data-ttu-id="31898-120">Beachten Sie, dass das Flag CREATE_CHECK_DUP übergeben wird, in der _UlFlags_ -Parameter, um zu verhindern, dass den Eintrag zweimal hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="31898-120">Notice that the CREATE_CHECK_DUP flag is passed in the  _ulFlags_ parameter to prevent the entry from being added twice.</span></span> 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. <span data-ttu-id="31898-121">Rufen Sie den neuen Eintrag **QueryInterface** -Methode, übergeben IID_IDistList als Schnittstellenbezeichner, um festzustellen, ob der Eintrag eine Verteilerliste ist und unterstützt die [IDistList: IMAPIContainer](idistlistimapicontainer.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="31898-121">Call the new entry's **IUnknown::QueryInterface** method, passing IID_IDistList as the interface identifier, to determine if the entry is a distribution list and supports the [IDistList : IMAPIContainer](idistlistimapicontainer.md) interface.</span></span> <span data-ttu-id="31898-122">Da **CreateEntry** einen Zeiger **IMAPIProp** statt der genauere **IMailUser** oder **IDistList** Zeiger zurückgegeben wird, überprüfen Sie, dass ein Verteilung List-Objekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="31898-122">Because **CreateEntry** returns an **IMAPIProp** pointer rather than the more specific **IMailUser** or **IDistList** pointer, check that a distribution list object was created.</span></span> <span data-ttu-id="31898-123">Wenn **QueryInterface** erfolgreich ist, können Sie sicher sein, dass Sie eine Verteilerliste, statt ein messaging-Benutzer erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="31898-123">If **QueryInterface** succeeds, you can be sure that you have created a distribution list rather than a messaging user.</span></span> 
    
9. <span data-ttu-id="31898-124">Rufen Sie die Verteilerliste [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode, um den Anzeigenamen und andere Eigenschaften festzulegen.</span><span class="sxs-lookup"><span data-stu-id="31898-124">Call the distribution list's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set its display name and other properties.</span></span> 
    
10. <span data-ttu-id="31898-125">Rufen Sie die Verteilerliste [IABContainer::CreateEntry](iabcontainer-createentry.md) -Methode, um einen oder mehrere messaging Benutzer hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="31898-125">Call the distribution list's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to add one or more messaging users.</span></span> 
    
11. <span data-ttu-id="31898-126">Rufen Sie die Verteilerliste [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, wenn Sie bereit sind, speichern Sie es.</span><span class="sxs-lookup"><span data-stu-id="31898-126">Call the distribution list's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when you're ready to save it.</span></span> <span data-ttu-id="31898-127">Zum Abrufen der Eintrags-ID der gespeicherten Verteilerliste legen Sie das Flag KEEP_OPEN_READWRITE, und rufen Sie dann [IMAPIProp::GetProps](imapiprop-getprops.md) anfordern die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="31898-127">To retrieve the entry identifier of the saved distribution list, set the KEEP_OPEN_READWRITE flag and then call [IMAPIProp::GetProps](imapiprop-getprops.md) requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
12. <span data-ttu-id="31898-128">Lassen Sie die neue Verteilerliste und PAB durch ihre **IUnknown** -Methoden aufrufen.</span><span class="sxs-lookup"><span data-stu-id="31898-128">Release the new distribution list and the PAB by calling their **IUnknown::Release** methods.</span></span> 
    
13. <span data-ttu-id="31898-129">Rufen Sie [MAPIFreeBuffer](mapifreebuffer.md) , um den Speicher für die Eintrags-ID der PAB und die Array-Größe Eigenschaft Tag freizugeben.</span><span class="sxs-lookup"><span data-stu-id="31898-129">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the memory for the entry identifier of the PAB and the sized property tag array.</span></span> 
    

