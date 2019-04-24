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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 26d6ffe66a5e7749c9d8c4e5210e9f72de808932
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328869"
---
# <a name="imapitablequeryrows"></a>IMAPITable::QueryRows

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine oder mehrere Zeilen aus einer Tabelle zurück, die an der aktuellen Cursorposition beginnen.
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a>Parameter

 _lRowCount_
  
> in Maximale Anzahl der zurückzugebenden Zeilen.
    
 _ulFlags_
  
> in Bitmaske von Flags, die Steuern, wie Zeilen zurückgegeben werden. Das folgende Flag kann festgelegt werden:
    
TBL_NOADVANCE 
  
> Verhindert das Fortschreiten des Cursors als Ergebnis des Zeilen Abrufs. Wenn das TBL_NOADVANCE-Flag festgelegt ist, zeigt der Cursor auf die erste zurückgegebene Zeile. Wenn das TBL_NOADVANCE-Flag nicht festgelegt ist, zeigt der Cursor auf die Zeile nach der letzten zurückgegebenen Zeile.
    
 _lppRows_
  
> Out Zeiger auf einen Zeiger auf eine [SRowSet](srowset.md) -Struktur, in der sich die Tabellenzeilen befinden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeilen wurden erfolgreich zurückgegeben.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Zeilenabruf Vorgang gestartet wird. Entweder sollte der ausgeführte Vorgang abgeschlossen oder beendet werden.
    
MAPI_E_INVALID_PARAMETER 
  
> Der Parameter _IRowCount_ wird auf NULL festgelegt. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable:: QueryRows** -Methode ruft eine oder mehrere Datenzeilen aus einer Tabelle ab. Der Wert des _IRowCount_ -Parameters wirkt sich auf den Anfangspunkt des Abrufs aus. Wenn _IRowCount_ positiv ist, werden Zeilen nach vorn gelesen, beginnend an der aktuellen Position. Wenn _IRowCount_ negativ ist, wird der Startpunkt von **QueryRows** zurückgesetzt, indem die angegebene Anzahl von Zeilen rückwärts bewegt wird. Nach dem Zurücksetzen des Cursors werden die Zeilen in der Forward-Reihenfolge gelesen. 
  
Das **Crows** -Element in der [SRowSet](srowset.md) -Struktur, auf die durch den _lppRows_ -Parameter verwiesen wird, gibt die Anzahl der zurückgegebenen Zeilen an. Wenn null Zeilen zurückgegeben werden: 
  
- Der Cursor war bereits am Anfang der Tabelle positioniert, und der Wert von _IRowCount_ ist negativ. Oder 
    
- Der Cursor wurde bereits am Ende der Tabelle positioniert, und der Wert von _IRowCount_ ist positiv. 
    
Die Anzahl der Spalten und ihre Reihenfolge ist für jede Zeile identisch. Wenn eine Eigenschaft nicht für eine Zeile vorhanden ist oder beim Lesen einer Eigenschaft ein Fehler auftritt, enthält die **SPropValue** -Struktur für die-Eigenschaft in der Zeile die folgenden Werte: 
  
- PT_ERROR für den Eigenschaftentyp im **ulPropTag** -Element. 
    
- MAPI_E_NOT_FOUND für den **Wert** Member. 
    
Der für die [SPropValue](spropvalue.md) -Strukturen im Zeilensatz, auf den der _lppRows_ -Parameter zeigt, verwendete Arbeitsspeicher muss für jede Zeile separat reserviert und freigegeben werden. Verwenden Sie [mapifreebufferfreigegeben](mapifreebuffer.md) , um die Eigenschaftswert Strukturen freizugeben und den Zeilensatz freizugeben. Wenn ein Aufruf von **QueryRows** NULL zurückgibt, aber den Anfang oder das Ende der Tabelle angibt, muss nur die **SRowSet** -Struktur selbst freigegeben werden. Weitere Informationen zum reservieren und Freigeben von Arbeitsspeicher in einer **SRowSet** -Struktur finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
Die zurückgegebenen Zeilen und die Reihenfolge, in der Sie zurückgegeben werden, hängen davon ab, ob erfolgreiche Aufrufe an [IMAPITable:: Restrict](imapitable-restrict.md) und [IMAPITable:: sortable](imapitable-sorttable.md)vorgenommen wurden. Filter Zeilen aus der Ansicht **einschränken** , sodass **QueryRows** nur die Zeilen zurückgibt, die den in der Einschränkung angegebenen Kriterien entsprechen. **Sortable** legt eine Standard-oder kategorisierte Sortierreihenfolge fest, die sich auf die Reihenfolge der von **QueryRows**zurückgegebenen Zeilen auswirkt. Die zurückgegebenen Zeilen befinden sich in der in der [SSortOrderSet](ssortorderset.md) -Struktur angegebenen **** Reihenfolge, die an sortable übergeben wird.
  
