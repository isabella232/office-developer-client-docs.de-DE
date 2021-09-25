---
title: IMAPITableSortTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.SortTable
api_type:
- COM
ms.assetid: ff5f78ac-06cf-46fb-93da-5f4a3a5d1b22
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 420b24254647a6a3fa420fed39b802d1858fe153
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625287"
---
# <a name="imapitablesorttable"></a>IMAPITable::SortTable

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die **IMAPITable::SortTable-Methode** sortiert die Zeilen der Tabelle, je nach Sortierkriterien. 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

_lpSortCriteria_
  
> [in] Zeiger auf eine [SSortOrderSet-Struktur,](ssortorderset.md) die die anzuwendenden Sortierkriterien enthält. Wenn Sie eine **SSortOrderSet-Struktur** übergeben, die Nullspalten enthält, bedeutet dies, dass die Tabelle nicht in einer bestimmten Reihenfolge sortiert werden muss. 
    
_ulFlags_
  
> [in] Bitmaske von Flags, die den Zeitpunkt des **IMAPITable::SortTable-Vorgangs** steuert. Die folgenden Flags können festgelegt werden: 
    
TBL_ASYNC 
  
> Startet den Vorgang asynchron und gibt zurück, bevor der Vorgang abgeschlossen ist.
    
TBL_BATCH 
  
> Verzögert den Abschluss der Sortierung, bis die Daten in der Tabelle erforderlich sind.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Sortiervorgang war erfolgreich.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Sortiervorgang gestartet wird. Entweder sollte der laufende Vorgang abgeschlossen werden können, oder er sollte beendet werden.
    
MAPI_E_NO_SUPPORT 
  
> Die Tabelle unterstützt den angeforderten Sortiertyp nicht.
    
MAPI_E_TOO_COMPLEX 
  
> Die Tabelle kann den Vorgang nicht ausführen, da die speziellen Sortierkriterien, auf die durch den  _Parameter lpSortCriteria_ verwiesen wird, zu komplex sind. **SortTable** kann unter den folgenden Bedingungen MAPI_E_TOO_COMPLEX zurückgeben. 
    
   - Ein Sortiervorgang wird für eine Eigenschaftsspalte angefordert, die von der Implementierung nicht sortiert werden kann.
    
   - Die Implementierung unterstützt nicht die Sortierreihenfolge, die im **ulOrder-Element** der **SSortOrderSet-Struktur** angefordert wird. 
    
   - Die Anzahl der zu sortierenden Spalten, wie im **cSorts-Element** in **SSortOrderSet** angegeben, ist größer, als die Implementierung verarbeiten kann.
    
   - Ein Sortiervorgang wird angefordert, wie durch ein Eigenschaftentag in **SSortOrderSet** angegeben, basierend auf einer Eigenschaft, die sich nicht im verfügbaren oder aktiven Satz befindet und die Implementierung keine Sortierung nach Eigenschaften unterstützt, die nicht im verfügbaren Satz enthalten sind.
    
   - Eine Eigenschaft wird mehrmals in einem Sortierreihenfolgesatz angegeben, wie durch mehrere Instanzen desselben Eigenschaftstags angegeben, und die Implementierung kann einen solchen Sortiervorgang nicht ausführen.
    
   - Ein Sortiervorgang basierend auf mehrwertigen Eigenschaftenspalten wird mit MVI_FLAG angefordert, und die Implementierung unterstützt keine Sortierung nach mehrwertigen Eigenschaften. 
    
   - Ein Eigenschaftstag für eine Eigenschaft in **SSortOrderSet** gibt eine Eigenschaft oder einen Typ an, die von der Implementierung nicht unterstützt wird. 
    
   - Ein anderer Sortiervorgang als einer, der die Tabelle von der **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) -Eigenschaft vorwärts durchläuft, wird nur für eine Anlagentabelle angegeben, die diesen Sortiertyp unterstützt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable::SortTable-Methode** ordnet die Zeilen in einer Tabellenansicht an. Während einige Tabellen sowohl die Standard- als auch die kategorisierte Sortierung nach verschiedenen Sortierschlüsselspalten unterstützen, sind andere Tabellen in ihrer Unterstützung eingeschränkter. Adressbuchanbieter unterstützen normalerweise keine Tabellensortierung. Nachrichtenspeicheranbieter unterstützen die Sortierung in der Regel so weit, dass sie die Sortierreihenfolge von Ordnern beibehalten, die sich ergeben, wenn eine vollständige Tabelle (eine Tabelle ohne Einschränkungen) sortiert wird. 
  
