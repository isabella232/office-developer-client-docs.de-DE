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
# <a name="iaddrbooknewentry"></a>IAddrBook::NewEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt einem Adressbuchcontainer oder der Empfängerliste einer ausgehenden Nachricht einen neuen Empfänger hinzu.
  
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
  
> [in] Ein Handle zum übergeordneten Fenster für das Dialogfeld.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Texttyp steuert, der verwendet wird. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.
    
 _cbEIDContainer_
  
> [in] Die Byteanzahl in der Eintrags-ID, auf die der  _lpEIDContainer-Parameter_ verweist. 
    
 _lpEIDContainer_
  
> [in] Ein Zeiger auf die Eintrags-ID des Containers, in dem der neue Empfänger hinzugefügt werden soll. Wenn der  _cbEIDContainer-Parameter_ null ist, gibt die **NewEntry-Methode** einen Empfängereintragsbezeichner und eine Liste von Vorlagen zurück, als ob die [IAddrBook::CreateOneOff-Methode](iaddrbook-createoneoff.md) aufgerufen wurde. 
    
 _cbEIDNewEntryTpl_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEIDNewEntryTpl-Parameter_ verweist. 
    
 _lpEIDNewEntryTpl_
  
> [in] Ein Zeiger auf eine einmal verwendete Vorlage, die zum Erstellen des neuen Empfängers verwendet wird. Wenn  _cbEIDNewEntryTpl_ null und  _lpEIDNewEntryTpl_ NULL ist, zeigt **NewEntry** ein Dialogfeld an, mit dem der Benutzer aus einer Liste von Vorlagen zum Hinzufügen neuer Einträge auswählen kann. 
    
 _lpcbEIDNewEntry_
  
> [out] Ein Zeiger auf die Byteanzahl im Eintragsbezeichner, auf den der  _lppEIDNewEntry-Parameter_ verweist. 
    
 _lppEIDNewEntry_
  
> [out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID des neuen Empfängers.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der neue Adressbucheintrag wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Hinweise

Die **NewEntry-Methode** erstellt einen neuen Adressbucheintrag, der direkt zu einem Container hinzugefügt oder für die Adresseingabe einer ausgehenden Nachricht verwendet werden soll. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn der neue Eintrag einem bestimmten Container hinzugefügt werden soll, legen Sie  _lpEIDContainer_ auf den Eintragsbezeichner des Containers und  _cbEIDContainer_ auf die Byteanzahl in der Eintrags-ID. 
  
Wenn der neue Eintrag der Empfängerliste einer ausgehenden Nachricht hinzugefügt werden soll, legen Sie  _lpEIDContainer_ auf NULL und  _cbEIDContainer_ auf Null. 
  
Wenn Sie dem Benutzer einer Clientanwendung die Auswahl des zu erstellenden Eintragstyps ermöglichen möchten, übergeben Sie null in  _cbEIDNewEntryTpl_ und NULL in  _lpEIDNewEntryTpl_. Die **NewEntry-Methode** zeigt die one-off-Tabelle MAPI an, eine Liste von Vorlagen, die von MAPI und von jedem Adressbuchanbieter in der Sitzung unterstützt werden. Jede Vorlage kann einen Empfängereintrag für einen oder mehrere Adresstypen erstellen. 
  
Wenn Sie den Eintragsbezeichner des neuen Eintrags beibehalten möchten, übergeben Sie gültige Zeiger in den _Parametern lpcbEIDNewEntry_ und _lppEIDNewEntry._ Sie sind dafür verantwortlich, diese Eintrags-ID frei zu machen, wenn Sie damit fertig sind, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen. 
  
Um eine bestimmte Vorlage zum Hinzufügen eines neuen Eintrags zu einem veränderbaren Container zu verwenden, verwenden Sie das folgende Verfahren:
  
1. Rufen Sie [die IMAPISession::OpenEntry-Methode](imapisession-openentry.md) auf, um den Zielcontainer zu öffnen, und legen Sie den  _lpEntryID-Parameter_ auf den Eintragsbezeichner des Containers fest. 
    
2. Rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des Zielcontainers auf, und legen Sie den  _ulPropTag-Parameter_ auf **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) und den  _lpiid-Parameter_ auf IID_IMAPITable. Der Container gibt eine einmal aufgeführte Tabelle zurück, in der alle Vorlagen aufgeführt sind, die er zum Erstellen neuer Einträge unterstützt. 
    
3. Rufen Sie die Zeile ab, die die Vorlage für den bestimmten Eintragstyp darstellt, den Sie erstellen möchten. Die **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) gibt den Adresstyp an, der von der Vorlage unterstützt wird.
    
4. Rufen Sie **die NewEntry-Methode** auf, und legen Sie  _lpEIDNewEntryTpl_ auf den Eintragsbezeichner der ausgewählten Vorlage. Der Eintragsbezeichner ist die **spalte PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) aus der Zeile der Vorlage in der Einmaltabelle. Übergeben Sie null in  _cbEIDContainer_ und NULL in  _lpEIDContainer_. Übergeben Sie einen gültigen Zeiger im  _lppEIDNewEntry-Parameter,_ wenn Sie den Eintragsbezeichner des neuen Eintrags beibehalten möchten. 
    
## <a name="see-also"></a>Siehe auch



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[PidTagCreateTemplates (kanonische Eigenschaft)](pidtagcreatetemplates-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

