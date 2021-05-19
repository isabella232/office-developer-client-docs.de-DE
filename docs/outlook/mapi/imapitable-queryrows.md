---
title: IMAPITableQueryRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryRows
api_type:
- COM
ms.assetid: f26384f1-467e-4343-92b3-0425da9d2123
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 26d6ffe66a5e7749c9d8c4e5210e9f72de808932
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416293"
---
# <a name="imapitablequeryrows"></a>IMAPITable::QueryRows

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine oder mehrere Zeilen aus einer Tabelle zurück, beginnend an der aktuellen Cursorposition.
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a>Parameter

 _lRowCount_
  
> [in] Maximale Anzahl von Zeilen, die zurückgegeben werden sollen.
    
 _ulFlags_
  
> [in] Bitmaske von Flags, die steuern, wie Zeilen zurückgegeben werden. Das folgende Flag kann festgelegt werden:
    
TBL_NOADVANCE 
  
> Verhindert, dass der Cursor als Ergebnis des Zeilenabrufs fortschreitet. Wenn das TBL_NOADVANCE festgelegt ist, zeigt der Cursor auf die erste zurückgegebene Zeile. Wenn das TBL_NOADVANCE nicht festgelegt ist, zeigt der Cursor auf die Zeile nach der letzten zurückgegebenen Zeile.
    
 _lppRows_
  
> [out] Zeiger auf einen Zeiger auf eine [SRowSet-Struktur,](srowset.md) die die Tabellenzeilen enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeilen wurden erfolgreich zurückgegeben.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Zeilenabrufvorgang gestartet wird. Der ausgeführte Vorgang sollte entweder abgeschlossen oder beendet werden.
    
MAPI_E_INVALID_PARAMETER 
  
> Der  _Parameter IRowCount_ ist auf Null festgelegt. 
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::QueryRows-Methode** ruft eine oder mehrere Datenzeilen aus einer Tabelle ab. Der Wert des  _IRowCount-Parameters_ wirkt sich auf den Ausgangspunkt für den Abruf aus. Wenn  _IRowCount_ positiv ist, werden Zeilen in Vorwärtsrichtung gelesen, beginnend an der aktuellen Position. Wenn  _IRowCount_ negativ ist, **setzt QueryRows** den Ausgangspunkt zurück, indem die angegebene Anzahl von Zeilen rückwärts bewegt wird. Nachdem der Cursor zurückgesetzt wurde, werden Zeilen in der Vorwärtsreihenfolge gelesen. 
  
Das **cRows-Element** in der [SRowSet-Struktur,](srowset.md) auf das der  _lppRows-Parameter_ verweist, gibt die Anzahl der zurückgegebenen Zeilen an. Wenn null Zeilen zurückgegeben werden: 
  
- Der Cursor wurde bereits am Anfang der Tabelle positioniert, und der Wert von  _IRowCount ist_ negativ. -Or- 
    
- Der Cursor wurde bereits am Ende der Tabelle positioniert, und der Wert von  _IRowCount ist_ positiv. 
    
Die Anzahl der Spalten und deren Reihenfolge ist für jede Zeile identisch. Wenn für eine Zeile keine Eigenschaft vorhanden ist oder ein Fehler beim Lesen einer Eigenschaft auftritt, enthält die **SPropValue-Struktur** für die Eigenschaft in der Zeile die folgenden Werte: 
  
- PT_ERROR für den Eigenschaftentyp im **ulPropTag-Element.** 
    
- MAPI_E_NOT_FOUND für das **Value-Element.** 
    
Für die [SPropValue-Strukturen](spropvalue.md) im Zeilensatz, auf den der  _lppRows-Parameter_ verweist, verwendeter Arbeitsspeicher muss für jede Zeile separat zugewiesen und frei werden. Verwenden [Sie MAPIFreeBuffer,](mapifreebuffer.md) um die Eigenschaftenwertstrukturen frei zu machen und den Zeilensatz frei zu machen. Wenn ein Aufruf von **QueryRows** jedoch Null zurückgibt und den Anfang oder das Ende der Tabelle angibt, muss nur die **SRowSet-Struktur** selbst frei. Weitere Informationen zum Zuordnen und Freispeichern von Arbeitsspeicher in einer **SRowSet-Struktur** finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
Die zurückgegebenen Zeilen und die Reihenfolge, in der sie zurückgegeben werden, hängen davon ab, ob erfolgreiche Aufrufe an [IMAPITable::Restrict](imapitable-restrict.md) und [IMAPITable::SortTable](imapitable-sorttable.md)ausgeführt wurden. **Beschränken** Sie Zeilen aus der Ansicht, sodass **QueryRows** nur die Zeilen zurück gibt, die den in der Einschränkung angegebenen Kriterien entsprechen. **SortTable** richtet eine standard- oder kategorisierte Sortierreihenfolge ein, die sich auf die Reihenfolge der von QueryRows zurückgegebenen **Zeilen ausdingt.** Die zurückgegebenen Zeilen befinden sich in der in der [SSortOrderSet-Struktur](ssortorderset.md) angegebenen Reihenfolge, die an **SortTable übergeben wird.**
  
