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
ms.openlocfilehash: 7108ae215562169244100a56cc9b9208d78b1893
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424175"
---
# <a name="creating-a-distribution-list"></a><span data-ttu-id="8c4aa-103">Erstellen einer Verteilerliste</span><span class="sxs-lookup"><span data-stu-id="8c4aa-103">Creating a distribution list</span></span>

<span data-ttu-id="8c4aa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c4aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c4aa-105">Clients können eine Verteilerliste direkt in einem änderbaren Container wie dem persönlichen Adressbuch (PAB) erstellen.</span><span class="sxs-lookup"><span data-stu-id="8c4aa-105">Clients can create a distribution list directly into a modifiable container such as the personal address book (PAB).</span></span>
  
<span data-ttu-id="8c4aa-106">**So erstellen Sie eine Verteilerliste im PAB**</span><span class="sxs-lookup"><span data-stu-id="8c4aa-106">**To create a distribution list in the PAB**</span></span>
  
1. <span data-ttu-id="8c4aa-107">Erstellen Sie ein Größe-Tag-Array mit einem Property-Tag, **PR_DEF_CREATE_DL** ([pidtagdefcreatedl (](pidtagdefcreatedl-canonical-property.md)), wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8c4aa-107">Create a sized property tag array with one property tag, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), as follows:</span></span>
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. <span data-ttu-id="8c4aa-108">Rufen Sie [IAddrBook:: GetPAB](iaddrbook-getpab.md) auf, um den Eintragsbezeichner des PAB abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8c4aa-108">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> <span data-ttu-id="8c4aa-109">Wenn ein Fehler vorliegt oder **GetPAB** NULL oder NULL zurückgibt, fahren Sie nicht fort.</span><span class="sxs-lookup"><span data-stu-id="8c4aa-109">If there is an error or **GetPAB** returns zero or NULL, do not continue.</span></span> 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. <span data-ttu-id="8c4aa-110">Rufen Sie [IAddrBook:: OpenEntry](iaddrbook-openentry.md) auf, um das PAB zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8c4aa-110">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the PAB.</span></span> <span data-ttu-id="8c4aa-111">Der _ulObjType_ -Ausgabeparameter sollte auf MAPI_ABCONT festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8c4aa-111">The  _ulObjType_ output parameter should be set to MAPI_ABCONT.</span></span> 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. <span data-ttu-id="8c4aa-112">Rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des PAB auf, um die PR_DEF_CREATE_DL-Eigenschaft abzurufen, die Sie zum Erstellen einer Verteilerliste verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c4aa-112">Call the PAB's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the PR_DEF_CREATE_DL property, the template that it uses to create a distribution list.</span></span> 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. <span data-ttu-id="8c4aa-113">Wenn \*\*\*\* GetProps fehlschlägt:</span><span class="sxs-lookup"><span data-stu-id="8c4aa-113">If **GetProps** fails:</span></span> 
    
   1. <span data-ttu-id="8c4aa-114">Rufen Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode des PAB auf, um die **PR_CREATE_TEMPLATES** ([pidtagcreatetemplates (](pidtagcreatetemplates-canonical-property.md))-Eigenschaft mit der **IMAPITable** -Schnittstelle zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8c4aa-114">Call the PAB's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> 
      
   2. <span data-ttu-id="8c4aa-115">Erstellen Sie eine Eigenschaftseinschränkung, um nach der Zeile mit der **PR_ADDRTYPE** ([pidtagaddresstype (](pidtagaddresstype-canonical-property.md))-Spalte gleich "MAPIPDL" zu suchen.</span><span class="sxs-lookup"><span data-stu-id="8c4aa-115">Create a property restriction to search for the row with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column equal to "MAPIPDL."</span></span> 
      
   3. <span data-ttu-id="8c4aa-116">Rufen Sie [IMAPITable:: FindRow](imapitable-findrow.md) auf, um diese Zeile zu suchen.</span><span class="sxs-lookup"><span data-stu-id="8c4aa-116">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate this row.</span></span> 
    
6. <span data-ttu-id="8c4aa-117">Speichern Sie die Eintrags-ID \*\*\*\* , die von GetProps oder **FindRow**zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8c4aa-117">Save the entry identifier returned by either **GetProps** or **FindRow**.</span></span>
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. <span data-ttu-id="8c4aa-118">Rufen Sie die [IABContainer:: CreateEntry](iabcontainer-createentry.md) -Methode des PAB auf, um einen neuen Eintrag mithilfe der Vorlage zu erstellen, die durch die gespeicherte Eintrags-ID dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8c4aa-118">Call the PAB's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new entry using the template represented by the saved entry identifier.</span></span> <span data-ttu-id="8c4aa-119">Gehen Sie nicht davon aus, dass das zurückgegebene Objekt eine Verteilerliste anstelle eines Messaging Benutzers ist, wenn dieser Aufruf Remote ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8c4aa-119">Do not assume that the object returned will be a distribution list rather than a messaging user when this call is remoted.</span></span> <span data-ttu-id="8c4aa-120">Beachten Sie, dass das CREATE_CHECK_DUP-Flag im _ulFlags_ -Parameter übergeben wird, um zu verhindern, dass der Eintrag zweimal hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="8c4aa-120">Notice that the CREATE_CHECK_DUP flag is passed in the  _ulFlags_ parameter to prevent the entry from being added twice.</span></span> 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. <span data-ttu-id="8c4aa-121">Rufen Sie die **IUnknown:: QueryInterface** -Methode des neuen Eintrags auf, übergeben Sie IID_IDistList als Schnittstellenbezeichner, um zu ermitteln, ob es sich bei dem Eintrag um eine Verteilerliste handelt, und unterstützt die [IDistList: IMAPIContainer](idistlistimapicontainer.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8c4aa-121">Call the new entry's **IUnknown::QueryInterface** method, passing IID_IDistList as the interface identifier, to determine if the entry is a distribution list and supports the [IDistList : IMAPIContainer](idistlistimapicontainer.md) interface.</span></span> <span data-ttu-id="8c4aa-122">Da **CreateEntry** einen **IMAPIProp** -Zeiger anstelle des spezifischeren **IMailUser** -oder **IDistList** -Zeigers zurückgibt, überprüfen Sie, ob ein Verteilerlistenobjekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8c4aa-122">Because **CreateEntry** returns an **IMAPIProp** pointer rather than the more specific **IMailUser** or **IDistList** pointer, check that a distribution list object was created.</span></span> <span data-ttu-id="8c4aa-123">Wenn **QueryInterface** erfolgreich ist, können Sie sicher sein, dass Sie eine Verteilerliste anstelle eines Messaging Benutzers erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="8c4aa-123">If **QueryInterface** succeeds, you can be sure that you have created a distribution list rather than a messaging user.</span></span> 
    
9. <span data-ttu-id="8c4aa-124">Rufen Sie die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode der Verteilerliste auf, um den Anzeigenamen und andere Eigenschaften festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8c4aa-124">Call the distribution list's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set its display name and other properties.</span></span> 
    
10. <span data-ttu-id="8c4aa-125">Rufen Sie die [IABContainer:: CreateEntry](iabcontainer-createentry.md) -Methode der Verteilerliste auf, um einen oder mehrere Messagingbenutzer hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="8c4aa-125">Call the distribution list's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to add one or more messaging users.</span></span> 
    
11. <span data-ttu-id="8c4aa-126">Rufen Sie die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode der Verteilerliste auf, wenn Sie Sie speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="8c4aa-126">Call the distribution list's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when you're ready to save it.</span></span> <span data-ttu-id="8c4aa-127">Um den Eintragsbezeichner der gespeicherten Verteilerliste abzurufen, legen Sie das KEEP_OPEN_READWRITE-Flag fest, und rufen Sie dann [IMAPIProp::](imapiprop-getprops.md) GetProps auf, das die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft anfordert.</span><span class="sxs-lookup"><span data-stu-id="8c4aa-127">To retrieve the entry identifier of the saved distribution list, set the KEEP_OPEN_READWRITE flag and then call [IMAPIProp::GetProps](imapiprop-getprops.md) requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
12. <span data-ttu-id="8c4aa-128">Veröffentlichen Sie die neue Verteilerliste und das PAB, indem Sie Ihre **IUnknown:: Release** -Methoden aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8c4aa-128">Release the new distribution list and the PAB by calling their **IUnknown::Release** methods.</span></span> 
    
13. <span data-ttu-id="8c4aa-129">Rufen Sie [mapifreebufferfreigegeben](mapifreebuffer.md) auf, um den Speicher für die Eintrags-ID des PAB und das Array der sized-Eigenschaftstags freizugeben.</span><span class="sxs-lookup"><span data-stu-id="8c4aa-129">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the memory for the entry identifier of the PAB and the sized property tag array.</span></span> 
    