Einige Tabellen ermöglichen die Sortierung in einer beliebigen Tabellenspalte. Andere Tabellen nicht; Spalten, die nicht in der Tabellenansicht enthalten sind, sind von einem **SortTable-Aufruf** nicht betroffen. Einige Tabellen erfordern, dass Sortierschlüssel nur mit Spalten im aktuellen Spaltensatz der Tabelle erstellt werden. 
  
Eine Tabelle kann entweder MAPI_E_NO_SUPPORT oder MAPI_E_TOO_COMPLEX aus **SortTable** zurückgeben, wenn ein Sortiervorgang nicht abgeschlossen werden kann. Darüber hinaus ist es nicht garantiert, dass Speicheranbieter den für Hierarchietabellen angegebenen Sortierreihenfolgesatz berücksichtigen. 
  
Wenn die [SSortOrderSet-Struktur](ssortorderset.md) null Spalten enthält, auf die der  _Parameter lpSortCriteria_ verweist, gibt die Tabelle den aktuellen Spaltensatz zurück. Die aktuelle Sortierreihenfolge kann durch Aufrufen der [IMAPITable::QuerySortOrder-Methode](imapitable-querysortorder.md) der Tabelle abgerufen werden. 
  
Alle Textmarken für eine Tabelle werden ungültig und sollten gelöscht werden, wenn ein Aufruf von **SortTable** ausgeführt wird, und die BOOKMARK_CURRENT Textmarke, die die aktuelle Cursorposition angibt, sollte auf den Anfang der Tabelle festgelegt werden. 
  
Wenn Sie nach einer Spalte sortieren, die eine mehrwertige Eigenschaft ohne den MVI_FLAG Flagsatz enthält, werden die Werte der Spalte als vollständig sortiertes Tupel behandelt. Ein Vergleich von zwei mehrwertigen Spalten vergleicht die Spaltenelemente in der reihenfolge, wobei die Beziehung der Spalten bei der ersten Gleichung gemeldet wird, und gibt nur dann Gleichheit zurück, wenn die verglichenen Spalten dieselben Werte in derselben Reihenfolge enthalten. Wenn eine Spalte weniger Werte aufweist als die andere, ist die gemeldete Beziehung die eines NULL-Werts zum anderen Wert.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

**SortTable** wird synchron ausgeführt, es sei denn, Sie legen eines der Flags fest. Wenn Sie das flag TBL_BATCH festlegen, verschiebt **SortTable** den Sortiervorgang, es sei denn, Sie fordern die Daten an. Wenn das TBL_ASYNC Flag festgelegt ist, wird **SortTable** asynchron ausgeführt und wird möglicherweise vor Abschluss des Vorgangs zurückgegeben. 
  
Rufen Sie die [IMAPITable::Abort-Methode](imapitable-abort.md) auf, um einen laufenden asynchronen Vorgang zu beenden, wenn die Sortierung sofort durchgeführt werden muss. Wenn **SortTable** nicht fortgesetzt werden kann, weil ein oder mehrere asynchrone Vorgänge für die Tabelle ausgeführt werden, wird MAPI_E_BUSY zurückgegeben. 
  
Um eine optimale Leistung zu erzielen, rufen Sie **SetColumns** auf, um den Spaltensatz der Tabelle anzupassen, und **beschränken Sie** die Anzahl der Zeilen in der Tabelle, bevor Sie **SortTable** aufrufen, um die Sortierung durchzuführen. 
  
Wenn **SortTable** fehlschlägt, ist die Sortierreihenfolge, die vor dem Fehler wirksam war, weiterhin wirksam. 
  
## <a name="see-also"></a>Siehe auch

- [IMAPITable::Abort](imapitable-abort.md)
- [IMAPITable::GetRowCount](imapitable-getrowcount.md)
- [IMAPITable::QueryColumns](imapitable-querycolumns.md)
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
- [SSortOrderSet](ssortorderset.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)

