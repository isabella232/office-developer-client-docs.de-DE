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
ms.openlocfilehash: a6659f64f6e8d2e3dc61819b2263efe672cdd15c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792488"
---
# <a name="imapitablequeryrows"></a>IMAPITable::QueryRows

  
  
**Betrifft**: Outlook 
  
Gibt eine oder mehrere Zeilen aus einer Tabelle, beginnend bei der aktuellen Cursorposition zurück.
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a>Parameter

 _lRowCount_
  
> [in] Maximale Anzahl der Zeilen, die zurückgegeben werden soll.
    
 _ulFlags_
  
> [in] Bitmaske der Flags, die steuern, wie Zeilen zurückgegeben werden. Das folgende Flag kann festgelegt werden:
    
TBL_NOADVANCE 
  
> Verhindert, dass den Cursor als Ergebnis des Zeile Abrufs vorwärts verschoben. Wenn das Flag TBL_NOADVANCE festgelegt ist, zurückgegeben, die der Cursor verweist auf die erste Zeile. Wenn das Flag TBL_NOADVANCE nicht festgelegt ist, zeigt der Cursor auf die Zeile nach der letzten Zeile zurückgegeben.
    
 _lppRows_
  
> [out] Zeiger auf einen Zeiger auf eine [SRowSet](srowset.md) -Struktur, die die Tabellenzeilen. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Zeilen wurden erfolgreich zurückgegeben.
    
MAPI_E_BUSY 
  
> Ein anderer Vorgang wird ausgeführt, die verhindert, den Vorgang Zeile nicht gestartet dass. Entweder dürfen der Vorgang in Arbeit abgeschlossen oder angehalten werden sollte.
    
MAPI_E_INVALID_PARAMETER 
  
> Der Parameter _IRowCount_ wird auf 0 (null) festgelegt. 
    
## <a name="remarks"></a>Bemerkungen

**Die QueryRows** Ruft eine oder mehrere Zeilen mit Daten aus einer Tabelle ab. Der Wert des Parameters _IRowCount_ wirkt sich auf der Ausgangspunkt für das Abrufen. _IRowCount_ positiv darf, werden vorwärts, ab der aktuellen Position Zeilen gelesen. Wenn _IRowCount_ negativ ist, setzt **QueryRows** Startpunkt durch Verschieben rückwärts die angegebene Anzahl von Zeilen zurück. Nach dem Zurücksetzen von des Cursors werden die Zeilen in der Reihenfolge gelesen. 
  
Der **cRows** Member in der [SRowSet](srowset.md) -Struktur, die auf das durch den Parameter _LppRows_ gibt die Anzahl von Zeilen zurückgegeben. Wenn keine Zeilen zurückgegeben werden: 
  
- Der Cursor wurde bereits am Anfang der Tabelle positioniert, und der Wert der _IRowCount_ negativ ist. \Endash oder \endash 
    
- Der Cursor wurde bereits am Ende der Tabelle positioniert, und der Wert der _IRowCount_ positiv ist. 
    
Die Anzahl der Spalten und ihrer Reihenfolge wird für jede Zeile identisch. Wenn eine Eigenschaft für eine Zeile nicht vorhanden, oder es wird ein Fehler beim Lesen einer Eigenschaft, enthält die **SPropValue** -Struktur für die Eigenschaft in der Zeile die folgenden Werte: 
  
- PT_ERROR für den Eigenschaftentyp im **UlPropTag** -Member. 
    
- MAPI_E_NOT_FOUND für **das Element** . 
    
Für die [SPropValue](spropvalue.md) Strukturen in der Zeile auf das durch den Parameter _LppRows_ verwendeter Arbeitsspeicher muss separat belegt und für jede Zeile freigegeben werden. Verwenden Sie [MAPIFreeBuffer](mapifreebuffer.md) , um die Eigenschaft Wert Strukturen frei, und legen Sie die Zeile frei, um. Wenn Sie ein Anruf an **QueryRows** gibt 0 (null) zurück, jedoch muss, der angibt, der Anfang oder das Ende der Tabelle nur die **SRowSet** Struktur selbst freigegeben werden. Weitere Informationen zum Zuordnen und Freigeben von Arbeitsspeicher in eine **SRowSet** -Struktur finden Sie unter [Verwalten von Arbeitsspeicher für ADRLIST und SRowSet Strukturen](managing-memory-for-adrlist-and-srowset-structures.md).
  
