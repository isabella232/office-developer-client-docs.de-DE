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
ms.openlocfilehash: 143ca03a5e98d638d29394f5c0803e349ab4de25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792471"
---
# <a name="imapitableseekrow"></a>IMAPITable::SeekRow

  
  
**Betrifft**: Outlook 
  
Verschiebt den Cursor an eine bestimmte Position in der Tabelle an.
  
```cpp
HRESULT SeekRow(
BOOKMARK bkOrigin,
LONG lRowCount,
LONG FAR * lplRowsSought
);
```

## <a name="parameters"></a>Parameter

 _bkOrigin_
  
> [in] Die Textmarke, die die Anfangsposition für den Vorgang Seek identifiziert. Eine Textmarke kann mithilfe der [IMAPITable::CreateBookmark](imapitable-createbookmark.md) -Methode erstellt werden, oder eine der folgenden vordefinierten Werte übergeben werden kann. 
    
BOOKMARK_BEGINNING 
  
> Startet den Suchvorgang am Anfang der Tabelle. 
    
BOOKMARK_CURRENT 
  
> Startet den Suchvorgang aus der Zeile in der Tabelle, in dem sich der Cursor befindet. 
    
BOOKMARK_END 
  
> Startet den Suchvorgang vom Ende der Tabelle an. 
    
 _lRowCount_
  
> [in] Die Anzahl der Anzahl der zu verschiebenden Zeilen mit Vorzeichen, durch den Parameter _BkOrigin_ identifiziert die Textmarke ab. 
    
 _lplRowsSought_
  
> [out] Ist _lRowCount_ ein gültiger Zeiger auf input _LplRowsSought_ verweist auf die Anzahl der Zeilen, die in den Suchvorgang verarbeitet wurden, gibt die Zeichen, von denen die Richtung der Suche, vorwärts oder rückwärts. Wenn _lRowCount_ negativ ist, klicken Sie dann ist _LplRowsSought_ negativ. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Suchvorgang erfolgreich war.
    
MAPI_E_BUSY 
  
> Ein anderer Vorgang wird ausgeführt, die den Vorgang Zeile Ansprechpartner bei einem Neustart verhindert. Entweder dürfen der Vorgang in Arbeit abgeschlossen oder angehalten werden sollte.
    
MAPI_E_INVALID_BOOKMARK 
  
> Die Textmarke im _BkOrigin_ -Parameter angegebene ist ungültig oder da sie entfernt wurde, da sie nach der letzten Zeile angefordert wird. 
    
MAPI_W_POSITION_CHANGED 
  
> Der Aufruf war erfolgreich, aber im _BkOrigin_ -Parameter angegebene Textmarke wird nicht mehr in der gleichen Zeile festgelegt, wie bei der es zuletzt verwendet wurde. Wenn die Textmarke nicht verwendet wurden, ist es nicht mehr an derselben Position wie bei der es erstellt wurde. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet. Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::SeekRow** -Methode stellt eine neue BOOKMARK_CURRENT Position für den Cursor her. Der Parameter _lRowCount_ gibt die Anzahl der Zeilen, die der Cursor bewegt wird und die Richtung der Bewegung an. 
  
Wenn die resultierende Position nach der letzten Zeile der Tabelle ist, wird der Cursor nach der letzten Zeile positioniert. Wenn die resultierende Position vor der ersten Zeile der Tabelle ist, wird der Cursor am Anfang der ersten Zeile positioniert. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn die Zeile, die auf den _BkOrigin_ in der Tabelle nicht mehr vorhanden ist und Sie keine neue Position für das Lesezeichen, geben Sie MAPI_E_INVALID_BOOKMARK zurück. Wenn die Zeile, die auf den _BkOrigin_ nicht mehr vorhanden ist und Sie können eine neue Position für das Lesezeichen einrichten, geben Sie MAPI_W_POSITION_CHANGED zurück. 
  
Eine Textmarke verweisen auf eine Zeile, die aus der Tabellenansicht reduziert ist kann immer noch verwendet werden. Wenn der Aufrufer versucht, den Cursor in solchen ein Lesezeichen zu verschieben, bewegen Sie den Cursor in die nächste Zeile sichtbar und zurückzugeben Sie MAPI_W_POSITION_CHANGED. 
  
Sie können verschieben Lesezeichen für Positionen reduziert aus der Ansicht, die zum Zeitpunkt der Verwendung oder zur Zeit, die die Zeile reduziert ist. Wenn eine Textmarke Zeitpunkt verschoben wird, die die Zeile reduziert ist, lassen Sie etwas in die Textmarke, die angibt, ob die Textmarke wurde seit der letzten Verwendung verschoben oder, hat es nie, seit seiner Erstellung verwendet wurde.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Ebene nach hinten Verschiebung für **SeekRow**angegeben haben, übergeben Sie einen negativen Wert _lRowCount_. Um an den Anfang der Tabelle zu suchen, übergeben Sie NULL in _lRowCount_ und der Wert BOOKMARK_BEGINNING in _BkOrigin_. 
  
Wenn viele Zeilen in der Tabelle vorhanden sind, kann der Vorgang **SeekRow** langsam sein. Leistung kann auch beeinflusst werden, wenn Sie benötigen eine Zeilenanzahl in den Inhalt des Parameters _LplRowsSought_ zurückgegeben werden soll. 
  
 **SeekRow** gibt die Anzahl der Zeilen tatsächlich über gesucht, positiven oder negativen, in der Variablen, die auf den _lRowCount_zurück. Im normalen Betrieb sollten sie den gleichen Wert für _LplRowsSought_ zurückgeben, wie für _lRowCount_, übergeben, sofern die Suche der Anfang oder das Ende der Tabelle erreicht. 
  
Legen Sie nicht _lRowCount_ auf eine Zahl größer als 50. Um eine größere Anzahl von Zeilen zu suchen, verwenden Sie [die SeekRowApprox](imapitable-seekrowapprox.md) . 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProcessor.cpp  <br/> |CMAPIProcessor::ProcessMailboxTable  <br/> |MFCMAPI (engl.) verwendet die **IMAPITable::SeekRow** -Methode, um den Anfang der Tabelle vor der Verarbeitung zu suchen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable](imapitable-findrow.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

