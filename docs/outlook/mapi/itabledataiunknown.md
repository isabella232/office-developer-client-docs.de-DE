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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3992bea899239ee5975505dec366490d6bbe1698
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430595"
---
# <a name="itabledata--iunknown"></a>ITableData : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt Hilfsmethoden für die Arbeit mit Tabellen zur Verfügung. MAPI stellt Tabellendatenobjekte oder -objekte zur Verfügung, die **ITableData** implementieren, um Dienstanbietern bei der Durchführung der Tabellenwartung zu helfen. Zum Abrufen eines Tabellendatenobjekts rufen Dienstanbieter die [CreateTable-Funktion](createtable.md) auf. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Tabellendatenobjekte  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPITableData  <br/> |
|Zeigertyp:  <br/> |LPTABLEDATA  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[HrGetView](itabledata-hrgetview.md) <br/> |Erstellt eine Tabellenansicht und gibt einen Zeiger auf eine [IMAPITable-Implementierung](imapitableiunknown.md) zurück.  <br/> |
|[HrModifyRow](itabledata-hrmodifyrow.md) <br/> |Fügt eine neue Tabellenzeile ein und ersetzt möglicherweise eine vorhandene Zeile.  <br/> |
|[HrDeleteRow](itabledata-hrdeleterow.md) <br/> |Löscht eine Tabellenzeile.  <br/> |
|[HrQueryRow](itabledata-hrqueryrow.md) <br/> |Ruft eine Tabellenzeile ab.  <br/> |
|[HrEnumRow](itabledata-hrenumrow.md) <br/> |Ruft eine Zeile basierend auf ihrer Position in der Tabelle ab.  <br/> |
|[HrNotify](itabledata-hrnotify.md) <br/> |Sendet eine Benachrichtigung für eine Tabellenzeile.  <br/> |
|[HrInsertRow](itabledata-hrinsertrow.md) <br/> |Fügt eine Tabellenzeile ein.  <br/> |
|[HrModifyRows](itabledata-hrmodifyrows.md) <br/> |Fügt mehrere Tabellenzeilen ein und ersetzt möglicherweise vorhandene Zeilen.  <br/> |
|[HrDeleteRows](itabledata-hrdeleterows.md) <br/> |Löscht mehrere Tabellenzeilen.  <br/> |
   
## <a name="remarks"></a>Hinweise

Die MAPI-Implementierung von **ITableData** funktioniert mit Tabellen, indem alle Daten und alle zugehörigen Einschränkungen im Arbeitsspeicher gespeichert werden, wodurch sie für die Verwendung mit sehr großen Tabellen ungeeignet ist. Große Einschränkungen und komplexe Vorgänge wie kategorisierung werden nicht unterstützt. 
  
Tabellendatenobjekte identifizieren Zeilen mithilfe einer Indexspalte, einer Eigenschaft, die garantiert einen eindeutigen Wert für jede Zeile hat. Die meisten Dienstanbieter **verwenden die PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) -Eigenschaft als Indexspalte. Eigenschaften mit mehreren Werten können nicht als Indexspalte verwendet werden.
  
Tabellendatenobjekte generieren unabhängig von der Anzahl der Zeilen, die von einer Änderung oder Löschung betroffen sind, eine einzelne Benachrichtigung. Wenn eine Zielzeile in einem Vorgang nicht vorhanden ist, wird eine Zeile hinzugefügt.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

