---
title: IMAPITableSeekRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRow
api_type:
- COM
ms.assetid: 93ac63ae-f254-45e1-a9b1-347d69d2ed9f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fbc990a8c962883aa07987b200d1d2fd55434f93
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328826"
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
  
> in Die Textmarke, die die Anfangsposition für den Seek-Vorgang identifiziert. Eine Textmarke kann mit der [IMAPITable:: CreateBookMark](imapitable-createbookmark.md) -Methode oder einem der folgenden vordefinierten Werte erstellt werden. 
    
BOOKMARK_BEGINNING 
  
> Startet den Seek-Vorgang vom Anfang der Tabelle aus. 
    
BOOKMARK_CURRENT 
  
> Startet den Seek-Vorgang von der Zeile in der Tabelle, in der sich der Cursor befindet. 
    
BOOKMARK_END 
  
> Startet den Seek-Vorgang am Ende der Tabelle. 
    
 _lRowCount_
  
> in Die signierte Anzahl der zu verschiebende Zeilen, beginnend mit der durch den _bkOrigin_ -Parameter angegebenen Textmarke. 
    
 _lplRowsSought_
  
> Out Wenn _lRowCount_ ein gültiger Zeiger auf der Eingabe ist, zeigt _lplRowsSought_ auf die Anzahl der Zeilen, die in der Seek-Operation verarbeitet wurden, deren Vorzeichen die Richtung der Suche angibt, vorwärts oder rückwärts. Wenn _lRowCount_ negativ ist, ist _lplRowsSought_ negativ. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Seek-Vorgang war erfolgreich.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Zeilen Suchvorgang gestartet wird. Entweder sollte der ausgeführte Vorgang abgeschlossen oder beendet werden.
    
MAPI_E_INVALID_BOOKMARK 
  
> Die im _bkOrigin_ -Parameter angegebene Textmarke ist ungültig, da Sie entfernt wurde oder über die letzte angeforderte Zeile hinausgeht. 
    
MAPI_W_POSITION_CHANGED 
  
> Der Aufruf wurde erfolgreich ausgeführt, aber die im _bkOrigin_ -Parameter angegebene Textmarke wird nicht mehr in derselben Zeile festgelegt wie bei der letzten Verwendung. Wenn die Textmarke nicht verwendet wurde, befindet Sie sich nicht mehr in der gleichen Position wie bei ihrer Erstellung. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro. Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable:: SeekRow** -Methode richtet eine neue BOOKMARK_CURRENT-Position für den Cursor ein. Der Parameter _lRowCount_ gibt die Anzahl der Zeilen an, die der Cursor verschiebt, und die Bewegungsrichtung. 
  
Wenn sich die resultierende Position jenseits der letzten Zeile der Tabelle befindet, wird der Cursor nach der letzten Zeile positioniert. Wenn sich die resultierende Position vor der ersten Zeile der Tabelle befindet, wird der Cursor am Anfang der ersten Zeile positioniert. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn die Zeile, auf die durch _bkOrigin_ verwiesen wird, in der Tabelle nicht mehr vorhanden ist und Sie keine neue Position für die Textmarke festlegen können, geben Sie MAPI_E_INVALID_BOOKMARK zurück. Wenn die Zeile, auf die durch _bkOrigin_ verwiesen wird, nicht mehr vorhanden ist und Sie eine neue Position für die Textmarke festlegen können, geben Sie MAPI_W_POSITION_CHANGED zurück. 
  
Eine Textmarke, die auf eine Zeile zeigt, die aus der Tabellenansicht ausgeblendet ist, kann weiterhin verwendet werden. Wenn der Aufrufer versucht, den Cursor auf eine solche Textmarke zu verschieben, bewegen Sie den Cursor zur nächsten sichtbaren Zeile, und geben Sie MAPI_W_POSITION_CHANGED. 
  
Sie können Lesezeichen für Positionen verschieben, die aus der Ansicht ausgeblendet wurden, entweder zum Zeitpunkt der Verwendung oder zum Zeitpunkt, zu dem die Zeile reduziert wird. Wenn eine Textmarke zu dem Zeitpunkt verschoben wird, zu dem die Zeile reduziert wird, behalten Sie ein Bit in der Textmarke, die angibt, ob die Textmarke seit der letzten Verwendung verschoben wurde, oder, falls Sie noch nie verwendet wurde, seit ihrer Erstellung.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Rückwärtsbewegung für **SeekRow**anzugeben, geben Sie einen negativen Wert in _lRowCount_an. Um am Anfang der Tabelle zu suchen, überschreiten Sie NULL in _lRowCount_ und den Wert BOOKMARK_BEGINNING in _bkOrigin_. 
  
Wenn in der Tabelle viele Zeilen vorhanden sind, kann der **SeekRow** -Vorgang langsam sein. Die Leistung kann auch beeinträchtigt werden, wenn eine Zeilenanzahl im Inhalt des _lplRowsSought_ -Parameters zurückgegeben werden muss. 
  
 **SeekRow** gibt die Anzahl der Zeilen zurück, die tatsächlich durchsucht wurden, positiv oder negativ in der Variablen, auf die durch _lRowCount_verwiesen wird. Im gewöhnlichen Vorgang sollte es den gleichen Wert für _lplRowsSought_ zurückgeben, wie er für _lRowCount_übergeben wird, es sei denn, die Suche hat den Anfang oder das Ende der Tabelle erreicht. 
  
Legen Sie _lRowCount_ nicht auf eine Zahl größer als 50. Verwenden Sie die [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) -Methode, um eine größere Anzahl von Zeilen zu suchen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProcessor. cpp  <br/> |CMAPIProcessor::P rocessMailboxTable  <br/> |MFCMAPI verwendet die **IMAPITable:: SeekRow** -Methode, um den Anfang der Tabelle vor der Verarbeitung zu suchen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

