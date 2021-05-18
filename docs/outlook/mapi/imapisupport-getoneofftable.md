---
title: IMAPISupportGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetOneOffTable
api_type:
- COM
ms.assetid: 6800fd3a-aa43-45fe-9cc2-102d0ef43edf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c0beec8a0b234794d3f623c4ceac773db698dd79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412758"
---
# <a name="imapisupportgetoneofftable"></a>IMAPISupport::GetOneOffTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Zeiger auf die einmal aufgeführte MAPI-Tabelle zurück (eine Liste der Vorlagen, die von allen Adressbuchanbietern zum Erstellen neuer Empfänger unterstützt werden).
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der Zeichenfolgenspalten steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgenspalten sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgenspalten im ANSI-Format.
    
 _lppTable_
  
> [out] Ein Zeiger auf einen Zeiger auf die einmal aufgeführte Tabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die einmal aufgeführte Tabelle wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::GetOneOffTable-Methode** wird für Unterstützungsobjekte des Adressbuchanbieters implementiert. Adressbuchanbieter rufen **GetOneOffTable auf,** um die vollständige Liste der Vorlagen zum Erstellen neuer Empfänger abzurufen. Diese Tabelle enthält Vorlagen für Adressbuchanbieter, die in der Sitzungsunterstützung aktiv sind, sowie Vorlagen, die MAPI unterstützt. 
  
Die neu erstellten Empfänger können verwendet werden, um eine Nachricht zu adressiert oder einem Adressbuchcontainer hinzugefügt werden.
  
Eine Liste der Eigenschaften, aus der die erforderliche Spaltensatz in einmal festgelegten Tabellen ist, finden Sie unter [One-Off Tables](one-off-tables.md).
  
Das Festlegen MAPI_UNICODE im  _ulFlags-Parameter_ wirkt sich auf das Format der Spalten aus, die von den [Methoden IMAPITable::QueryColumns](imapitable-querycolumns.md) und [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegeben werden. Dieses Flag steuert auch die Eigenschaftstypen in der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder-Methode zurückgegeben](imapitable-querysortorder.md) wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie registriert sind, um Benachrichtigungen über Änderungen an dieser einmal erstellten Tabelle zu erhalten, erhalten Sie auch Benachrichtigungen über Änderungen an den einmal aufgeführten Tabellen anderer Anbieter. Basierend auf diesen Benachrichtigungen können Sie neue Adresstypen unterstützen, die während der aktuellen Sitzung hinzugefügt werden.
  
## <a name="see-also"></a>Siehe auch



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPISupport::NewEntry](imapisupport-newentry.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[PidTagCreateTemplates (kanonische Eigenschaft)](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Einmaltabellen](one-off-tables.md)

