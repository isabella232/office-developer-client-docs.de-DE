---
title: IMAPITableSeekRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.SeekRow
api_type:
- COM
ms.assetid: 93ac63ae-f254-45e1-a9b1-347d69d2ed9f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0b54979a9cd61985de58f1d11ddf741f435e8a60
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630586"
---
# <a name="imapitableseekrow"></a>IMAPITable::SeekRow

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verschiebt den Cursor an eine bestimmte Position in der Tabelle.
  
```cpp
HRESULT SeekRow(
BOOKMARK bkOrigin,
LONG lRowCount,
LONG FAR * lplRowsSought
);
```

## <a name="parameters"></a>Parameter

 _bkOrigin_
  
> [in] Das Lesezeichen, das die Startposition für den Suchvorgang identifiziert. Eine Textmarke kann mithilfe der [IMAPITable::CreateBookmark-Methode](imapitable-createbookmark.md) erstellt werden, oder einer der folgenden vordefinierten Werte kann übergeben werden. 
    
BOOKMARK_BEGINNING 
  
> Startet den Suchvorgang am Anfang der Tabelle. 
    
BOOKMARK_CURRENT 
  
> Startet den Suchvorgang aus der Zeile in der Tabelle, in der sich der Cursor befindet. 
    
BOOKMARK_END 
  
> Startet den Suchvorgang am Ende der Tabelle. 
    
 _lRowCount_
  
> [in] Die signierte Anzahl der Zeilen, die verschoben werden sollen, beginnend mit der vom  _bkOrigin-Parameter_ identifizierten Textmarke. 
    
 _lplRowsS über_
  
> [out] Wenn  _lRowCount_ ein gültiger Zeiger für die Eingabe ist, zeigt  _lplRowsSung_ auf die Anzahl der Zeilen, die im Suchvorgang verarbeitet wurden, deren Vorzeichen die Suchrichtung angibt, vorwärts oder rückwärts. Wenn  _"lRowCount"_ negativ ist, ist  _"lplRowsS emerge"_ negativ. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Suchvorgang war erfolgreich.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Vorgang zur Zeilensuche gestartet wird. Entweder sollte der laufende Vorgang abgeschlossen werden können, oder er sollte beendet werden.
    
MAPI_E_INVALID_BOOKMARK 
  
> Die im  _bkOrigin-Parameter_ angegebene Textmarke ist ungültig, weil sie entfernt wurde oder weil sie über der letzten angeforderten Zeile liegt. 
    
MAPI_W_POSITION_CHANGED 
  
> Der Aufruf war erfolgreich, aber die im  _bkOrigin-Parameter_ angegebene Textmarke wird nicht mehr in derselben Zeile wie bei der letzten Verwendung festgelegt. Wenn die Textmarke nicht verwendet wurde, befindet sie sich nicht mehr an derselben Position wie bei der Erstellung. Wenn diese Warnung zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden. Verwenden Sie das Makro **HR_FAILED, um** diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwenden von Makros für die Fehlerbehandlung.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable::SeekRow-Methode** richtet eine neue BOOKMARK_CURRENT Position für den Cursor ein. Der  _lRowCount-Parameter_ gibt die Anzahl der Zeilen an, die der Cursor verschiebt, und die Bewegungsrichtung. 
  
Wenn sich die resultierende Position außerhalb der letzten Zeile der Tabelle befindet, wird der Cursor hinter der letzten Zeile positioniert. Wenn sich die resultierende Position vor der ersten Zeile der Tabelle befindet, wird der Cursor am Anfang der ersten Zeile positioniert. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn die Zeile, auf die von  _bkOrigin_ verwiesen wird, nicht mehr in der Tabelle vorhanden ist und Sie keine neue Position für die Textmarke festlegen können, geben Sie MAPI_E_INVALID_BOOKMARK zurück. Wenn die Zeile, auf die von  _bkOrigin_ verwiesen wird, nicht mehr vorhanden ist und Sie eine neue Position für die Textmarke festlegen können, geben Sie MAPI_W_POSITION_CHANGED zurück. 
  
Eine Textmarke, die auf eine Zeile zeigt, die aus der Tabellenansicht reduziert ist, kann weiterhin verwendet werden. Wenn der Aufrufer versucht, den Cursor in eine solche Textmarke zu verschieben, verschieben Sie den Cursor in die nächste sichtbare Zeile, und geben Sie MAPI_W_POSITION_CHANGED zurück. 
  
Sie können Lesezeichen für Positionen verschieben, die zum Zeitpunkt der Verwendung oder zum Zeitpunkt des Reduzierens der Zeile aus der Ansicht reduziert wurden. Wenn eine Textmarke zu dem Zeitpunkt verschoben wird, zu dem die Zeile reduziert wird, behalten Sie ein Bit in der Textmarke bei, das angibt, ob die Textmarke seit der letzten Verwendung oder, wenn sie nie verwendet wurde, seit der Erstellung verschoben wurde.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Rückwärtsbewegung für **SeekRow** anzugeben, übergeben Sie einen negativen Wert in  _lRowCount_. Um an den Anfang der Tabelle zu suchen, übergeben Sie null in  _lRowCount_ und den Wert BOOKMARK_BEGINNING in  _bkOrigin_. 
  
Wenn die Tabelle viele Zeilen enthält, kann der **SeekRow-Vorgang** langsam sein. Die Leistung kann auch beeinträchtigt werden, wenn sie erfordert, dass eine Zeilenanzahl im Inhalt des  _lplRowsS über_ den Parameter zurückgegeben wird. 
  
 **SeekRow** gibt die Anzahl der Zeilen zurück, die tatsächlich durchsucht wurden( positiv oder negativ) in der Variablen, auf die durch  _lRowCount_ verwiesen wird. Im normalen Vorgang sollte derselbe Wert für  _lplRowsS übergibt_ werden, es sei  _denn,_ die Suche hat den Anfang oder das Ende der Tabelle erreicht. 
  
Legen Sie  _lRowCount_ nicht auf eine Zahl fest, die größer als 50 ist. Verwenden Sie die [IMAPITable::SeekRowApprox-Methode,](imapitable-seekrowapprox.md) um eine größere Anzahl von Zeilen zu durchsuchen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProcessor.cpp  <br/> |CMAPIProcessor::P apiessMailboxTable  <br/> |MFCMAPI verwendet die **IMAPITable::SeekRow-Methode,** um den Anfang der Tabelle vor der Verarbeitung zu suchen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

