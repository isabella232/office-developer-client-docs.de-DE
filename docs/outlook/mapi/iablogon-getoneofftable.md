---
title: IABLogonGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.GetOneOffTable
api_type:
- COM
ms.assetid: 7ac2a8d4-6890-4346-a6b6-34deca9dab50
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8c119c9f11ad38f2cb3eaa8916e16496187dda02
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610741"
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
  
> [in] Eine Bitmaske mit Flags, die den Typ der in der Tabelle enthaltenen Zeichenfolgenspalten steuert. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgenspalten haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgenspalten das ANSI-Format.
    
 _lppTable_
  
> [out] Ein Zeiger auf einen Zeiger auf die einmalige Tabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die einmalige Tabelle wurde erfolgreich abgerufen.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das flag MAPI_UNICODE festgelegt, und der Adressbuchanbieter unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und der Adressbuchanbieter unterstützt nur Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Der Adressbuchanbieter stellt keine einmaligen Vorlagen bereit.
    
## <a name="remarks"></a>HinwBemerkungeneise

MAPI ruft die **GetOneOffTable-Methode** auf, um einmalige Vorlagen zum Erstellen von Empfängern verfügbar zu machen. Die neuen Empfänger werden der Empfängerliste einer ausgehenden Nachricht hinzugefügt. Adressbuchanbieter sollten Benachrichtigungen auf ihrer einmaligen Tabelle unterstützen, um MAPI über Vorlagenänderungen zu informieren. DIE MAPI hält die einmalige Tabelle geöffnet, um die dynamische Aktualisierung zu ermöglichen. 
  
Adressbuchanbieter können auch eine einmalige Tabelle für jeden container unterstützen. Aufrufer rufen diese einmalige Tabelle ab, indem sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des Containers aufrufen und die **eigenschaft PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) anfordern. Die in dieser Tabelle verfügbaren Vorlagen werden verwendet, um dem Container Empfänger hinzuzufügen. Eine Erläuterung der Unterschiede zwischen den beiden Typen von einmaligen Tabellen finden Sie unter [Implementieren von One-Off Tabellen.](implementing-one-off-tables.md)
  
Eine Liste der erforderlichen Spalten in der einmaligen Tabelle eines Adressbuchanbieters finden Sie unter ["Einmalige Tabellen".](one-off-tables.md)
  
## <a name="see-also"></a>Siehe auch



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IAddrBook::NewEntry](iaddrbook-newentry.md)
  
[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

