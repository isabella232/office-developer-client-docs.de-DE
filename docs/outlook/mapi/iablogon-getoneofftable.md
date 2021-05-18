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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411876"
---
# <a name="iablogongetoneofftable"></a>IABLogon::GetOneOffTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine Tabelle mit einmal erstellten Vorlagen zum Erstellen von Empfängern zurück, die der Empfängerliste einer ausgehenden Nachricht hinzugefügt werden sollen.
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ von Zeichenfolgenspalten steuert, die in der Tabelle enthalten sind. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgenspalten sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgenspalten im ANSI-Format.
    
 _lppTable_
  
> [out] Ein Zeiger auf einen Zeiger auf die einmal aufgeführte Tabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die einmal aufgeführte Tabelle wurde erfolgreich abgerufen.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde MAPI_UNICODE-Flag festgelegt, und der Adressbuchanbieter unterstützt Unicode nicht, oder MAPI_UNICODE nicht festgelegt, und der Adressbuchanbieter unterstützt nur Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Der Adressbuchanbieter stellt keine einmal verwendeten Vorlagen bereit.
    
## <a name="remarks"></a>Hinweise

MAPI ruft die **GetOneOffTable-Methode** auf, um einmal verfügbare Vorlagen zum Erstellen von Empfängern zur Verfügung zu stellen. Die neuen Empfänger werden der Empfängerliste einer ausgehenden Nachricht hinzugefügt. Adressbuchanbieter sollten Benachrichtigungen in ihrer einmal erstellten Tabelle unterstützen, um MAPI über Vorlagenänderungen zu informieren. MAPI hält die einmal aufgeführte Tabelle offen, um dynamische Aktualisierungen zu ermöglichen. 
  
Adressbuchanbieter können auch eine einzelne Tabelle für jeden container unterstützen. Aufrufer rufen diese einmaltabelle ab, indem sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des Containers aufrufen und die **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) -Eigenschaft anfordern. Die in dieser Tabelle verfügbaren Vorlagen werden zum Hinzufügen von Empfängern zum Container verwendet. Eine Diskussion über die Unterschiede zwischen den beiden Arten von einmal erstellten Tabellen finden Sie unter [Implementing One-Off Tables](implementing-one-off-tables.md).
  
Eine Liste der erforderlichen Spalten in der Einmaltabelle eines Adressbuchanbieters finden Sie unter [One-Off Tables](one-off-tables.md).
  
## <a name="see-also"></a>Siehe auch



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IAddrBook::NewEntry](iaddrbook-newentry.md)
  
[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

