---
title: Erstellen einer Verteilerliste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b63a6024-910d-4569-a3b4-c3ebf0b32c3d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5fe588b31de1c84f1eba3633252cd265760fe378
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631073"
---
# <a name="creating-a-distribution-list"></a>Erstellen einer Verteilerliste

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients können eine Verteilerliste direkt in einem modifizierbaren Container wie dem persönlichen Adressbuch (PAB) erstellen.
  
**So erstellen Sie eine Verteilerliste im PAB**
  
1. Erstellen Sie ein Eigenschaftentagarray der Größe mit einem Eigenschaftentag, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), wie folgt:
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. Rufen Sie [IAddrBook::GetPAB](iaddrbook-getpab.md) auf, um den Eintragsbezeichner des PAB abzurufen. Wenn ein Fehler auftritt oder **GetPAB** Null oder NULL zurückgibt, fahren Sie nicht fort. 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. Rufen Sie [IAddrBook::OpenEntry](iaddrbook-openentry.md) auf, um das PAB zu öffnen. Der  _ulObjType-Ausgabeparameter_ sollte auf MAPI_ABCONT festgelegt werden. 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des PAB auf, um die PR_DEF_CREATE_DL-Eigenschaft abzurufen, die Vorlage, die zum Erstellen einer Verteilerliste verwendet wird. 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. Wenn **GetProps** fehlschlägt: 
    
   1. Rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des PAB auf, um die **eigenschaft PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) mit der **IMAPITable-Schnittstelle** zu öffnen. 
      
   2. Erstellen Sie eine Eigenschaftseinschränkung, um nach der Zeile zu suchen, deren **spalte PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) gleich "MAPIPDL" ist. 
      
   3. Rufen Sie [IMAPITable::FindRow](imapitable-findrow.md) auf, um diese Zeile zu suchen. 
    
6. Speichern Sie den Von GetProps oder **FindRow** **zurückgegebenen Eintragsbezeichner.**
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. Rufen Sie die [IABContainer::CreateEntry-Methode](iabcontainer-createentry.md) des PAB auf, um einen neuen Eintrag mithilfe der Vorlage zu erstellen, die durch den gespeicherten Eintragsbezeichner dargestellt wird. Gehen Sie nicht davon aus, dass es sich bei dem zurückgegebenen Objekt um eine Verteilerliste und nicht um einen Messagingbenutzer handelt, wenn dieser Anruf remote ist. Beachten Sie, dass das flag CREATE_CHECK_DUP im  _ulFlags-Parameter_ übergeben wird, um zu verhindern, dass der Eintrag zweimal hinzugefügt wird. 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. Rufen Sie die **IUnknown::QueryInterface-Methode** des neuen Eintrags auf, und übergeben Sie IID_IDistList als Schnittstellenbezeichner, um zu ermitteln, ob der Eintrag eine Verteilerliste ist und die [IDistList : IMAPIContainer-Schnittstelle](idistlistimapicontainer.md) unterstützt. Da **CreateEntry** einen **IMAPIProp-Zeiger** anstelle des spezifischeren **IMailUser-** oder **IDistList-Zeigers** zurückgibt, überprüfen Sie, ob ein Verteilerlistenobjekt erstellt wurde. Wenn **QueryInterface** erfolgreich ist, können Sie sicher sein, dass Sie eine Verteilerliste anstelle eines Messagingbenutzers erstellt haben. 
    
9. Rufen Sie die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) der Verteilerliste auf, um den Anzeigenamen und andere Eigenschaften festzulegen. 
    
10. Rufen Sie die [IABContainer::CreateEntry-Methode](iabcontainer-createentry.md) der Verteilerliste auf, um einen oder mehrere Messagingbenutzer hinzuzufügen. 
    
11. Rufen Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der Verteilerliste auf, wenn Sie bereit sind, sie zu speichern. Um den Eintragsbezeichner der gespeicherten Verteilerliste abzurufen, legen Sie das KEEP_OPEN_READWRITE Flag fest, und rufen Sie dann [IMAPIProp::GetProps auf,](imapiprop-getprops.md) das die **eigenschaft PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) anfordert.
    
12. Release the new distribution list and the PAB by calling their **IUnknown::Release** methods. 
    
13. Rufen Sie [MAPIFreeBuffer](mapifreebuffer.md) auf, um den Speicher für den Eintragsbezeichner des PAB und das Array der Eigenschaftentags der Größe freizugeben. 
    

