---
title: IMAPISupportGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.GetOneOffTable
api_type:
- COM
ms.assetid: 6800fd3a-aa43-45fe-9cc2-102d0ef43edf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 55958af9d68ac27a92f06528dbc8fbc1fc62e574
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556511"
---
# <a name="imapisupportgetoneofftable"></a>IMAPISupport::GetOneOffTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Zeiger auf die EINMALIGE MAPI-Tabelle zurück (eine Liste der Vorlagen, die alle Adressbuchanbieter beim Erstellen neuer Empfänger unterstützen).
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der Zeichenfolgenspalten steuert. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgenspalten haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgenspalten das ANSI-Format.
    
 _lppTable_
  
> [out] Ein Zeiger auf einen Zeiger auf die einmalige Tabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die einmalige Tabelle wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::GetOneOffTable-Methode** ist für Supportobjekte des Adressbuchanbieters implementiert. Adressbuchanbieter rufen **GetOneOffTable** auf, um die vollständige Liste der Vorlagen zum Erstellen neuer Empfänger abzurufen. Diese Tabelle enthält Vorlagen, die von Adressbuchanbietern unterstützt werden, die in der Sitzungsunterstützung aktiv sind, sowie Vorlagen, die mapi unterstützt. 
  
Die neu erstellten Empfänger können verwendet werden, um eine Nachricht zu adressiert, oder sie können einem Adressbuchcontainer hinzugefügt werden.
  
Eine Liste der Eigenschaften, aus denen die erforderliche Spalte besteht, die in einmaligen Tabellen festgelegt ist, finden Sie unter ["Einmalige Tabellen".](one-off-tables.md)
  
Das Festlegen des MAPI_UNICODE Flags im  _ulFlags-Parameter_ wirkt sich auf das Format der Spalten aus, die von den Methoden [IMAPITable::QueryColumns](imapitable-querycolumns.md) und [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegeben werden. Dieses Flag steuert auch die Eigenschaftstypen in der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder-Methode](imapitable-querysortorder.md) zurückgegeben wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie für den Empfang von Benachrichtigungen über Änderungen an dieser einmaligen Tabelle registriert sind, erhalten Sie auch Benachrichtigungen über Änderungen an den einmaligen Tabellen anderer Anbieter. Basierend auf diesen Benachrichtigungen können Sie neue Adresstypen unterstützen, die während der aktuellen Sitzung hinzugefügt werden.
  
## <a name="see-also"></a>Siehe auch



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPISupport::NewEntry](imapisupport-newentry.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[PidTagCreateTemplates (kanonische Eigenschaft)](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Einmalige Tabellen](one-off-tables.md)

