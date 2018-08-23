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
ms.openlocfilehash: d54487928abcc889441ec9bf89ab6a10e5290062
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570835"
---
# <a name="imapisupportgetoneofftable"></a>IMAPISupport::GetOneOffTable

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt einen Zeiger auf die einmaligen MAPI-Tabelle (eine Liste der Vorlagen, dass alle Anbieter für die Unterstützung für das Erstellen von neuen Empfänger Adressbuch).
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ der Zeichenfolgenspalten steuert. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die Zeichenfolgenspalten sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, werden die Zeichenfolgenspalten im ANSI-Format.
    
 _lppTable_
  
> [out] Ein Zeiger auf einen Zeiger auf die einmaligen Tabelle.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die einmalige Tabelle wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::GetOneOffTable** -Methode wird für Address Book Anbieter Unterstützungsobjekte implementiert. Von adressbuchanbietern implementierte Aufrufen **GetOneOffTable** , um die vollständige Liste der Vorlagen zum Erstellen von neuen Empfänger abzurufen. Die folgende Tabelle enthält Vorlagen, die Unterstützung von adressbuchanbietern implementierte, die in der Sitzung aktiv sind, sowie Formularvorlagen, die MAPI unterstützt. 
  
Die neu erstellten Empfänger können verwendet werden, um eine Nachricht oder ein Adressbuchcontainer hinzugefügt werden können.
  
Eine Liste der Eigenschaften, die die erforderliche Spalte festlegen in einmaligen Tabellen bilden, finden Sie unter [Einmaligen Tabellen](one-off-tables.md).
  
Festlegen der Option MAPI_UNICODE im Parameter _UlFlags_ wirkt sich auf das Format der von den Methoden [IMAPITable::QueryColumns](imapitable-querycolumns.md) und [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegebenen Spalten aus. Dieses Kennzeichen steuert auch die Eigenschaftentypen in der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) -Methode zurückgegeben. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie Erhalt von Benachrichtigungen von Änderungen an dieser einmaligen Tabelle registriert sind, erhalten Sie auch Benachrichtigungen von Änderungen an andere Anbieter einmaligen Tabellen. Basierend auf diese Benachrichtigungen, können Sie neue Adresstypen unterstützen, die während der aktuellen Sitzung hinzugefügt werden.
  
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

