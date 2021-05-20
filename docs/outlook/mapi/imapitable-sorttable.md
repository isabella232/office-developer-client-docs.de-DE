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
  
Die **IMAPITable::SortTable-Methode** sortiert die Zeilen der Tabelle in Abhängigkeit von Sortierkriterien. 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

_lpSortCriteria_
  
> [in] Zeiger auf eine [SSortOrderSet-Struktur,](ssortorderset.md) die die anzuwendende Sortierkriterien enthält. Das Übergeben einer **SSortOrderSet-Struktur,** die null Spalten enthält, bedeutet, dass die Tabelle nicht in einer bestimmten Reihenfolge sortiert werden muss. 
    
_ulFlags_
  
> [in] Bitmaske von Flags, die das Timing des **IMAPITable::SortTable-Vorgangs** steuert. Die folgenden Kennzeichen können festgelegt werden: 
    
TBL_ASYNC 
  
> Startet den Vorgang asynchron und gibt zurück, bevor der Vorgang abgeschlossen ist.
    
TBL_BATCH 
  
> Der Abschluss der Sortierung wird so lange auf die Daten in der Tabelle verf?en.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Sortiervorgang war erfolgreich.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Sortiervorgang gestartet wird. Der ausgeführte Vorgang sollte entweder abgeschlossen oder beendet werden.
    
MAPI_E_NO_SUPPORT 
  
> Die Tabelle unterstützt den angeforderten Sortiertyp nicht.
    
MAPI_E_TOO_COMPLEX 
  
> Die Tabelle kann den Vorgang nicht ausführen, da die bestimmten Sortierkriterien, auf die der  _lpSortCriteria-Parameter_ verweist, zu komplex sind. **SortTable** kann MAPI_E_TOO_COMPLEX unter den folgenden Bedingungen zurückgeben. 
    
   - Für eine Eigenschaftenspalte, die von der Implementierung nicht sortiert werden kann, wird ein Sortiervorgang angefordert.
    
   - Die Implementierung unterstützt die im **ulOrder-Element** der **SSortOrderSet-Struktur** angeforderte Sortierreihenfolge nicht. 
    
   - Die Anzahl der spalten, die sortiert werden sollen, wie im **cSorts-Element** in **SSortOrderSet** angegeben, ist größer, als die Implementierung verarbeiten kann.
    
   - Ein Sortiervorgang wird angefordert, wie durch ein Eigenschaftentag in **SSortOrderSet** angegeben, basierend auf einer Eigenschaft, die sich nicht im verfügbaren oder aktiven Satz befindet, und die Implementierung unterstützt das Sortieren von Eigenschaften, die nicht im verfügbaren Satz enthalten sind, nicht.
    
   - Eine Eigenschaft wird in einem Sortierreihenfolgensatz mehrmals angegeben, wie von mehreren Instanzen desselben Eigenschaftstags angegeben, und die Implementierung kann einen solchen Sortiervorgang nicht ausführen.
    
   - Ein Sortiervorgang basierend auf mehrwertigen Eigenschaftenspalten wird mithilfe von MVI_FLAG angefordert, und die Implementierung unterstützt die Sortierung nach mehrwertigen Eigenschaften nicht. 
    
   - Ein Eigenschaftstag für eine Eigenschaft in **SSortOrderSet** gibt eine Eigenschaft oder einen Typ an, die von der Implementierung nicht unterstützt wird. 
    
   - Ein anderer Sortiervorgang, der die Tabelle von der **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))-Eigenschaft vorwärts durchgeht, wird nur für eine Anlagentabelle angegeben, die diese Art von Sortierung unterstützt.
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::SortTable-Methode** ordnet die Zeilen in einer Tabellenansicht an. Während einige Tabellen sowohl die standard- als auch die kategorisierte Sortierung für verschiedene Sortierschlüsselspalten unterstützen, sind andere Tabellen in ihrer Unterstützung eingeschränkter. Adressbuchanbieter unterstützen normalerweise keine Tabellensortierung. Nachrichtenspeicheranbieter unterstützen die Sortierung in der Regel so weit, dass sie die Sortierreihenfolge von Ordnern behalten, die sich ergibt, wenn eine vollständige Tabelle (eine Tabelle ohne Einschränkungen) sortiert wird. 
  
