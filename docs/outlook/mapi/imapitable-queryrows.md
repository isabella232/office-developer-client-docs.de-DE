---
title: IMAPITableQueryRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.QueryRows
api_type:
- COM
ms.assetid: f26384f1-467e-4343-92b3-0425da9d2123
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7f21172c00f1b5130de657e7018d05f04d16afe5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625350"
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
  
> [in] Maximale Anzahl der zurückzugebenden Zeilen.
    
 _ulFlags_
  
> [in] Bitmaske von Flags, die steuern, wie Zeilen zurückgegeben werden. Das folgende Kennzeichen kann festgelegt werden:
    
TBL_NOADVANCE 
  
> Verhindert, dass der Cursor als Ergebnis des Zeilenabrufs anhält. Wenn das flag TBL_NOADVANCE festgelegt ist, zeigt der Cursor auf die erste zurückgegebene Zeile. Wenn das flag TBL_NOADVANCE nicht festgelegt ist, zeigt der Cursor auf die Zeile, die auf die letzte zurückgegebene Zeile folgt.
    
 _lppRows_
  
> [out] Zeiger auf einen Zeiger auf eine [SRowSet-Struktur,](srowset.md) die die Tabellenzeilen enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeilen wurden erfolgreich zurückgegeben.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Zeilenabrufvorgang gestartet wird. Entweder sollte der laufende Vorgang abgeschlossen werden können, oder er sollte beendet werden.
    
MAPI_E_INVALID_PARAMETER 
  
> Der  _IRowCount-Parameter_ ist auf Null festgelegt. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable::QueryRows-Methode** ruft eine oder mehrere Datenzeilen aus einer Tabelle ab. Der Wert des  _IRowCount-Parameters_ wirkt sich auf den Startpunkt für den Abruf aus. Wenn  _IRowCount_ positiv ist, werden Zeilen vorwärts gelesen, beginnend an der aktuellen Position. Wenn  _IRowCount_ negativ ist, setzt **QueryRows** den Anfangspunkt zurück, indem die angegebene Anzahl von Zeilen rückwärts verschoben wird. Nachdem der Cursor zurückgesetzt wurde, werden zeilenweise gelesen. 
  
Das **cRows-Element** in der [SRowSet-Struktur,](srowset.md) auf das der  _lppRows-Parameter_ verweist, gibt die Anzahl der zurückgegebenen Zeilen an. Wenn null Zeilen zurückgegeben werden: 
  
- Der Cursor wurde bereits am Anfang der Tabelle positioniert, und der Wert von  _IRowCount_ ist negativ. -Or- 
    
- Der Cursor wurde bereits am Ende der Tabelle positioniert, und der Wert von  _IRowCount_ ist positiv. 
    
Die Anzahl der Spalten und deren Reihenfolge ist für jede Zeile identisch. Wenn eine Eigenschaft für eine Zeile nicht vorhanden ist oder beim Lesen einer Eigenschaft ein Fehler auftritt, enthält die **SPropValue-Struktur** für die Eigenschaft in der Zeile die folgenden Werte: 
  
- PT_ERROR für den Eigenschaftstyp im **ulPropTag-Element.** 
    
- MAPI_E_NOT_FOUND für das **Value-Element.** 
    
Speicher, der für die [SPropValue-Strukturen](spropvalue.md) in dem Zeilensatz verwendet wird, auf den der  _lppRows-Parameter verweist,_ muss für jede Zeile separat zugeordnet und freigegeben werden. Verwenden Sie [MAPIFreeBuffer,](mapifreebuffer.md) um die Eigenschaftswertstrukturen freizugeben und den Zeilensatz freizugeben. Wenn ein Aufruf von **QueryRows** jedoch Null zurückgibt, was den Anfang oder das Ende der Tabelle angibt, muss nur die **SRowSet-Struktur** selbst freigegeben werden. Weitere Informationen zum Zuordnen und Freigeben von Speicher in einer **SRowSet-Struktur** finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
Die zurückgegebenen Zeilen und die Reihenfolge, in der sie zurückgegeben werden, hängen davon ab, ob erfolgreiche Aufrufe an [IMAPITable::Restrict](imapitable-restrict.md) und [IMAPITable::SortTable](imapitable-sorttable.md)vorgenommen wurden. **Filterzeilen** aus der Ansicht einschränken, wodurch **QueryRows** nur die Zeilen zurückgibt, die den in der Einschränkung angegebenen Kriterien entsprechen. **SortTable** richtet eine standard- oder kategorisierte Sortierreihenfolge ein, die sich auf die von **QueryRows** zurückgegebene Zeilenfolge auswirkt. Die zurückgegebenen Zeilen befinden sich in der Reihenfolge, die in der [SSortOrderSet-Struktur](ssortorderset.md) angegeben ist, die an SortTable übergeben **wird.**
  
