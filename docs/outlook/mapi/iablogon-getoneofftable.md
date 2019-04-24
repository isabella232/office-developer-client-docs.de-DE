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
ms.openlocfilehash: 326a78ed512ec82a9f16b1540aad60954ab2d864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338409"
---
# <a name="iablogongetoneofftable"></a>IABLogon::GetOneOffTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine Tabelle mit einmaligen Vorlagen zum Erstellen von Empfängern zurück, die der Empfängerliste einer ausgehenden Nachricht hinzugefügt werden sollen.
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Typ der Zeichenfolgenspalten in der Tabelle steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgenspalten sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sind die Zeichenfolgenspalten im ANSI-Format.
    
 _lppTable_
  
> Out Ein Zeiger auf einen Zeiger auf die einmalige Tabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die einmalige Tabelle wurde erfolgreich abgerufen.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und der Adressbuchanbieter unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und der Adressbuchanbieter unterstützt nur Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Der Adressbuchanbieter liefert keine einmaligen Vorlagen.
    
## <a name="remarks"></a>Bemerkungen

MAPI Ruft die **GetOneOffTable** -Methode auf, um für die Erstellung von Empfängern einmalige Vorlagen zur Verfügung zu stellen. Die neuen Empfänger werden der Empfängerliste einer ausgehenden Nachricht hinzugefügt. Adressbuchanbieter sollten die Benachrichtigung über ihre einmalige Tabelle unterstützen, um MAPI über Vorlagenänderungen zu informieren. MAPI hält die einmalige Tabelle geöffnet, um dynamische Updates zu aktivieren. 
  
Adressbuchanbieter können auch eine einmalige Tabelle für jeden ihrer Container unterstützen. Aufrufer rufen diese einmalige Tabelle ab, indem Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode des Containers aufrufen und die **PR_CREATE_TEMPLATES** ([pidtagcreatetemplates (](pidtagcreatetemplates-canonical-property.md))-Eigenschaft anfordern. Die über diese Tabelle verfügbaren Vorlagen werden zum Hinzufügen von Empfängern zum Container verwendet. Eine Erläuterung der Unterschiede zwischen den beiden Arten von einmaligen Tabellen finden Sie unter [Implementieren von einmal Tabellen](implementing-one-off-tables.md).
  
Eine Liste der erforderlichen Spalten in der einmaligen Tabelle eines Adressbuch Anbieters finden Sie unter [einmalige Tabellen](one-off-tables.md).
  
## <a name="see-also"></a>Siehe auch



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IAddrBook::NewEntry](iaddrbook-newentry.md)
  
[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

