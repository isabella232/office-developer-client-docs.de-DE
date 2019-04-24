---
title: ITableData IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData
api_type:
- COM
ms.assetid: ac7ae09f-ce19-45cf-8963-fad5bba75452
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3992bea899239ee5975505dec366490d6bbe1698
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348769"
---
# <a name="itabledata--iunknown"></a>ITableData : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt Dienstprogrammmethoden zum Arbeiten mit Tabellen bereit. MAPI stellt Tabellendaten Objekte oder Objekte bereit, die **ITableData** implementieren, um Dienstanbieter bei der Tabellenwartung zu unterstützen. Zum Abrufen eines Tabellendaten Objekts rufen Dienstanbieter die CreateTable-Funktion auf. [](createtable.md) 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Tabellendaten Objekte  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPITableData  <br/> |
|Zeigertyp:  <br/> |LPTABLEDATA  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[HrGetView](itabledata-hrgetview.md) <br/> |Erstellt eine Tabellenansicht und gibt einen Zeiger auf eine [IMAPITable](imapitableiunknown.md) -Implementierung zurück.  <br/> |
|[HrModifyRow](itabledata-hrmodifyrow.md) <br/> |Fügt eine neue Tabellenzeile ein, die möglicherweise eine vorhandene Zeile ersetzt.  <br/> |
|[HrDeleteRow](itabledata-hrdeleterow.md) <br/> |Löscht eine Tabellenzeile.  <br/> |
|[HrQueryRow](itabledata-hrqueryrow.md) <br/> |Ruft eine Tabellenzeile ab.  <br/> |
|[HrEnumRow](itabledata-hrenumrow.md) <br/> |Ruft eine Zeile basierend auf ihrer Position in der Tabelle ab.  <br/> |
|[HrNotify](itabledata-hrnotify.md) <br/> |Sendet eine Benachrichtigung für eine Tabellenzeile.  <br/> |
|[HrInsertRow](itabledata-hrinsertrow.md) <br/> |Fügt eine Tabellenzeile ein.  <br/> |
|[HrModifyRows](itabledata-hrmodifyrows.md) <br/> |Fügt mehrere Tabellenzeilen ein, die möglicherweise vorhandene Zeilen ersetzen.  <br/> |
|[HrDeleteRows](itabledata-hrdeleterows.md) <br/> |Löscht mehrere Tabellenzeilen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die MAPI-Implementierung von **ITableData** funktioniert mit Tabellen, indem alle Daten und zugeordneten Einschränkungen im Arbeitsspeicher gespeichert werden, sodass Sie nicht für sehr große Tabellen verwendet werden können. Umfangreiche Einschränkungen und komplexe Vorgänge wie Kategorisierung werden nicht unterstützt. 
  
Tabellendaten Objekte identifizieren Zeilen mithilfe einer Indexspalte, einer Eigenschaft, die garantiert einen eindeutigen Wert für jede Zeile hat. Die meisten Dienstanbieter verwenden die **PR_INSTANCE_KEY** ([pidtaginstancekey (](pidtaginstancekey-canonical-property.md))-Eigenschaft als Indexspalte. Eigenschaften mit mehreren Werten können nicht als Indexspalte verwendet werden.
  
Tabellendaten Objekte generieren eine einzelne Benachrichtigung, unabhängig von der Anzahl von Zeilen, die von einer Änderung oder Löschung betroffen sind. Wenn eine Ziel Zeile in einem Vorgang nicht vorhanden ist, wird eine Zeile hinzugefügt.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

