---
title: IAddrBookNewEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.NewEntry
api_type:
- COM
ms.assetid: 8d2d786b-e621-456d-b087-3373df6f8ac5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bbf86646322497c7d475589a5fac0e86572c4486
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613975"
---
# <a name="iaddrbooknewentry"></a>IAddrBook::NewEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt einen neuen Empfänger zu einem Adressbuchcontainer oder zur Empfängerliste einer ausgehenden Nachricht hinzu.
  
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

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster für das Dialogfeld.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ des verwendeten Texts steuert. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
 _cbEIDContainer_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _parameter lpEIDContainer_ verweist. 
    
 _lpEIDContainer_
  
> [in] Ein Zeiger auf den Eintragsbezeichner des Containers, dem der neue Empfänger hinzugefügt werden soll. Wenn der  _cbEIDContainer-Parameter_ Null ist, gibt die **NewEntry-Methode** einen Empfängereintragsbezeichner und eine Liste von Vorlagen zurück, als ob die [IAddrBook::CreateOneOff-Methode](iaddrbook-createoneoff.md) aufgerufen würde. 
    
 _cbEIDNewEntryTpl_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _parameter lpEIDNewEntryTpl_ verweist. 
    
 _lpEIDNewEntryTpl_
  
> [in] Ein Zeiger auf eine einmalige Vorlage, die zum Erstellen des neuen Empfängers verwendet wird. Wenn  _cbEIDNewEntryTpl_ null und  _lpEIDNewEntryTpl_ NULL ist, zeigt **NewEntry** ein Dialogfeld an, in dem der Benutzer aus einer Liste von Vorlagen zum Hinzufügen neuer Einträge auswählen kann. 
    
 _lpcbEIDNewEntry_
  
> [out] Ein Zeiger auf die Byteanzahl im Eintragsbezeichner, auf den der  _Parameter "lppEIDNewEntry"_ verweist. 
    
 _lppEIDNewEntry_
  
> [out] Ein Zeiger auf einen Zeiger auf den Eintragsbezeichner des neuen Empfängers.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der neue Adressbucheintrag wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Bemerkungen

Die **NewEntry-Methode** erstellt einen neuen Adressbucheintrag, der direkt zu einem Container hinzugefügt oder zum Adressieren einer ausgehenden Nachricht verwendet werden soll. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn der neue Eintrag einem bestimmten Container hinzugefügt werden soll, legen Sie  _lpEIDContainer_ auf den Eintragsbezeichner des Containers und  _cbEIDContainer_ auf die Byteanzahl im Eintragsbezeichner fest. 
  
Wenn der neue Eintrag der Empfängerliste einer ausgehenden Nachricht hinzugefügt werden soll, legen Sie  _lpEIDContainer_ auf NULL und  _cbEIDContainer_ auf Null fest. 
  
Wenn Sie zulassen möchten, dass der Benutzer einer Clientanwendung den zu erstellenden Eintragstyp auswählt, übergeben Sie null in _cbEIDNewEntryTpl_ und NULL in _lpEIDNewEntryTpl._ Die **NewEntry-Methode** zeigt die einmalige MAPI-Tabelle an, eine Liste der Vorlagen, die von der MAPI und von jedem Adressbuchanbieter in der Sitzung unterstützt werden. Jede Vorlage kann einen Empfängereintrag für einen oder mehrere Adresstypen erstellen. 
  
Wenn Sie den Eintragsbezeichner des neuen Eintrags beibehalten möchten, übergeben Sie gültige Zeiger in den _Parametern lpcbEIDNewEntry_ und _lppEIDNewEntry._ Sie sind dafür verantwortlich, diesen Eintragsbezeichner frei zu geben, wenn Sie damit fertig sind, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen. 
  
Gehen Sie folgendermaßen vor, um eine bestimmte Vorlage zum Hinzufügen eines neuen Eintrags zu einem modifizierbaren Container zu verwenden:
  
1. Rufen Sie die [IMAPISession::OpenEntry-Methode](imapisession-openentry.md) auf, um den Zielcontainer zu öffnen, und legen Sie den  _Parameter lpEntryID_ auf den Eintragsbezeichner des Containers fest. 
    
2. Rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des Zielcontainers auf, und legen Sie den  _ulPropTag-Parameter_ auf **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) und den  _lpiid-Parameter_ auf IID_IMAPITable fest. Der Container gibt eine einmalige Tabelle zurück, in der alle Vorlagen aufgeführt sind, die zum Erstellen neuer Einträge unterstützt werden. 
    
3. Dient zum Abrufen der Zeile, die die Vorlage für den bestimmten Eintragstyp darstellt, den Sie erstellen möchten. Die **Spalte PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) gibt den Adresstyp an, der von der Vorlage unterstützt wird.
    
4. Rufen Sie die **NewEntry-Methode** auf, und legen Sie  _lpEIDNewEntryTpl_ auf den Eintragsbezeichner der ausgewählten Vorlage fest. Der Eintragsbezeichner ist die **spalte PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) aus der Zeile der Vorlage in der einmaligen Tabelle. Übergeben Sie Null in  _cbEIDContainer_ und NULL in  _lpEIDContainer_. Übergeben Sie einen gültigen Zeiger im  _lppEIDNewEntry-Parameter,_ wenn Sie den Eintragsbezeichner des neuen Eintrags beibehalten möchten. 
    
## <a name="see-also"></a>Siehe auch



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[PidTagCreateTemplates (kanonische Eigenschaft)](pidtagcreatetemplates-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

