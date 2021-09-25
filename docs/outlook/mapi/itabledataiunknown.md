---
title: ITableData IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData
api_type:
- COM
ms.assetid: ac7ae09f-ce19-45cf-8963-fad5bba75452
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ac60e3691f64ab932f7d8a53370f43efaa0fa9ce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571563"
---
# <a name="itabledata--iunknown"></a>ITableData : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt Hilfsmethoden zum Arbeiten mit Tabellen bereit. MAPI stellt Tabellendatenobjekte oder -objekte bereit, die **ITableData** implementieren, um Dienstanbieter bei der Tabellenwartung zu unterstützen. Zum Abrufen eines Tabellendatenobjekts rufen Dienstanbieter die [CreateTable-Funktion](createtable.md) auf. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Tabellendatenobjekte  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPITableData  <br/> |
|Zeigertyp:  <br/> |LPTABLEDATA  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[HrGetView](itabledata-hrgetview.md) <br/> |Erstellt eine Tabellenansicht und gibt einen Zeiger auf eine [IMAPITable-Implementierung](imapitableiunknown.md) zurück.  <br/> |
|[HrModifyRow](itabledata-hrmodifyrow.md) <br/> |Fügt eine neue Tabellenzeile ein, wobei möglicherweise eine vorhandene Zeile ersetzt wird.  <br/> |
|[HrDeleteRow](itabledata-hrdeleterow.md) <br/> |Löscht eine Tabellenzeile.  <br/> |
|[HrQueryRow](itabledata-hrqueryrow.md) <br/> |Ruft eine Tabellenzeile ab.  <br/> |
|[HrEnumRow](itabledata-hrenumrow.md) <br/> |Ruft eine Zeile basierend auf ihrer Position in der Tabelle ab.  <br/> |
|[HrNotify](itabledata-hrnotify.md) <br/> |Sendet eine Benachrichtigung für eine Tabellenzeile.  <br/> |
|[HrInsertRow](itabledata-hrinsertrow.md) <br/> |Fügt eine Tabellenzeile ein.  <br/> |
|[HrModifyRows](itabledata-hrmodifyrows.md) <br/> |Fügt mehrere Tabellenzeilen ein, wobei möglicherweise vorhandene Zeilen ersetzt werden.  <br/> |
|[HrDeleteRows](itabledata-hrdeleterows.md) <br/> |Löscht mehrere Tabellenzeilen.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die MAPI-Implementierung von **ITableData** funktioniert mit Tabellen, indem alle Daten und alle zugehörigen Einschränkungen im Speicher gespeichert werden, sodass sie nicht für die Verwendung mit sehr großen Tabellen geeignet sind. Umfangreiche Einschränkungen und komplexe Vorgänge wie kategorisierung werden nicht unterstützt. 
  
Tabellendatenobjekte identifizieren Zeilen mithilfe einer Indexspalte, einer Eigenschaft, die garantiert einen eindeutigen Wert für jede Zeile aufweist. Die meisten Dienstanbieter verwenden die **Eigenschaft PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) als Indexspalte. Eigenschaften mit mehreren Werten können nicht als Indexspalte verwendet werden.
  
Tabellendatenobjekte generieren eine einzelne Benachrichtigung, unabhängig von der Anzahl der Zeilen, die von einer Änderung oder löschung betroffen sind. Wenn keine Zielzeile in einem Vorgang vorhanden ist, wird eine Zeile hinzugefügt.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

