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
  
Fügt einen neuen Empfänger direkt einem Adressbuchcontainer oder der Empfängerliste einer ausgehenden Nachricht hinzu.
  
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
  
> in Ein Handle für das übergeordnete Fenster des Dialogfelds.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _cbEIDContainer_
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEIDContainer_ -Parameter verwiesen wird. 
    
 _lpEIDContainer_
  
> in Ein Zeiger auf die Eintrags-ID des Containers, um den neuen Eintrag zu empfangen. Wenn _cbEIDContainer_ 0 ist und _LPEIDCONTAINER_ den Wert NULL **** hat, erstellt der Neueintrag eine einmalige Eintrags-ID, die denselben Typ aufweist wie bei einem Aufruf der [IMAPISupport:: CreateOneOff](imapisupport-createoneoff.md) -Methode. 
    
 _cbEIDNewEntryTpl_
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEIDNewEntryTpl_ -Parameter verwiesen wird. 
    
 _lpEIDNewEntryTpl_
  
> in Ein Zeiger auf den Eintragsbezeichner der Vorlage, die zum Erstellen des neuen Eintrags verwendet werden soll. Wenn _cbEIDNewEntryTpl_ 0 und _lpEIDNewEntryTpl_ ist, zeigt der neue **Eintrag** ein Dialogfeld an, in dem der Benutzer aus einer Liste von Vorlagen zum Hinzufügen neuer Einträge auswählen kann. 
    
 _lpcbEIDNewEntry_
  
> Out Ein Zeiger auf die Bytezahl in der Eintrags-ID, auf die durch den _lppEIDNewEntry_ -Parameter verwiesen wird. 
    
 _lppEIDNewEntry_
  
> Out Ein Zeiger auf einen Zeiger auf die Eintrags-ID des neu erstellten Eintrags.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der neue Eintrag wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: neuentry** -Methode wird für Support Objekte des Adressbuch Anbieters implementiert. Adressbuchanbieter rufen **** den neueintrags auf, um einen neuen Adressbucheintrag zu erstellen, der direkt zu einem Container hinzugefügt oder zur Behebung einer ausgehenden Nachricht verwendet werden soll. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn der neue Eintrag einem bestimmten Container hinzugefügt werden soll, legen Sie _lpEIDContainer_ auf die Eintrags-ID des Containers und _cbEIDContainer_ auf die Bytezahl in der Eintrags-ID fest. 
  
Wenn der neue Eintrag der Empfängerliste einer ausgehenden Nachricht hinzugefügt werden soll, legen Sie _lpEIDContainer_ auf NULL und _cbEIDContainer_ auf 0 fest. 
  
Wenn Sie zulassen möchten, dass der Benutzer einer Clientanwendung den Typ des zu erstellenden Eintrags auswählen kann, geben Sie 0 in _cbEIDNewEntryTpl_ und NULL in _lpEIDNewEntryTpl_. Bei der erneuten **Eingabe** wird die MAPI-einmalige Tabelle, eine Liste der Vorlagen, die MAPI und die einzelnen Adressbuchanbieter in der Sitzung unterstützen, angezeigt. Jede Vorlage kann einen Empfängereintrag für einen oder mehrere Adresstypen erstellen. 
  
Wenn Sie die Eintrags-ID des neuen Eintrags behalten möchten, übergeben Sie gültige Zeiger in den Parametern _lpcbEIDNewEntry_ und _lppEIDNewEntry_ . Sie sind für die Freigabe dieser Eintrags-ID verantwortlich, wenn Sie damit fertig sind, indem Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufrufen. 
  
Gehen Sie folgendermaßen vor, um eine bestimmte Vorlage zum Hinzufügen eines neuen Eintrags zu einem änderbaren Container zu verwenden:
  
1. Rufen Sie die [IMAPISupport:: OpenEntry](imapisupport-openentry.md) -Methode auf, um den Zielcontainer zu öffnen, und legen Sie den Parameter _lpEntryID_ auf den Eintragsbezeichner des Containers fest. 
    
2. Rufen Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode des Zielcontainers auf, und legen Sie den Parameter _ulPropTag_ auf **PR_CREATE_TEMPLATES** ([pidtagcreatetemplates (](pidtagcreatetemplates-canonical-property.md)) und den _lpIID_ -Parameter auf IID_IMAPITable fest. Der Container gibt eine einmalige Tabelle zurück, in der alle Vorlagen aufgeführt sind, die für das Erstellen neuer Einträge unterstützt werden. 
    
3. Rufen Sie die Zeile ab, die die Vorlage für den jeweiligen Eintragstyp darstellt, den Sie erstellen möchten. Die **PR_ADDRTYPE** ([pidtagaddresstype (](pidtagaddresstype-canonical-property.md)) gibt den von der Vorlage unterstützten Adresstyp an. 
    
4. Rufen Sie **IMAPISupport:: neuentry** auf, und legen Sie den Parameter _lpEIDNewEntryTpl_ auf den Eintragsbezeichner der ausgewählten Vorlage fest. Die Eintrags-ID ist die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Spalte aus der Zeile der Vorlage in der einmaligen Tabelle. Übergibt 0 in _cbEIDContainer_ und NULL in _lpEIDContainer_. Übergeben Sie einen gültigen Zeiger im _lppEIDNewEntry_ -Parameter, wenn Sie die Eintrags-ID des neuen Eintrags aufbewahren möchten. 
    
## <a name="see-also"></a>Siehe auch



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport::OpenEntry](imapisupport-openentry.md)
  
[Kanonische Pidtagcreatetemplates (-Eigenschaft](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

