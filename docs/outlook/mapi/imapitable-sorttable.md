---
title: IMAPITableSortTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SortTable
api_type:
- COM
ms.assetid: ff5f78ac-06cf-46fb-93da-5f4a3a5d1b22
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 46a87a6eb5c80244c04ae6257cd4441b8797ba36
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792480"
---
# <a name="imapitablesorttable"></a>SortTable

**Betrifft**: Outlook 
  
Die **SortTable** -Methode ordnet die Zeilen der Tabelle ist, je nach sortieren Kriterien. 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

_lpSortCriteria_
  
> [in] Zeiger auf eine [SSortOrderSet](ssortorderset.md) -Struktur, die die Sortierkriterien anzuwendende enthält. Übergeben eine **SSortOrderSet** -Struktur, die keine Spalten enthält, gibt an, dass die Tabelle nicht vorhanden ist, in einer bestimmten Reihenfolge sortiert werden sollen. 
    
_ulFlags_
  
> [in] Bitmaske aus Flags, die den Zeitpunkt des Vorgangs **SortTable** steuert. Die folgenden Kennzeichen können festgelegt werden: 
    
TBL_ASYNC 
  
> Die Operation asynchron startet und zurückgibt, bevor der Vorgang abgeschlossen ist.
    
TBL_BATCH 
  
> Nach Abschluss der Sortierung verzögert, bis die Daten in der Tabelle erforderlich ist.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Sortiervorgang war erfolgreich.
    
MAPI_E_BUSY 
  
> Ein anderer Vorgang wird ausgeführt, die den Sortiervorgang Neustart verhindert. Entweder dürfen der Vorgang in Arbeit abgeschlossen oder angehalten werden sollte.
    
MAPI_E_NO_SUPPORT 
  
> Die Tabelle unterstützt nicht den Typ der Sortierung angefordert.
    
MAPI_E_TOO_COMPLEX 
  
> Die Tabelle kann nicht den Vorgang ausgeführt werden, da die bestimmten Sortierkriterien auf das durch den Parameter _LpSortCriteria_ ist zu komplex. **SortTable** kann unter den folgenden Umständen MAPI_E_TOO_COMPLEX zurückgeben. 
    
   - Ein Sortiervorgang ist für eine Spalte angefordert, dass die Implementierung sortieren kann.
    
   - Die Implementierung unterstützt nicht die Sortierreihenfolge im **UlOrder** Member der Struktur **SSortOrderSet** angefordert. 
    
   - Die Anzahl der Spalten sortiert werden, wie in den **cSorts** Member in **SSortOrderSet**angegeben, ist größer als die Implementierung verarbeitet werden kann.
    
   - Ein Sortiervorgang angefordert, gekennzeichnet durch ein Tag-Eigenschaft in **SSortOrderSet**, basierend auf einer Eigenschaft, die nicht in der Sammlung verfügbar oder aktiv ist und die Implementierung unterstützt nicht das Sortieren nach Eigenschaften nicht in der verfügbare Satz.
    
   - Eine Eigenschaft angegeben ist mehrmals in einer Reihenfolge sortiert, wie mehrere Instanzen des gleichen Eigenschaftstags angegeben, und die Implementierung dieser einen Sortiervorgang kann nicht ausgeführt werden.
    
   - Ein mehrwertige Eigenschaftenspalten Grundlage Sortiervorgang ist mit MVI_FLAG angefordert und die Implementierung die Sortierung auf mehrwertige Eigenschaften nicht unterstützt. 
    
   - Ein Eigenschaftentag für eine Eigenschaft im **SSortOrderSet** gibt eine Eigenschaft oder Typ, der die Implementierung nicht unterstützt. 
    
   - Ein Sortiervorgang, die durch die Tabelle aus der **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))-Eigenschaft vorwärts wird fortgesetzt wird nur für eine Anlagentabelle angegeben, die diese Art der Sortierung unterstützt.
    
## <a name="remarks"></a>Hinweise

