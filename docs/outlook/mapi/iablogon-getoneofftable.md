---
title: IABLogonGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetOneOffTable
api_type:
- COM
ms.assetid: 7ac2a8d4-6890-4346-a6b6-34deca9dab50
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3732d8cbfaf9a6a10c62eae9e7a12b04de8a80ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583680"
---
# <a name="iablogongetoneofftable"></a>IABLogon::GetOneOffTable

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt eine Tabelle mit einmaligen Vorlagen zum Erstellen von Empfängern, die Empfängerliste von ausgehenden Nachrichten hinzugefügt werden soll.
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ der in der Tabelle enthaltenen Zeichenfolgenspalten steuert. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die Zeichenfolgenspalten sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, werden die Zeichenfolgenspalten im ANSI-Format.
    
 _lppTable_
  
> [out] Ein Zeiger auf einen Zeiger auf die einmaligen Tabelle.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die einmalige Tabelle wurde erfolgreich abgerufen.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und die Adressbuchanbieter unterstützt keine Unicode oder Parameter MAPI_UNICODE wurde nicht festgelegt und die Adressbuchanbieter unterstützt nur Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Der Adressbuchanbieter nicht einmal-Vorlagen zur Verfügung.
    
## <a name="remarks"></a>HinwBemerkungeneise

MAPI-Aufrufen die **GetOneOffTable** -Methode, um die verfügbare einmalige Vorlagen zum Erstellen von Empfängern tätigen. Die Empfängerliste von ausgehenden Nachrichten werden die neuen Empfänger hinzugefügt. Von adressbuchanbietern implementierte sollte Benachrichtigung auf ihre einmaligen Tabelle um MAPI Vorlage Änderungen informieren zu unterstützen. MAPI bleibt die einmalige Tabelle geöffnet, um dynamische Aktualisieren zu aktivieren. 
  
Von adressbuchanbietern implementierte können auch eine einmalige Tabelle für jeden ihrer Container unterstützen. Anrufer Abrufen dieser einmaligen Tabelle, des Containers [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode aufrufen und die Eigenschaft **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) anfordern. Über diese Tabelle verfügbaren Vorlagen dienen zum Empfänger zum Container hinzuzufügen. Eine Erläuterung der Unterschiede zwischen den beiden Typen von einmaligen Tabellen finden Sie unter [Implementieren der einmaligen Tabellen](implementing-one-off-tables.md).
  
Eine Übersicht über die erforderlichen Spalten in einer Adressbuchanbieter einmaligen Tabelle finden Sie unter [Einmaligen Tabellen](one-off-tables.md).
  
## <a name="see-also"></a>Siehe auch



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IAddrBook::NewEntry](iaddrbook-newentry.md)
  
[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