Die für jede Zeile zurückgegebenen Spalten und die Reihenfolge, in der sie zurückgegeben werden, hängen davon ab, ob ein erfolgreicher Aufruf an [IMAPITable::SetColumns erfolgt ist.](imapitable-setcolumns.md) **SetColumns** richtet einen Spaltensatz ein und gibt die Eigenschaften an, die in Spalten in der Tabelle enthalten sein sollen, und die Reihenfolge, in der sie eingeschlossen werden sollen. Wenn ein **SetColumns-Aufruf** ausgeführt wurde, entsprechen die einzelnen Spalten in jeder Zeile und die Reihenfolge dieser Spalten der im Aufruf angegebenen Spaltensatz. Wenn kein **SetColumns-Aufruf** erfolgt ist, gibt die Tabelle den Standardspaltensatz zurück. 
  
Wenn keiner dieser Aufrufe ausgeführt wurde, gibt **QueryRows** alle Zeilen in der Tabelle zurück. Jede Zeile enthält die Standardspalte, die in der Standardreihenfolge festgelegt ist. 
  
Wenn der spaltensatz, der in einem Aufruf von [IMAPITable::SetColumns](imapitable-setcolumns.md) eingerichtet wurde, Spalten enthält, die auf PR_NULL festgelegt sind, enthält das [SPropValue-Array](spropvalue.md) innerhalb des in  _lppRows_ zurückgegebenen Zeilensatz leere Slots. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können zulassen, dass ein Aufrufer eine nicht unterstützte Spalte in den Spaltensatz einrist. Platzieren Sie in diesem Fall PT_ERROR im Eigenschaftentypteil des Eigenschaftstags und MAPI_E_NOT_FOUND eigenschaftswert für die nicht unterstützte Spalte. 
  
Behandeln Sie die Zeilenanzahl als Anforderung und nicht als Anforderung. Sie können eine beliebige Stelle von Nullzeilen zurückgeben, wenn keine Zeilen in Der Richtung der Abfrage vorhanden sind, zur angeforderten Nummer. 
  
Gibt nur die Zeilen zurück, die dem Benutzer angezeigt werden, wenn Zeilen aus einer kategorisierten Tabellenansicht angefordert werden, sodass der Aufrufer gültige Annahmen über den Umfang der Daten treffen und zusätzliche Arbeit vermeiden kann. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

In der Regel erhalten Sie so viele Zeilen wie im _lRowCount-Parameter angegeben._ Wenn speicher- oder implementierungsbeschränkungen jedoch ein Problem sind oder wenn der Vorgang den Anfang oder das Ende der Tabelle vorzeitig erreicht, gibt **QueryRows** weniger Zeilen zurück als angefordert. 
  
Wenn **QueryRows** MAPI_E_BUSY zurückgibt, rufen Sie die [IMAPITable::WaitForCompletion-Methode](imapitable-waitforcompletion.md) auf, und wiederholen Sie den Aufruf von **QueryRows,** wenn der asynchrone Vorgang abgeschlossen ist. 
  
Beachten Sie beim Aufrufen von **QueryRows,** dass das Timing asynchroner Benachrichtigungen dazu führen kann, dass der Zeilensatz, den Sie von **QueryRows** erhalten, die zugrunde liegenden Daten nicht genau repräsentiert. Beispielsweise wird durch einen Aufruf von **QueryRows** an die Inhaltstabelle eines Ordners nach dem Löschen einer Nachricht, aber vor dem Eingang der entsprechenden Benachrichtigung die gelöschte Zeile im Zeilensatz zurückgegeben. Warten Sie immer, bis eine Benachrichtigung eintrifft, bevor Sie die Ansicht der Daten des Benutzers aktualisieren. 
  
Weitere Informationen zum Abrufen von Zeilen aus Tabellen finden Sie unter [Abrufen von Daten aus Tabellenzeilen](retrieving-data-from-table-rows.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI verwendet die **IMAPITable::QueryRows-Methode,** um Zeilen in der Tabelle abzurufen, die in die Ansicht geladen werden sollen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ADRENTRY](adrentry.md)
  
[FreeProws](freeprows.md)
  
[HrQueryAllRows](hrqueryallrows.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SRow](srow.md)
  
[SRowSet](srowset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

