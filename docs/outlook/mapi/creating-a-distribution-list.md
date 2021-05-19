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
# <a name="creating-a-distribution-list"></a><span data-ttu-id="26564-103">Erstellen einer Verteilerliste</span><span class="sxs-lookup"><span data-stu-id="26564-103">Creating a distribution list</span></span>

<span data-ttu-id="26564-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26564-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26564-105">Clients können eine Verteilerliste direkt in einem veränderbaren Container wie dem persönlichen Adressbuch (PAB) erstellen.</span><span class="sxs-lookup"><span data-stu-id="26564-105">Clients can create a distribution list directly into a modifiable container such as the personal address book (PAB).</span></span>
  
<span data-ttu-id="26564-106">**So erstellen Sie eine Verteilerliste im PAB**</span><span class="sxs-lookup"><span data-stu-id="26564-106">**To create a distribution list in the PAB**</span></span>
  
1. <span data-ttu-id="26564-107">Erstellen Sie ein #A0 mit einem Eigenschaftstag, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), wie folgt:</span><span class="sxs-lookup"><span data-stu-id="26564-107">Create a sized property tag array with one property tag, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), as follows:</span></span>
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. <span data-ttu-id="26564-108">Rufen [Sie IAddrBook::GetPAB auf,](iaddrbook-getpab.md) um die Eintrags-ID des PAB abzurufen.</span><span class="sxs-lookup"><span data-stu-id="26564-108">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> <span data-ttu-id="26564-109">Wenn ein Fehler auftritt oder **GetPAB** Null oder NULL zurückgibt, fahren Sie nicht fort.</span><span class="sxs-lookup"><span data-stu-id="26564-109">If there is an error or **GetPAB** returns zero or NULL, do not continue.</span></span> 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. <span data-ttu-id="26564-110">Rufen [Sie IAddrBook::OpenEntry auf,](iaddrbook-openentry.md) um das PAB zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="26564-110">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the PAB.</span></span> <span data-ttu-id="26564-111">Der  _ulObjType-Ausgabeparameter_ sollte auf MAPI_ABCONT.</span><span class="sxs-lookup"><span data-stu-id="26564-111">The  _ulObjType_ output parameter should be set to MAPI_ABCONT.</span></span> 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. <span data-ttu-id="26564-112">Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des PAB auf, um die PR_DEF_CREATE_DL-Eigenschaft abzurufen, die Vorlage, die zum Erstellen einer Verteilerliste verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="26564-112">Call the PAB's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the PR_DEF_CREATE_DL property, the template that it uses to create a distribution list.</span></span> 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. <span data-ttu-id="26564-113">Wenn **GetProps fehlschlägt:**</span><span class="sxs-lookup"><span data-stu-id="26564-113">If **GetProps** fails:</span></span> 
    
   1. <span data-ttu-id="26564-114">Rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des PAB auf, um die **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) -Eigenschaft mit der **IMAPITable-Schnittstelle zu** öffnen.</span><span class="sxs-lookup"><span data-stu-id="26564-114">Call the PAB's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> 
      
   2. <span data-ttu-id="26564-115">Erstellen Sie eine Eigenschaftseinschränkung, um nach der Zeile mit der Spalte **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) zu suchen, die "MAPIPDL" entspricht.</span><span class="sxs-lookup"><span data-stu-id="26564-115">Create a property restriction to search for the row with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column equal to "MAPIPDL."</span></span> 
      
   3. <span data-ttu-id="26564-116">Rufen [Sie IMAPITable::FindRow auf,](imapitable-findrow.md) um diese Zeile zu finden.</span><span class="sxs-lookup"><span data-stu-id="26564-116">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate this row.</span></span> 
    