Die spalten für jede Zeile zurückgegeben und die Reihenfolge, in der sie zurückgegeben werden, hängt davon ab, ob ein erfolgreicher Aufruf an [IMAPITable::SetColumns](imapitable-setcolumns.md)vorgenommen wurde oder nicht. **SetColumns** richtet einen Spaltensatz ein, der die Eigenschaften angibt, die in Spalten in der Tabelle enthalten sein sollen, und die Reihenfolge, in der sie eingeschlossen werden sollen. Wenn ein **SetColumns-Aufruf** ausgeführt wurde, stimmen die einzelnen Spalten in jeder Zeile und die Reihenfolge dieser Spalten mit dem im Aufruf angegebenen Spaltensatz überein. Wenn kein **SetColumns-Aufruf** ausgeführt wurde, gibt die Tabelle den Standardspaltensatz zurück. 
  
Wenn keiner dieser Aufrufe ausgeführt wurde, gibt **QueryRows** alle Zeilen in der Tabelle zurück. Jede Zeile enthält die Standardspalte, die in der Standardreihenfolge festgelegt ist. 
  
Wenn der in einem Aufruf von [IMAPITable::SetColumns](imapitable-setcolumns.md) erstellte Spaltensatz Spalten enthält, die auf PR_NULL festgelegt sind, enthält das [SPropValue-Array](spropvalue.md) innerhalb des in  _lppRows zurückgegebenen_ Zeilensatzes leere Steckplätze. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können zulassen, dass ein Aufrufer anfordert, dass eine nicht unterstützte Spalte in den Spaltensatz einbezogen wird. Platzieren Sie in diesem Fall PT_ERROR im Eigenschaftentypteil des Eigenschaftentags und MAPI_E_NOT_FOUND im Eigenschaftswert für die nicht unterstützte Spalte. 
  
Behandeln Sie die Zeilenanzahl nicht als Anforderung, sondern als Anforderung. Sie können an einer beliebigen Stelle von null Zeilen, wenn keine Zeilen in der Richtung der Abfrage vorhanden sind, zur angeforderten Zahl zurückkehren. 
  
Gibt nur die Zeilen zurück, die dem Benutzer angezeigt werden, wenn Zeilen aus einer kategorisierten Tabellenansicht angefordert werden, sodass der Aufrufer gültige Annahmen über den Umfang der Daten treffen und zusätzliche Arbeit vermeiden kann. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

In der Regel erhalten Sie so viele Zeilen, wie Sie im  _Parameter "lRowCount"_ angegeben haben. Wenn Speicher- oder Implementierungsgrenzwerte jedoch ein Problem darstellen oder wenn der Vorgang den Anfang oder das Ende der Tabelle vorzeitig erreicht, gibt **QueryRows** weniger Zeilen als angefordert zurück. 
  
Wenn **QueryRows** MAPI_E_BUSY zurückgibt, rufen Sie die [IMAPITable::WaitForCompletion-Methode](imapitable-waitforcompletion.md) auf, und wiederholen Sie den Aufruf von **QueryRows,** wenn der asynchrone Vorgang abgeschlossen ist. 
  
Beachten Sie beim Aufrufen von **QueryRows,** dass der Zeitpunkt asynchroner Benachrichtigungen dazu führen kann, dass der Zeilensatz, den Sie von **QueryRows** abrufen, die zugrunde liegenden Daten nicht genau darstellt. Beispielsweise führt ein Aufruf von **QueryRows** zum Inhaltsverzeichnis eines Ordners nach dem Löschen einer Nachricht, aber vor dem Empfang der entsprechenden Benachrichtigung dazu, dass die gelöschte Zeile im Zeilensatz zurückgegeben wird. Warten Sie immer, bis eine Benachrichtigung eintrifft, bevor Sie die Ansicht der Daten des Benutzers aktualisieren. 
  
Weitere Informationen zum Abrufen von Zeilen aus Tabellen finden Sie unter [Abrufen von Daten aus Tabellenzeilen](retrieving-data-from-table-rows.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |AdrianThreadFuncLoadTable  <br/> |MFCMAPI verwendet die **IMAPITable::QueryRows-Methode,** um Zeilen in der Tabelle abzurufen, die in die Ansicht geladen werden sollen.  <br/> |
   
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