In einigen Tabellen kann die Sortierung in jeder Tabellenspalte durchgeführt werden. Andere Tabellen nicht; Spalten, die nicht in der Tabellenansicht enthalten sind, sind von einem **SortTable-Aufruf nicht** betroffen. Einige Tabellen erfordern, dass Sortierschlüssel nur mit Spalten im aktuellen Spaltensatz der Tabelle erstellt werden. 
  
Eine Tabelle kann entweder MAPI_E_NO_SUPPORT oder MAPI_E_TOO_COMPLEX **SortTable** zurückgeben, wenn sie keinen Sortiervorgang abschließen kann. Darüber hinaus ist es nicht garantiert, dass Speicheranbieter den für Hierarchietabellen angegebenen Sortierreihenfolgensatz würdigen. 
  
Wenn die [SSortOrderSet-Struktur](ssortorderset.md) null Spalten enthält, auf die der  _lpSortCriteria-Parameter_ verweist, gibt die Tabelle den aktuellen Spaltensatz zurück. Die aktuelle Sortierreihenfolge kann durch Aufrufen der [IMAPITable::QuerySortOrder-Methode der Tabelle abgerufen](imapitable-querysortorder.md) werden. 
  
Alle Lesezeichen für eine Tabelle sind ungültig und sollten gelöscht werden, wenn ein Aufruf von **SortTable** erfolgt, und die BOOKMARK_CURRENT-Textmarke, die die aktuelle Cursorposition angibt, sollte auf den Anfang der Tabelle festgelegt werden. 
  
Wenn Sie nach einer Spalte sortieren, die eine mehrwertige Eigenschaft ohne das flag set MVI_FLAG enthält, werden die Werte der Spalte als vollständig sortiertes Tupel behandelt. Bei einem Vergleich von zwei mehrwertigen Spalten werden die Spaltenelemente in der Reihenfolge verglichen. Dabei wird das Verhältnis der Spalten bei der ersten Ungleichheit angegeben, und es wird nur Gleichheit zurückgegeben, wenn die zu vergleichenden Spalten dieselben Werte in derselben Reihenfolge enthalten. Wenn eine Spalte weniger Werte als die andere hat, ist die gemeldete Beziehung die eines Nullwerts zum anderen Wert.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

**SortTable** funktioniert synchron, es sei denn, Sie legen eines der Flags ein. Wenn Sie das TBL_BATCH festlegen, verschiebt **SortTable** den Sortiervorgang, es sei denn, Sie fordern die Daten an. Wenn das TBL_ASYNC festgelegt ist, wird **SortTable** asynchron betrieben und möglicherweise vor Abschluss des Vorgangs zurückgeben. 
  
Rufen Sie [die IMAPITable::Abort-Methode](imapitable-abort.md) auf, um einen asynchronen Vorgang zu beenden, wenn die Sortierung sofort durchgeführt werden muss. Wenn **SortTable** nicht fortgesetzt werden kann, da mindestens ein asynchroner Vorgang in der Tabelle ausgeführt wird, wird MAPI_E_BUSY. 
  
Um eine optimale Leistung zu erzielen, rufen Sie **SetColumns** auf, um den Spaltensatz der Tabelle anzupassen, und **beschränken** Sie, um die Anzahl der Zeilen in der Tabelle zu beschränken, bevor Sie **SortTable** aufrufen, um die Sortierung durchzuführen. 
  
Wenn **SortTable** fehlschlägt, ist die Sortierreihenfolge, die vor dem Fehler wirksam war, weiterhin wirksam. 
  
## <a name="see-also"></a>Siehe auch

- [IMAPITable::Abort](imapitable-abort.md)
- [IMAPITable::GetRowCount](imapitable-getrowcount.md)
- [IMAPITable::QueryColumns](imapitable-querycolumns.md)
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
- [SSortOrderSet](ssortorderset.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)