6. <span data-ttu-id="26564-117">Speichern Sie die von **GetProps** oder FindRow zurückgegebene **Eintrags-ID.**</span><span class="sxs-lookup"><span data-stu-id="26564-117">Save the entry identifier returned by either **GetProps** or **FindRow**.</span></span>
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. <span data-ttu-id="26564-118">Rufen Sie die [IABContainer::CreateEntry-Methode](iabcontainer-createentry.md) des PAB auf, um einen neuen Eintrag mithilfe der Vorlage zu erstellen, die durch die gespeicherte Eintrags-ID dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="26564-118">Call the PAB's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new entry using the template represented by the saved entry identifier.</span></span> <span data-ttu-id="26564-119">Gehen Sie nicht davon aus, dass es sich bei dem zurückgegebenen Objekt um eine Verteilerliste und nicht um einen Messagingbenutzer handelt, wenn dieser Aufruf remote ist.</span><span class="sxs-lookup"><span data-stu-id="26564-119">Do not assume that the object returned will be a distribution list rather than a messaging user when this call is remoted.</span></span> <span data-ttu-id="26564-120">Beachten Sie, dass CREATE_CHECK_DUP im  _ulFlags-Parameter_ übergeben wird, um zu verhindern, dass der Eintrag zweimal hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="26564-120">Notice that the CREATE_CHECK_DUP flag is passed in the  _ulFlags_ parameter to prevent the entry from being added twice.</span></span> 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. <span data-ttu-id="26564-121">Rufen Sie die **IUnknown::QueryInterface-Methode** des neuen Eintrags auf, übergeben Sie IID_IDistList als Schnittstellenbezeichner, um zu ermitteln, ob es sich bei dem Eintrag um eine Verteilerliste handelt und unterstützt die [IDistList : IMAPIContainer-Schnittstelle.](idistlistimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="26564-121">Call the new entry's **IUnknown::QueryInterface** method, passing IID_IDistList as the interface identifier, to determine if the entry is a distribution list and supports the [IDistList : IMAPIContainer](idistlistimapicontainer.md) interface.</span></span> <span data-ttu-id="26564-122">Da **CreateEntry** einen **IMAPIProp-Zeiger** anstelle des spezifischeren **IMailUser-** oder **IDistList-Zeigers** zurückgibt, überprüfen Sie, ob ein Verteilerlistenobjekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="26564-122">Because **CreateEntry** returns an **IMAPIProp** pointer rather than the more specific **IMailUser** or **IDistList** pointer, check that a distribution list object was created.</span></span> <span data-ttu-id="26564-123">Wenn **QueryInterface** erfolgreich ist, können Sie sicher sein, dass Sie eine Verteilerliste anstelle eines Messagingbenutzers erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="26564-123">If **QueryInterface** succeeds, you can be sure that you have created a distribution list rather than a messaging user.</span></span> 
    
9. <span data-ttu-id="26564-124">Rufen Sie die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) der Verteilerliste auf, um den Anzeigenamen und andere Eigenschaften festlegen.</span><span class="sxs-lookup"><span data-stu-id="26564-124">Call the distribution list's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set its display name and other properties.</span></span> 
    
10. <span data-ttu-id="26564-125">Rufen Sie die [IABContainer::CreateEntry-Methode](iabcontainer-createentry.md) der Verteilerliste auf, um einen oder mehrere Messagingbenutzer hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="26564-125">Call the distribution list's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to add one or more messaging users.</span></span> 
    
11. <span data-ttu-id="26564-126">Rufen Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der Verteilerliste auf, wenn Sie zum Speichern bereit sind.</span><span class="sxs-lookup"><span data-stu-id="26564-126">Call the distribution list's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when you're ready to save it.</span></span> <span data-ttu-id="26564-127">Legen Sie zum Abrufen der Eintrags-ID der gespeicherten Verteilerliste das Flag KEEP_OPEN_READWRITE und rufen Sie [dann IMAPIProp::GetProps](imapiprop-getprops.md) auf, der die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft anfordert.</span><span class="sxs-lookup"><span data-stu-id="26564-127">To retrieve the entry identifier of the saved distribution list, set the KEEP_OPEN_READWRITE flag and then call [IMAPIProp::GetProps](imapiprop-getprops.md) requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
12. <span data-ttu-id="26564-128">Geben Sie die neue Verteilerliste und das PAB frei, indem Sie ihre **IUnknown::Release-Methoden** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="26564-128">Release the new distribution list and the PAB by calling their **IUnknown::Release** methods.</span></span> 
    
13. <span data-ttu-id="26564-129">Rufen [Sie MAPIFreeBuffer auf,](mapifreebuffer.md) um den Arbeitsspeicher für die Eintrags-ID des PAB und das Array des Eigenschaftstags der Größe frei zu geben.</span><span class="sxs-lookup"><span data-stu-id="26564-129">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the memory for the entry identifier of the PAB and the sized property tag array.</span></span> 
    

