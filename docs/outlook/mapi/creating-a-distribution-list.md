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
ms.openlocfilehash: f0a6b7af196073d52ce98037b443569dcd1f41e6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582546"
---
# <a name="creating-a-distribution-list"></a>Erstellen einer Verteilerliste

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Clients können direkt in einem Container geändert werden wie das persönliche Adressbuch (PAB) erstellt eine Verteilerliste zu.
  
**Erstellt eine Verteilerliste in PAB**
  
1. Erstellen Sie ein Array-Größe Eigenschaft Tag mit einer Eigenschaftentag, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) wie folgt:
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. Rufen Sie [IAddrBook::GetPAB](iaddrbook-getpab.md) , um die Eintrags-ID des PAB abzurufen. Wenn ein Fehler aufgetreten ist, oder **GetPAB** 0 (null) oder NULL gibt, fahren Sie fort. 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. Rufen Sie [IAddrBook::OpenEntry](iaddrbook-openentry.md) , um die PAB zu öffnen. Der _UlObjType_ Output-Parameter sollte auf MAPI_ABCONT festgelegt werden. 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. Rufen Sie die PAB [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen der PR_DEF_CREATE_DL-Eigenschaft, die Vorlage, der zum Erstellen einer Verteilerliste verwendet. 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. Wenn **GetProps** ein Fehler auftritt: 
    
   1. Rufen Sie die PAB [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode zum Öffnen der **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md))-Eigenschaft mit der **IMAPITable** -Schnittstelle. 
      
   2. Erstellen Sie eine Eigenschaft Beschränkung Suche nach der Zeile mit der **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) Spalte gleich "MAPIPDL." 
      
   3. Rufen Sie [IMAPITable](imapitable-findrow.md) , um diese Zeile zu suchen. 
    
6. Speichern Sie die Eintrags-ID von **GetProps** oder **FindRow**zurückgegeben wird.
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. Rufen Sie die PAB [IABContainer::CreateEntry](iabcontainer-createentry.md) -Methode, um einen neuen Eintrag mit der Vorlage, dargestellt durch die gespeicherte Eintrags-ID zu erstellen. Gehen Sie nicht, dass das zurückgegebene Objekt eine Verteilerliste, statt ein messaging-Benutzer werden wird, wenn dieses Anrufs Remote übergeben wird. Beachten Sie, dass das Flag CREATE_CHECK_DUP übergeben wird, in der _UlFlags_ -Parameter, um zu verhindern, dass den Eintrag zweimal hinzugefügt wird. 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. Rufen Sie den neuen Eintrag **QueryInterface** -Methode, übergeben IID_IDistList als Schnittstellenbezeichner, um festzustellen, ob der Eintrag eine Verteilerliste ist und unterstützt die [IDistList: IMAPIContainer](idistlistimapicontainer.md) Schnittstelle. Da **CreateEntry** einen Zeiger **IMAPIProp** statt der genauere **IMailUser** oder **IDistList** Zeiger zurückgegeben wird, überprüfen Sie, dass ein Verteilung List-Objekt erstellt wurde. Wenn **QueryInterface** erfolgreich ist, können Sie sicher sein, dass Sie eine Verteilerliste, statt ein messaging-Benutzer erstellt haben. 
    
9. Rufen Sie die Verteilerliste [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode, um den Anzeigenamen und andere Eigenschaften festzulegen. 
    
10. Rufen Sie die Verteilerliste [IABContainer::CreateEntry](iabcontainer-createentry.md) -Methode, um einen oder mehrere messaging Benutzer hinzuzufügen. 
    
11. Rufen Sie die Verteilerliste [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, wenn Sie bereit sind, speichern Sie es. Zum Abrufen der Eintrags-ID der gespeicherten Verteilerliste legen Sie das Flag KEEP_OPEN_READWRITE, und rufen Sie dann [IMAPIProp::GetProps](imapiprop-getprops.md) anfordern die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft.
    
12. Lassen Sie die neue Verteilerliste und PAB durch ihre **IUnknown** -Methoden aufrufen. 
    
13. Rufen Sie [MAPIFreeBuffer](mapifreebuffer.md) , um den Speicher für die Eintrags-ID der PAB und die Array-Größe Eigenschaft Tag freizugeben. 
    

