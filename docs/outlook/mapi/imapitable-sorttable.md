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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f16ba9164d55fdb7bd688d4068f99dc4407e5413
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432366"
---
# <a name="imapitablesorttable"></a>IMAPITable::SortTable

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die **IMAPITable:: sortable** -Methode sortiert die Zeilen der Tabelle, je nach Sortierkriterien. 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

_lpSortCriteria_
  
> in Zeiger auf eine [SSortOrderSet](ssortorderset.md) -Struktur, die die anzuwendenden Sortierkriterien enthält. Durch das Übergeben einer **SSortOrderSet** -Struktur mit NULL-Spalten wird angegeben, dass die Tabelle nicht in einer bestimmten Reihenfolge sortiert werden muss. 
    
_ulFlags_
  
> in Bitmaske von Flags, die das Timing des **IMAPITable:: sortable** -Vorgangs steuert. Die folgenden Flags können festgelegt werden: 
    
TBL_ASYNC 
  
> Startet den Vorgang asynchron und wird zurückgegeben, bevor der Vorgang abgeschlossen ist.
    
TBL_BATCH 
  
> Verschiebt den Abschluss des Sortiervorgangs, bis die Daten in der Tabelle erforderlich sind.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Sortiervorgang war erfolgreich.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Sortiervorgang gestartet wird. Entweder sollte der ausgeführte Vorgang abgeschlossen oder beendet werden.
    
MAPI_E_NO_SUPPORT 
  
> Die Tabelle unterstützt den angeforderten Sortiertyp nicht.
    
MAPI_E_TOO_COMPLEX 
  
