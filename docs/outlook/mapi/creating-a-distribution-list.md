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
# <a name="creating-a-distribution-list"></a>Erstellen einer Verteilerliste

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients können eine Verteilerliste direkt in einem änderbaren Container wie dem persönlichen Adressbuch (PAB) erstellen.
  
**So erstellen Sie eine Verteilerliste im PAB**
  
1. Erstellen Sie ein Größe-Tag-Array mit einem Property-Tag, **PR_DEF_CREATE_DL** ([pidtagdefcreatedl (](pidtagdefcreatedl-canonical-property.md)), wie folgt:
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. Rufen Sie [IAddrBook:: GetPAB](iaddrbook-getpab.md) auf, um den Eintragsbezeichner des PAB abzurufen. Wenn ein Fehler vorliegt oder **GetPAB** NULL oder NULL zurückgibt, fahren Sie nicht fort. 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. Rufen Sie [IAddrBook:: OpenEntry](iaddrbook-openentry.md) auf, um das PAB zu öffnen. Der _ulObjType_ -Ausgabeparameter sollte auf MAPI_ABCONT festgelegt werden. 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. Rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des PAB auf, um die PR_DEF_CREATE_DL-Eigenschaft abzurufen, die Sie zum Erstellen einer Verteilerliste verwendet. 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. Wenn **** GetProps fehlschlägt: 
    
   1. Rufen Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode des PAB auf, um die **PR_CREATE_TEMPLATES** ([pidtagcreatetemplates (](pidtagcreatetemplates-canonical-property.md))-Eigenschaft mit der **IMAPITable** -Schnittstelle zu öffnen. 
      
   2. Erstellen Sie eine Eigenschaftseinschränkung, um nach der Zeile mit der **PR_ADDRTYPE** ([pidtagaddresstype (](pidtagaddresstype-canonical-property.md))-Spalte gleich "MAPIPDL" zu suchen. 
      
   3. Rufen Sie [IMAPITable:: FindRow](imapitable-findrow.md) auf, um diese Zeile zu suchen. 
    
6. Speichern Sie die Eintrags-ID **** , die von GetProps oder **FindRow**zurückgegeben wird.
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. Rufen Sie die [IABContainer:: CreateEntry](iabcontainer-createentry.md) -Methode des PAB auf, um einen neuen Eintrag mithilfe der Vorlage zu erstellen, die durch die gespeicherte Eintrags-ID dargestellt wird. Gehen Sie nicht davon aus, dass das zurückgegebene Objekt eine Verteilerliste anstelle eines Messaging Benutzers ist, wenn dieser Aufruf Remote ausgeführt wird. Beachten Sie, dass das CREATE_CHECK_DUP-Flag im _ulFlags_ -Parameter übergeben wird, um zu verhindern, dass der Eintrag zweimal hinzugefügt wird. 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. Rufen Sie die **IUnknown:: QueryInterface** -Methode des neuen Eintrags auf, übergeben Sie IID_IDistList als Schnittstellenbezeichner, um zu ermitteln, ob es sich bei dem Eintrag um eine Verteilerliste handelt, und unterstützt die [IDistList: IMAPIContainer](idistlistimapicontainer.md) -Schnittstelle. Da **CreateEntry** einen **IMAPIProp** -Zeiger anstelle des spezifischeren **IMailUser** -oder **IDistList** -Zeigers zurückgibt, überprüfen Sie, ob ein Verteilerlistenobjekt erstellt wurde. Wenn **QueryInterface** erfolgreich ist, können Sie sicher sein, dass Sie eine Verteilerliste anstelle eines Messaging Benutzers erstellt haben. 
    
9. Rufen Sie die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode der Verteilerliste auf, um den Anzeigenamen und andere Eigenschaften festzulegen. 
    
10. Rufen Sie die [IABContainer:: CreateEntry](iabcontainer-createentry.md) -Methode der Verteilerliste auf, um einen oder mehrere Messagingbenutzer hinzuzufügen. 
    
11. Rufen Sie die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode der Verteilerliste auf, wenn Sie Sie speichern möchten. Um den Eintragsbezeichner der gespeicherten Verteilerliste abzurufen, legen Sie das KEEP_OPEN_READWRITE-Flag fest, und rufen Sie dann [IMAPIProp::](imapiprop-getprops.md) GetProps auf, das die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft anfordert.
    
12. Veröffentlichen Sie die neue Verteilerliste und das PAB, indem Sie Ihre **IUnknown:: Release** -Methoden aufrufen. 
    
13. Rufen Sie [mapifreebufferfreigegeben](mapifreebuffer.md) auf, um den Speicher für die Eintrags-ID des PAB und das Array der sized-Eigenschaftstags freizugeben. 
    

