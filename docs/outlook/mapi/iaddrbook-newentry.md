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
  
> in Ein Handle für das übergeordnete Fenster für das Dialogfeld.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Typ des verwendeten Texts steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.
    
 _cbEIDContainer_
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEIDContainer_ -Parameter verwiesen wird. 
    
 _lpEIDContainer_
  
> in Ein Zeiger auf die Eintrags-ID des Containers, in dem der neue Empfänger hinzugefügt werden soll. Wenn der _cbEIDContainer_ -Parameter 0 (NULL **** ) ist, gibt die neuentry-Methode eine Empfänger Eintrags-ID und eine Liste von Vorlagen zurück, als ob die [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) -Methode aufgerufen wurde. 
    
 _cbEIDNewEntryTpl_
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEIDNewEntryTpl_ -Parameter verwiesen wird. 
    
 _lpEIDNewEntryTpl_
  
> in Ein Zeiger auf eine einmalige Vorlage, die zum Erstellen des neuen Empfängers verwendet wird. Wenn _cbEIDNewEntryTpl_ ist und _lpEIDNewEntryTpl_ NULL ist, zeigt der neue **Eintrag** ein Dialogfeld an, in dem der Benutzer aus einer Liste von Vorlagen zum Hinzufügen neuer Einträge auswählen kann. 
    
 _lpcbEIDNewEntry_
  
> Out Ein Zeiger auf die Bytezahl in der Eintrags-ID, auf die durch den _lppEIDNewEntry_ -Parameter verwiesen wird. 
    
 _lppEIDNewEntry_
  
> Out Ein Zeiger auf einen Zeiger auf die Eintrags-ID des neuen Empfängers.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der neue Adressbucheintrag wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Bemerkungen

Mit **** der neuentry-Methode wird ein neuer Adressbucheintrag erstellt, der direkt zu einem Container hinzugefügt oder zur Behebung einer ausgehenden Nachricht verwendet werden kann. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn der neue Eintrag einem bestimmten Container hinzugefügt werden soll, legen Sie _lpEIDContainer_ auf die Eintrags-ID des Containers und _cbEIDContainer_ auf die Bytezahl in der Eintrags-ID fest. 
  
Wenn der neue Eintrag der Empfängerliste einer ausgehenden Nachricht hinzugefügt werden soll, legen Sie _lpEIDContainer_ auf NULL und _cbEIDContainer_ auf 0 (null) fest. 
  
Wenn Sie dem Benutzer einer Clientanwendung erlauben möchten, den Typ des zu erstellenden Eintrags auszuwählen, überschreiten Sie NULL in _cbEIDNewEntryTpl_ und NULL in _lpEIDNewEntryTpl_. Die **** Posteingangs Methode zeigt die MAPI-einmalige Tabelle, eine Liste der von MAPI unterstützten Vorlagen und jedes Adressbuch Anbieters in der Sitzung an. Jede Vorlage kann einen Empfängereintrag für einen oder mehrere Adresstypen erstellen. 
  
Wenn Sie die Eintrags-ID des neuen Eintrags behalten möchten, übergeben Sie gültige Zeiger in den Parametern _lpcbEIDNewEntry_ und _lppEIDNewEntry_ . Sie sind für die Freigabe dieser Eintrags-ID verantwortlich, wenn Sie damit fertig sind, indem Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufrufen. 
  
Gehen Sie folgendermaßen vor, um eine bestimmte Vorlage zum Hinzufügen eines neuen Eintrags zu einem änderbaren Container zu verwenden:
  
1. Rufen Sie die [IMAPISession:: OpenEntry](imapisession-openentry.md) -Methode auf, um den Zielcontainer zu öffnen, und legen Sie den Parameter _lpEntryID_ auf den Eintragsbezeichner des Containers fest. 
    
2. Rufen Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode des Zielcontainers auf, und legen Sie den Parameter _ulPropTag_ auf **PR_CREATE_TEMPLATES** ([pidtagcreatetemplates (](pidtagcreatetemplates-canonical-property.md)) und den _lpIID_ -Parameter auf IID_IMAPITable fest. Der Container gibt eine einmalige Tabelle zurück, in der alle Vorlagen aufgeführt sind, die für das Erstellen neuer Einträge unterstützt werden. 
    
3. Rufen Sie die Zeile ab, die die Vorlage für den jeweiligen Eintragstyp darstellt, den Sie erstellen möchten. Die **PR_ADDRTYPE** ([pidtagaddresstype (](pidtagaddresstype-canonical-property.md)) gibt den von der Vorlage unterstützten Adresstyp an.
    
4. Rufen Sie **** die neuentry-Methode auf, und legen Sie _lpEIDNewEntryTpl_ auf die Eintrags-ID der ausgewählten Vorlage fest. Die Eintrags-ID ist die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Spalte aus der Zeile der Vorlage in der einmaligen Tabelle. NULL in _cbEIDContainer_ und NULL in _lpEIDContainer_. Übergeben Sie einen gültigen Zeiger im _lppEIDNewEntry_ -Parameter, wenn Sie die Eintrags-ID des neuen Eintrags aufbewahren möchten. 
    
## <a name="see-also"></a>Siehe auch



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[Kanonische Pidtagcreatetemplates (-Eigenschaft](pidtagcreatetemplates-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