> Die Tabelle kann den Vorgang nicht ausführen, da die bestimmten Sortierkriterien, auf die durch den _lpSortCriteria_ -Parameter verwiesen wird, zu komplex sind. **Sortable** kann MAPI_E_TOO_COMPLEX unter den folgenden Bedingungen zurückgeben. 
    
   - Ein Sortiervorgang wird für eine Eigenschaftsspalte angefordert, die von der Implementierung nicht sortiert werden kann.
    
   - Die Implementierung unterstützt nicht die im **ulOrder** -Element der **SSortOrderSet** -Struktur angeforderte Sortierreihenfolge. 
    
   - Die Anzahl der zu sortierenden Spalten, wie im **cSorts** -Element in **SSortOrderSet**angegeben, ist größer als die Implementierung verarbeiten kann.
    
   - Ein Sortiervorgang wird, wie durch ein Property-Tag in **SSortOrderSet**angegeben, angefordert, basierend auf einer Eigenschaft, die sich nicht im verfügbaren oder aktiven Satz befindet, und die Implementierung unterstützt das Sortieren von Eigenschaften nicht im verfügbaren Satz.
    
   - Eine Eigenschaft wird mehrmals in einem Sortier Reihenfolge-Satz angegeben, wie durch mehrere Instanzen desselben Property-Tags angegeben, und die Implementierung kann keinen solchen Sortiervorgang ausführen.
    
   - Ein Sortiervorgang basierend auf mehrwertigen Eigenschaftsspalten wird mithilfe von MVI_FLAG angefordert, und die Implementierung unterstützt das Sortieren von mehrwertigen Eigenschaften nicht. 
    
   - Ein Property-Tag für eine Eigenschaft in **SSortOrderSet** gibt eine Eigenschaft oder einen Typ an, die von der Implementierung nicht unterstützt wird. 
    
   - Ein anderer Sortiervorgang als einer, der die Tabelle aus der **PR_RENDERING_POSITION** ([pidtagrenderingposition (](pidtagrenderingposition-canonical-property.md))-Eigenschaft Forward durchläuft, wird nur für eine Anlagentabelle angegeben, die diesen Sortiertyp unterstützt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable:: sortable** -Methode ordnet die Zeilen in einer Tabellenansicht an. Während einige Tabellen sowohl die standardmäßige als auch die kategorisierte Sortierung in verschiedenen Sortierschlüsselspalten unterstützen, sind andere Tabellen in ihrer Unterstützung eingeschränkter. Adressbuchanbieter unterstützen die Tabellensortierung normalerweise nicht. Nachrichtenspeicher Anbieter unterstützen die Sortierung in der Regel so weit, dass Sie die Sortierreihenfolge von Ordnern beibehalten, die beim Sortieren einer vollständigen Tabelle (eine Tabelle ohne Einschränkungen) auftreten. 
  
In einigen Tabellen kann die Sortierung für eine beliebige Tabellenspalte ausgeführt werden. Andere Tabellen nicht; Spalten, die nicht in der Tabellenansicht enthalten sind, werden **** von einem sortable-Aufruf nicht beeinflusst. Einige Tabellen erfordern, dass Sortierschlüssel nur mit Spalten im aktuellen Spaltensatz der Tabelle erstellt werden. 
  
Eine Tabelle kann MAPI_E_NO_SUPPORT oder MAPI_E_TOO_COMPLEX aus der **sortable** zurückgeben, wenn ein Sortiervorgang nicht abgeschlossen werden kann. Darüber hinaus werden Speicheranbieter nicht unbedingt für die für Hierarchietabellen angegebenen Sortierreihenfolgen festgelegt. 
  
Wenn in der [SSortOrderSet](ssortorderset.md) -Struktur NULL-Spalten vorhanden sind, auf die durch den _lpSortCriteria_ -Parameter verwiesen wird, gibt die Tabelle den aktuellen Spaltensatz zurück. Die aktuelle Sortierreihenfolge kann abgerufen werden, indem die [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) -Methode der Tabelle aufgerufen wird. 
  
Alle Lesezeichen für eine Tabelle sind ungültig und sollten gelöscht werden, wenn ein **** Aufruf der sortable-Funktion erfolgt, und das BOOKMARK_CURRENT-Lesezeichen, das die aktuelle Cursorposition angibt, sollte auf den Anfang der Tabelle festgelegt werden. 
  
Wenn Sie nach einer Spalte sortieren, die eine mehrwertige Eigenschaft ohne das MVI_FLAG-Flagsatz enthält, werden die Werte der Spalte als vollständig geordnetes Tupel behandelt. Ein Vergleich zwischen zwei mehrwertigen Spalten vergleicht die Spaltenelemente in der Reihenfolge, gibt die Relation der Spalten bei der ersten Ungleichheit zurück und gibt die Gleichheit nur, wenn die verglichenen Spalten die gleichen Werte in der gleichen Reihenfolge enthalten. Wenn eine Spalte weniger Werte als die andere hat, ist die berichtete Relation die eines NULL-Werts für den anderen Wert.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **Sortier** Tabellenfunktion funktioniert synchron, es sei denn, Sie legen eine der Flags fest. Wenn Sie das TBL_BATCH-Flag festlegen **** , verschiebt sortable den Sortiervorgang, es sei denn, Sie fordern die Daten an. Wenn das TBL_ASYNC-Flag festgelegt **** ist, wird die sortable-Operation asynchron ausgeführt, und möglicherweise vor dem Abschluss des Vorgangs zurückgegeben. 
  
Rufen Sie die [IMAPITable:: Abort](imapitable-abort.md) -Methode auf, um einen asynchronen Vorgang zu beenden, der ausgeführt wird, wenn Ihre Sortierung sofort ausgeführt werden muss. Wenn **** die sortable-Funktion nicht fortgesetzt werden kann, da mindestens ein asynchroner Vorgang in der Tabelle ausgeführt wird, wird MAPI_E_BUSY zurückgegeben. 
  
Um eine optimale Leistung zu **** erzielen, rufen Sie SetColumns auf, um den Spaltensatz der Tabelle anzupassen und die Anzahl der Zeilen in der Tabelle einzuschränken, bevor Sie **sortable** aufrufen, um die Sortierung auszuführen. **** 
  
Bei jeder fehlerhaften **Sortier** Funktion wird die Sortierreihenfolge, die vor dem Fehler wirksam war, weiterhin wirksam. 
  
## <a name="see-also"></a>Siehe auch

- [IMAPITable::Abort](imapitable-abort.md)
- [IMAPITable::GetRowCount](imapitable-getrowcount.md)
- [IMAPITable::QueryColumns](imapitable-querycolumns.md)
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
- [SSortOrderSet](ssortorderset.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)

