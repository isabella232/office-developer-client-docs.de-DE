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
  
Clients können eine Verteilerliste direkt in einem veränderbaren Container wie dem persönlichen Adressbuch (PAB) erstellen.
  
**So erstellen Sie eine Verteilerliste im PAB**
  
1. Erstellen Sie ein #A0 mit einem Eigenschaftstag, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), wie folgt:
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. Rufen [Sie IAddrBook::GetPAB auf,](iaddrbook-getpab.md) um die Eintrags-ID des PAB abzurufen. Wenn ein Fehler auftritt oder **GetPAB** Null oder NULL zurückgibt, fahren Sie nicht fort. 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. Rufen [Sie IAddrBook::OpenEntry auf,](iaddrbook-openentry.md) um das PAB zu öffnen. Der  _ulObjType-Ausgabeparameter_ sollte auf MAPI_ABCONT. 
    
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

5. Wenn **GetProps fehlschlägt:** 
    
   1. Rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des PAB auf, um die **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) -Eigenschaft mit der **IMAPITable-Schnittstelle zu** öffnen. 
      
   2. Erstellen Sie eine Eigenschaftseinschränkung, um nach der Zeile mit der Spalte **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) zu suchen, die "MAPIPDL" entspricht. 
      
   3. Rufen [Sie IMAPITable::FindRow auf,](imapitable-findrow.md) um diese Zeile zu finden. 
    
6. Speichern Sie die von **GetProps** oder FindRow zurückgegebene **Eintrags-ID.**
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. Rufen Sie die [IABContainer::CreateEntry-Methode](iabcontainer-createentry.md) des PAB auf, um einen neuen Eintrag mithilfe der Vorlage zu erstellen, die durch die gespeicherte Eintrags-ID dargestellt wird. Gehen Sie nicht davon aus, dass es sich bei dem zurückgegebenen Objekt um eine Verteilerliste und nicht um einen Messagingbenutzer handelt, wenn dieser Aufruf remote ist. Beachten Sie, dass CREATE_CHECK_DUP im  _ulFlags-Parameter_ übergeben wird, um zu verhindern, dass der Eintrag zweimal hinzugefügt wird. 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. Rufen Sie die **IUnknown::QueryInterface-Methode** des neuen Eintrags auf, übergeben Sie IID_IDistList als Schnittstellenbezeichner, um zu ermitteln, ob es sich bei dem Eintrag um eine Verteilerliste handelt und unterstützt die [IDistList : IMAPIContainer-Schnittstelle.](idistlistimapicontainer.md) Da **CreateEntry** einen **IMAPIProp-Zeiger** anstelle des spezifischeren **IMailUser-** oder **IDistList-Zeigers** zurückgibt, überprüfen Sie, ob ein Verteilerlistenobjekt erstellt wurde. Wenn **QueryInterface** erfolgreich ist, können Sie sicher sein, dass Sie eine Verteilerliste anstelle eines Messagingbenutzers erstellt haben. 
    
9. Rufen Sie die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) der Verteilerliste auf, um den Anzeigenamen und andere Eigenschaften festlegen. 
    
10. Rufen Sie die [IABContainer::CreateEntry-Methode](iabcontainer-createentry.md) der Verteilerliste auf, um einen oder mehrere Messagingbenutzer hinzuzufügen. 
    
11. Rufen Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der Verteilerliste auf, wenn Sie zum Speichern bereit sind. Legen Sie zum Abrufen der Eintrags-ID der gespeicherten Verteilerliste das Flag KEEP_OPEN_READWRITE und rufen Sie [dann IMAPIProp::GetProps](imapiprop-getprops.md) auf, der die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft anfordert.
    
12. Geben Sie die neue Verteilerliste und das PAB frei, indem Sie ihre **IUnknown::Release-Methoden** aufrufen. 
    
13. Rufen [Sie MAPIFreeBuffer auf,](mapifreebuffer.md) um den Arbeitsspeicher für die Eintrags-ID des PAB und das Array des Eigenschaftstags der Größe frei zu geben. 
    

