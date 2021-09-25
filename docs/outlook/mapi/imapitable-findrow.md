---
title: IMAPITableFindRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.FindRow
api_type:
- COM
ms.assetid: 6511368c-9777-497e-9eea-cf390c04b92e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ddee908a7f44c5cb0a7b2a9371fb9b8829212f4a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600984"
---
# <a name="imapitablefindrow"></a>IMAPITable::FindRow

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sucht die nächste Zeile in einer Tabelle, die bestimmten Suchkriterien entspricht, und verschiebt den Cursor in diese Zeile.
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpRestriction_
  
> [in] Ein Zeiger auf eine [SRestriction-Struktur,](srestriction.md) die die Suchkriterien beschreibt. 
    
 _BkOrigin_
  
> [in] Ein Lesezeichen, das die Zeile identifiziert, in der **FindRow** mit der Suche beginnen soll. Eine Textmarke kann mithilfe der [IMAPITable::CreateBookmark-Methode](imapitable-createbookmark.md) erstellt werden, oder einer der folgenden vordefinierten Werte kann übergeben werden. 
    
BOOKMARK_BEGINNING 
  
> Sucht vom Anfang der Tabelle aus. 
    
BOOKMARK_CURRENT 
  
> Sucht in der Zeile in der Tabelle, in der sich der Cursor befindet. 
    
BOOKMARK_END 
  
> Sucht vom Ende der Tabelle aus. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die die Suchrichtung steuert. Das folgende Kennzeichen kann festgelegt werden:
    
DIR_BACKWARD 
  
> Sucht rückwärts aus der Zeile, die durch die Textmarke identifiziert wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Suchvorgang war erfolgreich.
    
MAPI_E_INVALID_BOOKMARK 
  
> Die Textmarke im  _BkOrigin-Parameter_ ist ungültig, weil sie entfernt wurde oder weil sie über die letzte angeforderte Zeile hinausgeht. 
    
MAPI_E_NOT_FOUND 
  
> Es wurden keine Zeilen gefunden, die mit der Einschränkung übereinstimmten.
    
MAPI_W_POSITION_CHANGED
  
> Der Aufruf war erfolgreich, aber die in dem Vorgang verwendete Textmarke wird nicht mehr in derselben Zeile wie bei der letzten Verwendung festgelegt. wenn die Textmarke nicht verwendet wurde, befindet sie sich nicht mehr an derselben Position wie beim Erstellen. Wenn diese Warnung zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden. Verwenden Sie das Makro **HR_FAILED, um** diese Warnung zu testen. Informationen zur Fehlerbehandlung finden Sie unter [Verwenden von Makros.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPITable::FindRow-Methode** sucht die erste Zeile in der Tabelle, die mit einer Reihe von Suchkriterien übereinstimmt, die in der **SRestriction-Struktur** beschrieben sind, auf die durch den  _lpRestriction-Parameter_ verwiesen wird. 
  
In der Regel sucht **FindRow** vorwärts aus der angegebenen Textmarke. Der Aufrufer kann festlegen, dass die Suche von der Textmarke rückwärts verschoben wird, indem das flag DIR_BACKWARD im  _ulFlags-Parameter_ festgelegt wird. Die Vorwärtssuche beginnt mit der aktuellen Textmarke; Die Rückwärtssuche beginnt mit der Zeile vor der Textmarke. Die Endposition der Suche liegt direkt vor der ersten Zeile, die festgestellt hat, dass die Einschränkung erfüllt wurde. 
  
Wenn die Zeile, auf die durch die Textmarke im  _BkOrigin-Parameter_ verwiesen wird, nicht mehr in der Tabelle vorhanden ist und die Tabelle keine neue Position für die Textmarke herstellen kann, gibt **FindRow** MAPI_E_INVALID_BOOKMARK zurück. Wenn die Zeile, auf die von  _BkOrigin_ verwiesen wird, nicht mehr vorhanden ist und die Tabelle eine neue Position für die Textmarke einrichten kann, gibt **FindRow** MAPI_W_POSITION_CHANGED zurück. 
  
Wenn die in  _BkOrigin_ übergebene Textmarke entweder BOOKMARK_BEGINNING oder BOOKMARK_END ist, gibt **FindRow** MAPI_E_NOT_FOUND zurück, wenn keine übereinstimmende Zeile gefunden wird. Wenn die in  _BkOrigin_ verwendete Textmarke BOOKMARK_CURRENT ist, kann **FindRow** MAPI_W_POSITION_CHANGED zurückgeben, jedoch nicht MAPI_E_INVALID_BOOKMARK, da immer eine aktuelle Cursorposition vorhanden ist. 
  
Die **Eigenschaftsspalte PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) ist für alle Tabellen erforderlich, und alle Implementierungen von **FindRow** sind erforderlich, um Aufrufe zu unterstützen, die eine Zeile basierend auf PR_INSTANCE_KEY suchen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die Art der von **FindRow** durchgeführten Präfixsuche ist nur nützlich, wenn die Suche derselben Richtung folgt wie die Tabellenorganisation. Um das erforderliche Verhalten zu erzielen, sollte die Vergleichsfunktion, die von der in der Eigenschaftseinschränkungsstruktur **übergebenen RELOP_GE** impliziert wird, dieselbe Vergleichsfunktion sein, auf der die Sortierreihenfolge der Tabelle basiert. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können **FindRow** verwenden, um den Bildlauf basierend auf vom Benutzer eingegebenen Zeichenfolgen zu unterstützen, insbesondere in Listenfeldern in Adressdialogfeldern. Bei dieser Art von Bildlauf geben Benutzer schrittweise längere Präfixe eines gewünschten Zeichenfolgenwerts ein, und Sie können in regelmäßigen Abständen einen **FindRow-Aufruf** ausgeben, um zur ersten Zeile zu springen, die dem Präfix entspricht. Welche Richtung der Cursor springt, hängt davon ab, in welche Richtung die Suche ausgeführt werden soll. 
  
Um **FindRow** verwenden zu können, muss eine Textmarke festgelegt werden. Die Zeichenfolgensuche kann von einer beliebigen Textmarke stammen, einschließlich der voreingestellten Textmarken, die die aktuelle Position sowie den Anfang und das Ende der Tabelle angeben. Wenn eine große Anzahl von Zeilen in der Tabelle vorhanden ist, kann der Suchvorgang langsam sein.
  
Verwenden Sie eine Einschränkung, um ein Zeichenfolgenpräfix für den Bildlauf wie folgt zu suchen. Übergeben Sie für die vorwärtsgerichtete Suche nach einer in aufsteigender Reihenfolge sortierten Spalte und für die Rückwärtssuche nach einer spalte, die in absteigender Reihenfolge sortiert ist, eine Eigenschaftseinschränkungsstruktur im _LpRestriction-Parameter_ mit der Beziehung **RELOP_GE** und dem entsprechenden Eigenschaftentag und Präfix mithilfe des _Formattags_ _GE-Präfix._  
  
Weitere Informationen zur Verwendung von Einschränkungsstrukturen zum Angeben eines Filters finden Sie unter ["Einschränkungen".](about-restrictions.md)
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |AdrianThreadFuncLoadTable  <br/> |MFCMAPI verwendet die **IMAPITable::FindRow-Methode,** um Zeilen zu suchen, die einer Einschränkung entsprechen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

