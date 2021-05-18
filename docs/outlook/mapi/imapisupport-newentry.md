---
title: IMAPISupportNewEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.NewEntry
api_type:
- COM
ms.assetid: 588d002b-8412-4ab9-9757-04ad89e0a6f8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3468e4a92787e440f230d60ab31f37526fe7d5e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405457"
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
  
> [in] Ein Handle zum übergeordneten Fenster des Dialogfelds.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _cbEIDContainer_
  
> [in] Die Byteanzahl in der Eintrags-ID, auf die der  _lpEIDContainer-Parameter_ verweist. 
    
 _lpEIDContainer_
  
> [in] Ein Zeiger auf die Eintrags-ID des Containers, um den neuen Eintrag zu erhalten. Wenn  _cbEIDContainer_ den Wert 0 und  _lpEIDContainer_ NULL hat, erstellt **NewEntry** einen einmal verwendeten Eintragsbezeichner, der demselben Typ wie bei einem Aufruf der [IMAPISupport::CreateOneOff-Methode](imapisupport-createoneoff.md) folgt. 
    
 _cbEIDNewEntryTpl_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEIDNewEntryTpl-Parameter_ verweist. 
    
 _lpEIDNewEntryTpl_
  
> [in] Ein Zeiger auf die Eintrags-ID der Vorlage, die zum Erstellen des neuen Eintrags verwendet werden soll. Wenn  _cbEIDNewEntryTpl_ 0 und  _lpEIDNewEntryTpl_ NULL ist, wird **in NewEntry** ein Dialogfeld angezeigt, in dem der Benutzer aus einer Liste von Vorlagen zum Hinzufügen neuer Einträge auswählen kann. 
    
 _lpcbEIDNewEntry_
  
> [out] Ein Zeiger auf die Byteanzahl im Eintragsbezeichner, auf den der  _lppEIDNewEntry-Parameter_ verweist. 
    
 _lppEIDNewEntry_
  
> [out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID des neu erstellten Eintrags.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der neue Eintrag wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::NewEntry-Methode** wird für Unterstützungsobjekte des Adressbuchanbieters implementiert. Adressbuchanbieter rufen **NewEntry auf,** um einen neuen Adressbucheintrag zu erstellen, der direkt einem Container hinzugefügt oder zur Adressung einer ausgehenden Nachricht verwendet werden soll. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn der neue Eintrag einem bestimmten Container hinzugefügt werden soll, legen Sie  _lpEIDContainer_ auf den Eintragsbezeichner des Containers und  _cbEIDContainer_ auf die Byteanzahl in der Eintrags-ID. 
  
Wenn der neue Eintrag der Empfängerliste einer ausgehenden Nachricht hinzugefügt werden soll, legen Sie  _lpEIDContainer_ auf NULL und  _cbEIDContainer_ auf 0. 
  
Wenn Sie dem Benutzer einer Clientanwendung die Auswahl des zu erstellenden Eintragstyps ermöglichen möchten, übergeben Sie 0 in  _cbEIDNewEntryTpl_ und NULL in  _lpEIDNewEntryTpl_. **NewEntry** zeigt die einmal aufgeführte MAPI-Tabelle an, eine Liste der Vorlagen, die MAPI und die einzelnen Adressbuchanbieter in der Sitzung unterstützen. Jede Vorlage kann einen Empfängereintrag für einen oder mehrere Adresstypen erstellen. 
  
Wenn Sie den Eintragsbezeichner des neuen Eintrags beibehalten möchten, übergeben Sie gültige Zeiger in den _Parametern lpcbEIDNewEntry_ und _lppEIDNewEntry._ Sie sind dafür verantwortlich, diese Eintrags-ID frei zu machen, wenn Sie damit fertig sind, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen. 
  
Um eine bestimmte Vorlage zum Hinzufügen eines neuen Eintrags zu einem veränderbaren Container zu verwenden, verwenden Sie das folgende Verfahren:
  
1. Rufen Sie [die IMAPISupport::OpenEntry-Methode](imapisupport-openentry.md) auf, um den Zielcontainer zu öffnen, und legen Sie den  _lpEntryID-Parameter_ auf den Eintragsbezeichner des Containers. 
    
2. Rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des Zielcontainers auf, und legen Sie den  _ulPropTag-Parameter_ auf **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) und den  _lpiid-Parameter_ auf IID_IMAPITable. Der Container gibt eine einmal aufgeführte Tabelle zurück, in der alle Vorlagen aufgeführt sind, die er zum Erstellen neuer Einträge unterstützt. 
    
3. Rufen Sie die Zeile ab, die die Vorlage für den bestimmten Eintragstyp darstellt, den Sie erstellen möchten. Die **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) gibt den Adresstyp an, der von der Vorlage unterstützt wird. 
    
4. Rufen **Sie IMAPISupport::NewEntry** auf, und legen Sie den  _lpEIDNewEntryTpl-Parameter_ auf den Eintragsbezeichner der ausgewählten Vorlage. Der Eintragsbezeichner ist **die PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Spalte aus der Zeile der Vorlage in der Einmaltabelle. Übergeben Sie 0 in  _cbEIDContainer_ und NULL in  _lpEIDContainer_. Übergeben Sie einen gültigen Zeiger im  _lppEIDNewEntry-Parameter,_ wenn Sie den Eintragsbezeichner des neuen Eintrags beibehalten möchten. 
    
## <a name="see-also"></a>Siehe auch



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport::OpenEntry](imapisupport-openentry.md)
  
[PidTagCreateTemplates (kanonische Eigenschaft)](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

