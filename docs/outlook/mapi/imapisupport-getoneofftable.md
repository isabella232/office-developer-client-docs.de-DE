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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316576"
---
# <a name="imapisupportgetoneofftable"></a>IMAPISupport::GetOneOffTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Zeiger auf die MAPI-einmalige Tabelle zurück (eine Liste von Vorlagen, die von allen Adressbuch Anbietern für das Erstellen neuer Empfänger unterstützt werden).
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Typ der Zeichenfolgenspalten steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgenspalten sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sind die Zeichenfolgenspalten im ANSI-Format.
    
 _lppTable_
  
> Out Ein Zeiger auf einen Zeiger auf die einmalige Tabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die einmalige Tabelle wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: GetOneOffTable** -Methode wird für Support Objekte des Adressbuch Anbieters implementiert. Adressbuchanbieter rufen **GetOneOffTable** auf, um die vollständige Liste der Vorlagen zum Erstellen neuer Empfänger abzurufen. Diese Tabelle enthält Vorlagen für Adressbuchanbieter, die in der Sitzungsunterstützung aktiv sind, sowie Vorlagen, die von MAPI unterstützt werden. 
  
Die neu erstellten Empfänger können verwendet werden, um eine Nachricht zu adressieren oder einem Adressbuchcontainer hinzugefügt werden.
  
Eine Liste der Eigenschaften, die den erforderlichen Spaltensatz in einmaligen Tabellen bilden, finden Sie unter [einmalige Tabellen](one-off-tables.md).
  
Das Festlegen des MAPI_UNICODE-Flags im _ulFlags_ -Parameter wirkt sich auf das Format der Spalten aus, die von den Methoden [IMAPITable:: QueryColumns](imapitable-querycolumns.md) und [IMAPITable:: QueryRows](imapitable-queryrows.md) zurückgegeben werden. Dieses Flag steuert auch die Eigenschaftentypen in der von der [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) -Methode zurückgegebenen Sortierreihenfolge. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie für den Erhalt von Benachrichtigungen über Änderungen an dieser einmaligen Tabelle registriert sind, erhalten Sie auch Benachrichtigungen über Änderungen an den einmaligen Tabellen anderer Anbieter. Basierend auf diesen Benachrichtigungen können Sie neue Adresstypen unterstützen, die während der aktuellen Sitzung hinzugefügt werden.
  
## <a name="see-also"></a>Siehe auch



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPISupport::NewEntry](imapisupport-newentry.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[Kanonische Pidtagcreatetemplates (-Eigenschaft](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Einmalige Tabellen](one-off-tables.md)