Die Zeilen, die zurückgegeben werden und die Reihenfolge, in der sie zurückgegeben werden, hängt davon ab, unabhängig davon, ob erfolgreiche Anrufe an die [Methode IMAPITable:: Restrict](imapitable-restrict.md) und [SortTable](imapitable-sorttable.md)vorgenommen wurden. **Restrict** Filter Zeilen aus der Ansicht verursacht **QueryRows** , um nur die Zeilen zurück, die in der Einschränkung angegebenen Kriterien entsprechen. **SortTable** richtet einen Standard oder kategorisiert Sortierreihenfolge, beeinflussen die Abfolge von Zeilen von **QueryRows**zurückgegeben. Die zurückgegebenen Zeilen werden in der Reihenfolge, in der **SortTable**übergeben [SSortOrderSet](ssortorderset.md) Struktur angegeben.
  
Die Spalten für jede Zeile zurückgegeben und hängen von der Reihenfolge, in dem sie zurückgegeben werden, unabhängig davon, ob ein erfolgreicher Aufruf an [IMAPITable::SetColumns](imapitable-setcolumns.md)vorgenommen wurde. **SetColumns** richtet einen Spaltensatz angeben die Eigenschaften, die Spalten in der Tabelle und die Reihenfolge, in der sie enthalten sein sollen, berücksichtigt werden. Wenn ein Anruf **SetColumns** vorgenommen wurden, übereinstimmen bestimmten Spalten in jeder Zeile und die Reihenfolge der Spalten die Spalte festlegen in der Anruf angegeben. Falls kein Aufruf **SetColumns** vorgenommen wurden, gibt die Tabelle die standardspaltensammlung zurück. 
  
Wenn keine dieser Anrufe vorgenommen wurde, gibt **QueryRows** alle Zeilen in der Tabelle zurück. Jede Zeile enthält die Standardspalte in Standardreihenfolge festgelegt. 
  
Wenn die Spalte in einem Aufruf von [IMAPITable::SetColumns](imapitable-setcolumns.md) hergestellt Spalten auf PR_NULL gesetzt enthält, wird das Array [SPropValue](spropvalue.md) innerhalb der Zeile, die in _LppRows_ zurückgegeben leere Steckplätze enthalten. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können einen Anrufer zum Anfordern von nicht unterstützten Spalte, die in der Spalte Gruppe eingeschlossen werden. In diesem Fall wird die Eigenschaft Typ Teil der Eigenschafts-Tag und MAPI_E_NOT_FOUND im-Eigenschaftenwert für die Spalte nicht unterstützte versehen Sie PT_ERROR. 
  
Die Anzahl der Zeilen einer Anforderung, sondern als Voraussetzung zu behandeln. Sie können an einer beliebigen Stelle aus keine Zeilen zurückgeben, wenn keine Zeilen in die Richtung der Abfrage, auf die angeforderte Anzahl vorhanden sind. 
  
Nur die Zeilen, die dem Benutzer angezeigt wird, wenn Zeilen aus einer kategorisierten Tabellenansicht angefordert werden sodass Aufrufer gültige Annahmen bezüglich des Umfangs der Daten und zusätzliche Arbeit vermeiden zurück. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

In der Regel werden Sie am Ende beliebig viele Zeilen, die Sie in der _lRowCount_ -Parameter angegeben haben. Jedoch zurück Wenn Speicher oder-Implementierung Grenzwerten handelt es sich ein Problem oder der Vorgang der Anfang oder das Ende der Tabelle vorzeitig erreicht, **QueryRows** weniger Zeilen als angefordert. 
  
Wenn **QueryRows** MAPI_E_BUSY zurückgibt, wird rufen Sie die [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) -Methode auf, und wiederholen Sie den Anruf an **QueryRows** , wenn der asynchrone Vorgang abgeschlossen ist. 
  
Beim Aufruf von **QueryRows**, achten Sie darauf, dass der Zeitpunkt des asynchronen Benachrichtigungen das Rowset fest potenziell dazu führen, dass Sie ähnliche aus **QueryRows** erhalten haben, nicht für die zugrunde liegenden Daten genau darstellen. Legen Sie beispielsweise ein Aufruf von **QueryRows** , einen Ordner Inhalt Tabelle Folgendes, dass das Löschen einer Nachricht, aber vor dem Empfang des die entsprechende Benachrichtigung verursacht die gelöschte Zeile in der Zeile zurückgegeben werden soll. Warten Sie immer eine Benachrichtigung vor dem Aktualisieren der Ansicht der Daten des Benutzers eingehen. 
  
Weitere Informationen zum Abrufen von Zeilen aus Tabellen finden Sie unter [Abrufen von Daten aus Tabellenzeilen](retrieving-data-from-table-rows.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI (engl.) verwendet **die QueryRows** abzurufenden Zeilen in der Tabelle, in der Ansicht zu laden.  <br/> |
   
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