Die für jede Zeile zurückgegebenen Spalten und die Reihenfolge, in der Sie zurückgegeben werden, hängen davon ab, ob ein erfolgreicher Aufruf an [IMAPITable::](imapitable-setcolumns.md)SetColumns erfolgt ist oder nicht. **** SetColumns richtet eine Spaltengruppe ein, die die Eigenschaften angibt, die in Spalten in der Tabelle enthalten sein sollen, und die Reihenfolge, in der Sie eingeschlossen werden sollen. Wenn ein **** SetColumns-Aufruf ausgeführt wurde, stimmen die Spalten in jeder Zeile und die Reihenfolge dieser Spalten mit dem im Aufruf angegebenen Spaltensatz überein. Wenn kein **** SetColumns-Aufruf ausgeführt wurde, gibt die Tabelle den Standardspaltensatz zurück. 
  
Wenn keiner dieser Aufrufe vorgenommen wurde, gibt **QueryRows** alle Zeilen in der Tabelle zurück. Jede Zeile enthält den standardmäßigen Spaltensatz in der Standardreihenfolge. 
  
Wenn der in einem Aufruf von [IMAPITable::](imapitable-setcolumns.md) SetColumns eingerichtete Spaltensatz Spalten enthält, die auf PR_NULL festgelegt sind, enthält das [SPropValue](spropvalue.md) -Array innerhalb des in _lppRows_ zurückgegebenen Rowsets leere Slots. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können einem Anrufer gestatten, eine nicht unterstützte Spalte anzufordern, die in den Spaltensatz eingeschlossen werden soll. Wenn dies der Fall ist, platzieren Sie PT_ERROR im Eigenschafts Teil des Property-Tags und MAPI_E_NOT_FOUND im Eigenschaftswert für die nicht unterstützte Spalte. 
  
Behandeln Sie die Zeilenanzahl als Anforderung anstatt als Anforderung. Sie können an einer beliebigen Stelle von null Zeilen zurückkehren, wenn es keine Zeilen in der Richtung der Abfrage gibt, um die angeforderte Nummer. 
  
Gibt nur die Zeilen zurück, die dem Benutzer angezeigt werden, wenn Zeilen aus einer kategorisierten Tabellenansicht angefordert werden, sodass der Aufrufer gültige Annahmen über den Datenbereich treffen und zusätzliche Arbeit vermeiden kann. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

In der Regel werden Sie so viele Zeilen wie im Parameter _lRowCount_ angegeben haben. Wenn jedoch Speicher-oder Implementierungs Grenzwerte ein Problem sind oder wenn der Vorgang vorzeitig den Anfang oder das Ende der Tabelle erreicht, gibt **QueryRows** weniger Zeilen zurück als angefordert. 
  
Wenn **QUERYROWS** MAPI_E_BUSY zurückgibt, rufen Sie die [IMAPITable:: WaitForCompletion](imapitable-waitforcompletion.md) -Methode auf, und wiederholen Sie den Aufruf von **QueryRows** , wenn der asynchrone Vorgang abgeschlossen ist. 
  
Beachten Sie beim Aufrufen von **QueryRows**, dass der Zeitpunkt der asynchronen Benachrichtigungen potenziell dazu führen kann, dass der aus **QueryRows** zurückgegebene Zeilensatz die zugrunde liegenden Daten nicht genau darstellt. Beispielsweise bewirkt ein Aufruf von **QueryRows** in der Inhaltstabelle eines Ordners nach dem Löschen einer Nachricht, jedoch vor dem Empfang der entsprechenden Benachrichtigung, dass die gelöschte Zeile im Zeilensatz zurückgegeben wird. Warten Sie immer, bis eine Benachrichtigung eingeht, bevor Sie die Benutzeransicht der Daten aktualisieren. 
  
Weitere Informationen zum Abrufen von Zeilen aus Tabellen finden Sie unter [Abrufen von Daten aus Tabellenzeilen](retrieving-data-from-table-rows.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI verwendet die **IMAPITable:: QueryRows** -Methode zum Abrufen von Zeilen in der Tabelle, um Sie in die Ansicht zu laden.  <br/> |
   
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

