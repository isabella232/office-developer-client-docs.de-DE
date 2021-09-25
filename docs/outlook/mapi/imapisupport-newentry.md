---
title: IMAPISupportNewEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.NewEntry
api_type:
- COM
ms.assetid: 588d002b-8412-4ab9-9757-04ad89e0a6f8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4b38b703437c196c0842e802897aaf02d9f87f39
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630663"
---
# <a name="imapisupportnewentry"></a>IMAPISupport::NewEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt einen neuen Empfänger direkt zu einem Adressbuchcontainer oder zur Empfängerliste einer ausgehenden Nachricht hinzu.
  
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
  
> [in] Ein Handle für das übergeordnete Fenster des Dialogfelds.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _cbEIDContainer_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _parameter lpEIDContainer_ verweist. 
    
 _lpEIDContainer_
  
> [in] Ein Zeiger auf den Eintragsbezeichner des Containers, der den neuen Eintrag empfangen soll. Wenn  _cbEIDContainer_ 0 ist und  _lpEIDContainer_ NULL ist, erstellt **NewEntry** einen einmaligen Eintragsbezeichner, der denselben Typ aufweist, der durch einen Aufruf der [IMAPISupport::CreateOneOff-Methode](imapisupport-createoneoff.md) generiert wird. 
    
 _cbEIDNewEntryTpl_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _parameter lpEIDNewEntryTpl_ verweist. 
    
 _lpEIDNewEntryTpl_
  
> [in] Ein Zeiger auf den Eintragsbezeichner der Vorlage, die zum Erstellen des neuen Eintrags verwendet werden soll. Wenn  _cbEIDNewEntryTpl_ 0 und  _lpEIDNewEntryTpl_ NULL ist, zeigt **NewEntry** ein Dialogfeld an, in dem der Benutzer aus einer Liste von Vorlagen zum Hinzufügen neuer Einträge auswählen kann. 
    
 _lpcbEIDNewEntry_
  
> [out] Ein Zeiger auf die Byteanzahl im Eintragsbezeichner, auf den der  _Parameter "lppEIDNewEntry"_ verweist. 
    
 _lppEIDNewEntry_
  
> [out] Ein Zeiger auf einen Zeiger auf den Eintragsbezeichner des neu erstellten Eintrags.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der neue Eintrag wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::NewEntry-Methode** ist für Supportobjekte des Adressbuchanbieters implementiert. Adressbuchanbieter rufen **NewEntry** auf, um einen neuen Adressbucheintrag zu erstellen, der direkt zu einem Container hinzugefügt oder zum Adressieren einer ausgehenden Nachricht verwendet werden soll. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn der neue Eintrag einem bestimmten Container hinzugefügt werden soll, legen Sie  _lpEIDContainer_ auf den Eintragsbezeichner des Containers und  _cbEIDContainer_ auf die Byteanzahl im Eintragsbezeichner fest. 
  
Wenn der neue Eintrag der Empfängerliste einer ausgehenden Nachricht hinzugefügt werden soll, legen Sie  _lpEIDContainer_ auf NULL und  _cbEIDContainer_ auf 0 fest. 
  
Wenn Sie zulassen möchten, dass der Benutzer einer Clientanwendung den zu erstellenden Eintragstyp auswählt, übergeben Sie 0 in _cbEIDNewEntryTpl_ und NULL in _lpEIDNewEntryTpl._ **NewEntry** zeigt die einmalige MAPI-Tabelle an, eine Liste der Vorlagen, die von der MAPI und jedem Adressbuchanbieter in der Sitzung unterstützt werden. Jede Vorlage kann einen Empfängereintrag für einen oder mehrere Adresstypen erstellen. 
  
Wenn Sie den Eintragsbezeichner des neuen Eintrags beibehalten möchten, übergeben Sie gültige Zeiger in den _Parametern lpcbEIDNewEntry_ und _lppEIDNewEntry._ Sie sind dafür verantwortlich, diesen Eintragsbezeichner frei zu geben, wenn Sie damit fertig sind, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen. 
  
Gehen Sie folgendermaßen vor, um eine bestimmte Vorlage zum Hinzufügen eines neuen Eintrags zu einem modifizierbaren Container zu verwenden:
  
1. Rufen Sie die [IMAPISupport::OpenEntry-Methode](imapisupport-openentry.md) auf, um den Zielcontainer zu öffnen, und legen Sie den  _Parameter lpEntryID_ auf den Eintragsbezeichner des Containers fest. 
    
2. Rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des Zielcontainers auf, und legen Sie den  _ulPropTag-Parameter_ auf **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) und den  _lpiid-Parameter_ auf IID_IMAPITable fest. Der Container gibt eine einmalige Tabelle zurück, in der alle Vorlagen aufgeführt sind, die zum Erstellen neuer Einträge unterstützt werden. 
    
3. Dient zum Abrufen der Zeile, die die Vorlage für den bestimmten Eintragstyp darstellt, den Sie erstellen möchten. Die **Spalte PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) gibt den Adresstyp an, der von der Vorlage unterstützt wird. 
    
4. Rufen Sie **IMAPISupport::NewEntry** auf, und legen Sie den Parameter  _lpEIDNewEntryTpl_ auf den Eintragsbezeichner der ausgewählten Vorlage fest. Der Eintragsbezeichner ist die **spalte PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) aus der Zeile der Vorlage in der Einmaligen Tabelle. Übergeben Sie "0" in _"cbEIDContainer"_ und "NULL" in _"lpEIDContainer"._ Übergeben Sie einen gültigen Zeiger im  _lppEIDNewEntry-Parameter,_ wenn Sie den Eintragsbezeichner des neuen Eintrags beibehalten möchten. 
    
## <a name="see-also"></a>Siehe auch



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport::OpenEntry](imapisupport-openentry.md)
  
[PidTagCreateTemplates (kanonische Eigenschaft)](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