Die **SortTable** -Methode ordnet die Zeilen in einer Tabellenansicht. Während einige Tabellen Standard- und kategorisierten auf verschiedenen Sortierschlüsselspalten Sortierung unterstützt wird, sind die Unterstützung mehr anderen Tabellen beschränkt. Von adressbuchanbietern implementierte unterstützt normalerweise nicht Sortierung. Nachricht Anbieter unterstützen normalerweise sortieren, wenn sie aufzubewahren, der die Sortierreihenfolge der Ordner, die entsteht, wenn eine vollständige Tabelle (einer Tabelle ohne Einschränkungen) sortiert ist. 
  
Einige Tabellen zulassen Sortierung auf keiner Tabellenspalte erfolgen. Andere Tabellen nicht; Spalten, die nicht in der Tabellenansicht enthalten sind durch einen Aufruf der **SortTable** nicht betroffen. Einige Tabellen erfordern, dass Sortierschlüsseln nur mit Spalten in der Tabelle aktuellen Spalte Gruppe erstellt werden. 
  
Eine Tabelle kann entweder MAPI_E_NO_SUPPORT oder MAPI_E_TOO_COMPLEX aus **SortTable** zurückgeben, wenn einen Sortiervorgang abgeschlossen werden kann. Darüber hinaus sind Anbieter nicht unbedingt berücksichtigt die Sortierreihenfolge für Hierarchietabellen angegebenen festgelegt. 
  
Wenn keine Spalten in der [SSortOrderSet](ssortorderset.md) -Struktur, die auf das durch den Parameter _LpSortCriteria_ vorhanden sind, wird die Tabelle die aktuellen Spalte Gruppe zurückgegeben. Die aktuelle Sortierreihenfolge kann durch Aufrufen der Tabelle [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) -Methode abgerufen werden. 
  
Alle Lesezeichen für eine Tabelle ungültig sind, und bei **SortTable** wird aufgerufen, und die BOOKMARK_CURRENT Textmarke, die angibt, die aktuellen Cursorposition festgelegt werden sollte, an den Anfang der Tabelle gelöscht werden soll. 
  
Wenn Sie auf eine Spalte, die eine mehrwertige Eigenschaft, ohne die MVI_FLAG-Flag enthält sortieren, werden die Werte der Spalte als vollständig geordnete Tupel behandelt. Ein Vergleich von zwei Spalten mit mehreren Werten vergleicht die Spalte Elemente in der Reihenfolge, die Beziehung der Spalten auf der ersten Ungleichheit, reporting und Gleichheit nur zurückgegeben, wenn die zu vergleichenden Spalten dieselben Werte wie in der gleichen Reihenfolge enthalten. Wenn eine Spalte weniger Werte als die andere verfügt, kann die gemeldete Beziehung, die über einen null-Wert auf den anderen Wert.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

**SortTable** arbeitet synchron, es sei denn, Sie eines der Flags festlegen. Wenn Sie das TBL_BATCH-Flag festlegen, verschiebt **SortTable** Sortiervorgang, es sei denn, Sie die Daten anfordern. Wenn das Flag TBL_ASYNC festgelegt ist, arbeitet **SortTable** asynchron potenziell vor dem Abschluss des Vorgangs zurückgeben. 
  
Rufen Sie die [IMAPITable::Abort](imapitable-abort.md) -Methode, um einer asynchronen Operation in Bearbeitung beenden, wenn die Sortierung sofort ausgeführt werden muss. Wenn **SortTable** fortgesetzt werden kann, da eine oder mehrere asynchrone Vorgänge in der Tabelle ausgeführt werden, wird MAPI_E_BUSY zurückgegeben. 
  
Rufen Sie für eine optimale Leistung **SetColumns** zum Anpassen der Tabelle Spalte festlegen und **Restrict** zur Begrenzung der Anzahl der Zeilen in der Tabelle vor dem Aufrufen der **SortTable** , um die Sortierung durchzuführen. 
  
Bei jedem **SortTable** ein Fehler auftritt, wird die Sortierreihenfolge, die vor dem Ausfall gültig war noch wirksam. 
  
## <a name="see-also"></a>Siehe auch

- [IMAPITable::Abort](imapitable-abort.md)
- [IMAPITable::GetRowCount](imapitable-getrowcount.md)
- [IMAPITable::QueryColumns](imapitable-querycolumns.md)
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
- [SSortOrderSet](ssortorderset.md)
- [IMAPITable: IUnknown](imapitableiunknown.md)

