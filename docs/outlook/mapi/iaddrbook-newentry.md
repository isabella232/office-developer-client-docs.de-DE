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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e9b9ae316749659c6fc6a043bfb72c49010ccc9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792020"
---
# <a name="iaddrbooknewentry"></a>IAddrBook::NewEntry

  
  
**Betrifft**: Outlook 
  
Fügt einen neuen Empfänger um eine Adressbuchcontainer oder die Empfängerliste von ausgehenden Nachrichten.
  
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
  
> [in] Eine Bitmaske aus Flags, die den Typ des Texts gesteuert, die verwendet wird. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
 _cbEIDContainer_
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEIDContainer_ verwiesen. 
    
 _lpEIDContainer_
  
> [in] Ein Zeiger auf die Eintrags-ID des Containers, in der neue Empfänger wird hinzugefügt werden soll. Wenn der Parameter _CbEIDContainer_ gleich NULL ist, gibt die **NewEntry** -Methode ein Empfänger Eintrags-ID und eine Liste der Vorlagen, als ob die [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) -Methode aufgerufen wurde. 
    
 _cbEIDNewEntryTpl_
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEIDNewEntryTpl_ verwiesen. 
    
 _lpEIDNewEntryTpl_
  
> [in] Ein Zeiger auf eine einmalige Vorlage, die zum Erstellen des neuen Empfängers verwendet wird. Wenn _CbEIDNewEntryTpl_ 0 (null ist) und _LpEIDNewEntryTpl_ NULL ist, zeigt **NewEntry** ein Dialogfeld, mit denen der Benutzer aus einer Liste von Vorlagen für neue Einträge auswählen kann. 
    
 _lpcbEIDNewEntry_
  
> [out] Ein Zeiger auf die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LppEIDNewEntry_ verwiesen. 
    
 _lppEIDNewEntry_
  
> [out] Ein Zeiger auf einen Zeiger auf den neuen Empfänger Eintrags-ID.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der neuen Adresseintrag Adressbuch wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Hinweise

Die **NewEntry** -Methode erstellt einen neuen Address Book Eintrag direkt in einem Container hinzugefügt werden soll oder verwendet werden, um eine ausgehende Nachricht zu adressieren. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie den neuen Eintrag auf einen bestimmten Container hinzugefügt werden soll, legen Sie _LpEIDContainer_ Eintrags-ID und _CbEIDContainer_ , um die Byteanzahl von in die Eintrags-ID des Containers. 
  
Wenn Sie den neuen Eintrag der Empfängerliste von ausgehenden Nachrichten hinzugefügt werden soll, legen Sie _LpEIDContainer_ auf NULL und _CbEIDContainer_ auf NULL festgelegt. 
  
Wenn den Benutzer von einer Clientanwendung aus, wählen Sie den Typ der Eintrag erstellt werden soll, übergeben Sie NULL in _CbEIDNewEntryTpl_ und NULL in _LpEIDNewEntryTpl_. Die **NewEntry** -Methode der MAPI-einmalige Tabelle, eine Liste der Vorlagen unterstützt durch MAPI und durch jede Adressbuchanbieter in der Sitzung angezeigt. Jede Vorlage kann ein Empfänger Eintrag für einen oder mehrere Adresstypen erstellt. 
  
Wenn Sie die Eintrags-ID des neuen Eintrags beibehalten möchten, übergeben Sie die Parameter _LpcbEIDNewEntry_ und _LppEIDNewEntry_ gültige Zeiger. Sie sind verantwortlich für das Freigeben von dieses Eintrags-ID, wenn Sie mit ihm fertig sind, durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion. 
  
Um eine bestimmte Vorlage verwenden, um einen neuen Eintrag einem änderbare Container hinzuzufügen, verwenden Sie die folgende Schritte aus:
  
1. Rufen Sie die [IMAPISession::OpenEntry](imapisession-openentry.md) -Methode zum Öffnen den Zielcontainer, und legen Sie den Parameter _LpEntryID_ auf die Eintrags-ID des Containers. 
    
2. Rufen Sie das Ziel des Containers [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode, und legen Sie den Parameter _UlPropTag_ **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) und der Parameter _Lpiid_ auf IID_IMAPITable. Der Container gibt eine einmalige Tabelle zurück, die alle Vorlagen aufgeführt werden, die sie zum Erstellen neuer Einträge unterstützt. 
    
3. Rufen Sie die Zeile, die die Vorlage für den angegebenen Typ des Eintrags darstellt, den Sie erstellen möchten. Die **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))-Spalte gibt den Typ der Adresse, der von der Vorlage unterstützt wird.
    
4. Rufen Sie die **NewEntry** -Methode, und legen Sie _LpEIDNewEntryTpl_ die Eintrags-ID der ausgewählten Vorlage. Die Eintrags-ID wird die Spalte **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) aus der Vorlage Zeile in der Tabelle "einmal" sein. Übergeben Sie NULL in _CbEIDContainer_ und NULL in _LpEIDContainer_. Übergeben Sie einen gültigen Zeiger im _LppEIDNewEntry_ -Parameter, wenn Sie den neuen Eintrag Eintrags-ID beibehalten möchten. 
    
## <a name="see-also"></a>Siehe auch



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[Kanonische PidTagCreateTemplates-Eigenschaft](pidtagcreatetemplates-canonical-property.md)
  
[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)

