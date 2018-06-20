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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ae2a19d556fc9819312ce822f9347edcd6edc0d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792384"
---
# <a name="imapisupportnewentry"></a>IMAPISupport::NewEntry

  
  
**Betrifft**: Outlook 
  
Fügt einen neuen Empfänger direkt an einen Adressbuchcontainer oder die Empfängerliste von ausgehenden Nachrichten.
  
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
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEIDContainer_ verwiesen. 
    
 _lpEIDContainer_
  
> [in] Ein Zeiger auf die Eintrags-ID des Containers, um den neuen Eintrag zu erhalten. Wenn _CbEIDContainer_ 0 und _LpEIDContainer_ NULL ist, erstellt **NewEntry** einen Eingangs-Bezeichner, der den gleichen Typ ist, wie durch einen Aufruf an die [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) -Methode generiert wird. 
    
 _cbEIDNewEntryTpl_
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEIDNewEntryTpl_ verwiesen. 
    
 _lpEIDNewEntryTpl_
  
> [in] Ein Zeiger auf die Eintrags-ID der Vorlage, die verwendet werden, um den neuen Eintrag erstellen. Wenn _CbEIDNewEntryTpl_ 0 und _LpEIDNewEntryTpl_ NULL ist, zeigt **NewEntry** ein Dialogfeld, mit dem den Benutzer aus einer Liste von Vorlagen für neue Einträge auswählen kann. 
    
 _lpcbEIDNewEntry_
  
> [out] Ein Zeiger auf die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LppEIDNewEntry_ verwiesen. 
    
 _lppEIDNewEntry_
  
> [out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID des neu erstellten Eintrags.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der neue Eintrag wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::NewEntry** -Methode wird für Address Book Anbieter Unterstützungsobjekte implementiert. Von adressbuchanbietern implementierte Aufrufen **NewEntry** zum Erstellen eines neuen Address Book Eintrags direkt in einem Container hinzugefügt werden soll oder verwendet werden, um eine ausgehende Nachricht zu adressieren. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie den neuen Eintrag auf einen bestimmten Container hinzugefügt werden soll, legen Sie _LpEIDContainer_ Eintrags-ID und _CbEIDContainer_ , um die Byteanzahl von in die Eintrags-ID des Containers. 
  
Wenn Sie den neuen Eintrag der Empfängerliste von ausgehenden Nachrichten hinzugefügt werden soll, legen Sie _LpEIDContainer_ auf NULL und _CbEIDContainer_ auf 0. 
  
Wenn den Benutzer von einer Clientanwendung aus, wählen Sie den Typ der Eintrag erstellt werden soll, übergeben Sie 0 in _CbEIDNewEntryTpl_ und NULL in _LpEIDNewEntryTpl_. **NewEntry** zeigt die einmalige MAPI-Tabelle, die eine Liste der Vorlagen, die MAPI und aller der adressbuchanbietern implementierte in der Sitzung zu unterstützen. Jede Vorlage kann ein Empfänger Eintrag für einen oder mehrere Adresstypen erstellt. 
  
Wenn Sie die Eintrags-ID des neuen Eintrags beibehalten möchten, übergeben Sie die Parameter _LpcbEIDNewEntry_ und _LppEIDNewEntry_ gültige Zeiger. Sie sind verantwortlich für das Freigeben von dieses Eintrags-ID, wenn Sie mit ihm fertig sind, durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion. 
  
Um eine bestimmte Vorlage verwenden, um einen neuen Eintrag einem änderbare Container hinzuzufügen, verwenden Sie die folgende Schritte aus:
  
1. Rufen Sie die [IMAPISupport::OpenEntry](imapisupport-openentry.md) -Methode zum Öffnen den Zielcontainer, und legen Sie den Parameter _LpEntryID_ auf die Eintrags-ID des Containers. 
    
2. Rufen Sie das Ziel des Containers [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode, und legen Sie den Parameter _UlPropTag_ **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) und der Parameter _Lpiid_ auf IID_IMAPITable. Der Container gibt eine einmalige Tabelle zurück, die alle Vorlagen aufgeführt werden, die sie zum Erstellen neuer Einträge unterstützt. 
    
3. Rufen Sie die Zeile, die die Vorlage für den angegebenen Typ des Eintrags darstellt, den Sie erstellen möchten. Die **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))-Spalte gibt den Typ der Adresse, der von der Vorlage unterstützt wird. 
    
4. Rufen Sie **IMAPISupport::NewEntry** , und legen Sie den Parameter _LpEIDNewEntryTpl_ auf die Eintrags-ID der ausgewählten Vorlage. Die Eintrags-ID ist die Spalte **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) aus der Vorlage Zeile in der einmaligen Tabelle. Übergeben Sie 0 in _CbEIDContainer_ und NULL in _LpEIDContainer_. Übergeben Sie einen gültigen Zeiger im _LppEIDNewEntry_ -Parameter, wenn Sie den neuen Eintrag Eintrags-ID beibehalten möchten. 
    
## <a name="see-also"></a>Siehe auch



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport::OpenEntry](imapisupport-openentry.md)
  
[Kanonische PidTagCreateTemplates-Eigenschaft](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

