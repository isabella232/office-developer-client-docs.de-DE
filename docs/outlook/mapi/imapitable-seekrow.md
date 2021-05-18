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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fbc990a8c962883aa07987b200d1d2fd55434f93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413045"
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
  
> [in] Die Textmarke, die die Startposition für den Suchvorgang identifiziert. Eine Textmarke kann mit der [IMAPITable::CreateBookmark-Methode](imapitable-createbookmark.md) erstellt werden, oder einer der folgenden vordefinierten Werte kann übergeben werden. 
    
BOOKMARK_BEGINNING 
  
> Startet den Suchvorgang am Anfang der Tabelle. 
    
BOOKMARK_CURRENT 
  
> Startet den Suchvorgang aus der Zeile in der Tabelle, in der sich der Cursor befindet. 
    
BOOKMARK_END 
  
> Startet den Suchvorgang am Ende der Tabelle. 
    
 _lRowCount_
  
> [in] Die signierte Anzahl der zu verschiebende Zeilen, beginnend mit der textmarke, die durch den  _bkOrigin-Parameter identifiziert_ wird. 
    
 _lplRowsSought_
  
> [out] Wenn  _lRowCount_ ein gültiger Zeiger für die Eingabe ist, zeigt  _lplRowsSought_ auf die Anzahl der Zeilen, die im Suchvorgang verarbeitet wurden, deren Vorzeichen die Richtung der Suche angibt, vorwärts oder rückwärts. Wenn  _lRowCount_ negativ ist, ist  _lplRowsSought_ negativ. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Suchvorgang war erfolgreich.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Zeilensuchenvorgang gestartet wird. Der ausgeführte Vorgang sollte entweder abgeschlossen oder beendet werden.
    
MAPI_E_INVALID_BOOKMARK 
  
> Die im  _bkOrigin-Parameter_ angegebene Textmarke ist ungültig, weil sie entfernt wurde oder weil sie über die letzte angeforderte Zeile hinaus liegt. 
    
MAPI_W_POSITION_CHANGED 
  
> Der Aufruf ist erfolgreich, aber die im  _bkOrigin-Parameter_ angegebene Textmarke wird nicht mehr in derselben Zeile wie bei der letzten Verwendung festgelegt. Wenn die Textmarke nicht verwendet wurde, befindet sie sich nicht mehr an derselben Position wie beim Erstellen. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro. Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::SeekRow-Methode** richtet eine neue BOOKMARK_CURRENT position für den Cursor ein. Der  _lRowCount-Parameter_ gibt die Anzahl der Zeilen an, die der Cursor bewegt, und die Bewegungsrichtung. 
  
Wenn die resultierende Position über der letzten Zeile der Tabelle liegt, wird der Cursor hinter der letzten Zeile positioniert. Wenn sich die resultierende Position vor der ersten Zeile der Tabelle befindet, wird der Cursor am Anfang der ersten Zeile positioniert. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn die zeile, auf die  _von bkOrigin_ verwiesen wird, nicht mehr in der Tabelle vorhanden ist und Sie keine neue Position für die Textmarke einrichten können, geben Sie MAPI_E_INVALID_BOOKMARK. Wenn die Zeile, auf die  _von bkOrigin_ verwiesen wird, nicht mehr vorhanden ist und Sie eine neue Position für die Textmarke einrichten können, geben Sie MAPI_W_POSITION_CHANGED. 
  
Eine Textmarke, die auf eine Zeile zeigt, die aus der Tabellenansicht reduziert ist, kann weiterhin verwendet werden. Wenn der Aufrufer versucht, den Cursor zu einer solchen Textmarke zu verschieben, verschieben Sie den Cursor zur nächsten sichtbaren Zeile, und geben Sie MAPI_W_POSITION_CHANGED. 
  
Sie können Lesezeichen für Positionen verschieben, die zum Zeitpunkt der Verwendung oder zum Zeitpunkt des Reduzierens der Zeile aus der Ansicht reduziert wurden. Wenn eine Textmarke zu dem Zeitpunkt verschoben wird, zu dem die Zeile reduziert wird, behalten Sie ein Bit in der Textmarke bei, das angibt, ob die Textmarke seit der letzten Verwendung verschoben wurde oder, falls sie nie verwendet wurde, seit ihrer Erstellung.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Rückwärtsbewegung für **SeekRow** anzugeben, übergeben Sie einen negativen Wert in  _lRowCount_. Um an den Anfang der Tabelle zu suchen, übergeben Sie null in  _lRowCount_ und den Wert BOOKMARK_BEGINNING in  _bkOrigin_. 
  
Wenn die Tabelle viele Zeilen enthält, kann **der SeekRow-Vorgang** langsam sein. Die Leistung kann auch beeinträchtigt werden, wenn eine Zeilenanzahl im Inhalt des  _lplRowsSought-Parameters zurückgegeben werden_ muss. 
  
 **SeekRow** gibt die Anzahl der Zeilen zurück, die tatsächlich in der variablen, auf die von  _lRowCount_ verwiesen wird, positiv oder negativ durchsucht wurden. Im normalen Vorgang sollte derselbe Wert für  _lplRowsSought_ wie für  _lRowCount_ übergeben werden, es sei denn, die Suche hat den Anfang oder das Ende der Tabelle erreicht. 
  
Legen Sie  _lRowCount nicht_ auf eine Zahl größer als 50. Verwenden Sie zum Durchsuchen einer größeren Anzahl von Zeilen die [IMAPITable::SeekRowApprox-Methode.](imapitable-seekrowapprox.md) 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProcessor.cpp  <br/> |CMAPIProcessor::P rocessMailboxTable  <br/> |MFCMAPI verwendet die **IMAPITable::SeekRow-Methode,** um den Anfang der Tabelle vor der Verarbeitung zu finden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

