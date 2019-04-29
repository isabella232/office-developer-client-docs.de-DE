---
title: IMAPITableFindRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FindRow
api_type:
- COM
ms.assetid: 6511368c-9777-497e-9eea-cf390c04b92e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a5364af229721d101f38d2f054f528169b48c09e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429572"
---
# <a name="imapitablefindrow"></a>IMAPITable::FindRow

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sucht die nächste Zeile in einer Tabelle, die bestimmten Suchkriterien entspricht, und verschiebt den Cursor zu dieser Zeile.
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpRestriction_
  
> in Ein Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die die Suchkriterien beschreibt. 
    
 _BkOrigin_
  
> in Eine Textmarke, die die Zeile identifiziert, in der **FindRow** Ihre Suche beginnen soll. Eine Textmarke kann mit der [IMAPITable:: CreateBookMark](imapitable-createbookmark.md) -Methode oder einem der folgenden vordefinierten Werte erstellt werden. 
    
BOOKMARK_BEGINNING 
  
> Sucht vom Anfang der Tabelle aus. 
    
BOOKMARK_CURRENT 
  
> Sucht aus der Zeile in der Tabelle, in der sich der Cursor befindet. 
    
BOOKMARK_END 
  
> Sucht am Ende der Tabelle. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Richtung der Suche steuert. Das folgende Flag kann festgelegt werden:
    
DIR_BACKWARD 
  
> Sucht aus der durch die Textmarke identifizierten Zeile rückwärts.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Suchvorgang war erfolgreich.
    
MAPI_E_INVALID_BOOKMARK 
  
> Die Textmarke im _BkOrigin_ -Parameter ist ungültig, da Sie entfernt wurde oder über die letzte angeforderte Zeile hinausgeht. 
    
MAPI_E_NOT_FOUND 
  
> Es wurden keine Zeilen gefunden, die mit der Einschränkung übereinstimmen.
    
MAPI_W_POSITION_CHANGED
  
> Der Aufruf wurde erfolgreich ausgeführt, aber die im Vorgang verwendete Textmarke wird nicht mehr in derselben Zeile festgelegt wie bei der letzten Verwendung; Wenn die Textmarke nicht verwendet wurde, befindet Sie sich nicht mehr in derselben Position wie bei ihrer Erstellung. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro. Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable:: FindRow** -Methode sucht die erste Zeile in der Tabelle, die einer Reihe von Suchkriterien entspricht, die in der **SRestriction** -Struktur beschrieben ist, auf die durch den _lpRestriction_ -Parameter verwiesen wird. 
  
In der Regel sucht **FindRow** nach vorn aus der angegebenen Textmarke. Der Anrufer kann festlegen, dass die Suche rückwärts aus der Textmarke verschoben wird, indem das DIR_BACKWARD-Flag im _ulFlags_ -Parameter festgelegt wird. Die Vorwärtssuche beginnt mit der aktuellen Textmarke; die Rückwärtssuche beginnt von der Zeile vor der Textmarke. Die Endposition der Suche ist unmittelbar vor der ersten gefundenen Zeile, die die Einschränkung erfüllt hat. 
  
Wenn die Zeile, auf die durch die Textmarke im _BkOrigin_ -Parameter verwiesen wird, in der Tabelle nicht mehr vorhanden ist und die Tabelle keine neue Position für die Textmarke festlegen kann, gibt **FindRow** MAPI_E_INVALID_BOOKMARK zurück. Wenn die Zeile, auf die durch _BkOrigin_ verwiesen wird, nicht mehr vorhanden ist und die Tabelle eine neue Position für die Textmarke festlegen kann, gibt **FindRow** MAPI_W_POSITION_CHANGED zurück. 
  
Wenn die in _BkOrigin_ übergebene Textmarke entweder BOOKMARK_BEGINNING oder BOOKMARK_END ist, gibt **FindRow** MAPI_E_NOT_FOUND zurück, wenn keine übereinstimmende Zeile gefunden wird. Wenn die in _BkOrigin_ verwendete Textmarke BOOKMARK_CURRENT ist, kann **FindRow** MAPI_W_POSITION_CHANGED zurückgeben, aber nicht MAPI_E_INVALID_BOOKMARK, da immer eine aktuelle Cursor Position vorliegt. 
  
Die **PR_INSTANCE_KEY** ([pidtaginstancekey (](pidtaginstancekey-canonical-property.md))-Eigenschaftsspalte ist für alle Tabellen erforderlich, und alle Implementierungen von **FindRow** sind erforderlich, um Aufrufe zu unterstützen, die eine Zeile auf der Grundlage von PR_INSTANCE_KEY suchen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Der Typ der durch **FindRow** durchgeführten Präfixsuche ist nur nützlich, wenn die Suche dieselbe Richtung hat wie die Tabellenorganisation. Um das erforderliche Verhalten zu erreichen, sollte die Vergleichsfunktion, die von der **RELOP_GE** , die in der Eigenschafts Einschränkungs Struktur übergeben wird, die gleiche Vergleichsfunktion sein, auf der die Tabellen Sortierreihenfolge basiert. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können **FindRow** verwenden, um den Bildlauf basierend auf vom Benutzer eingegebenen Zeichenfolgen zu unterstützen, insbesondere in Listenfeldern in Adress Dialogfeldern. Bei diesem Bildlauftyp geben Benutzer progressiv längere Präfixe eines gewünschten Zeichenfolgenwerts ein, und Sie können in regelmäßigen Abständen einen **FindRow** -Aufruf ausgeben, um zur ersten Zeile zu wechseln, die mit dem Präfix übereinstimmt. Welche Richtung der Cursor springt, hängt davon ab, in welcher Richtung die Suche ausgeführt wird. 
  
Um **FindRow**zu verwenden, muss eine Textmarke festgelegt werden. Die Zeichenfolgensuche kann von einer beliebigen Textmarke stammen, einschließlich der vordefinierten Lesezeichen, die die aktuelle Position und den Anfang und das Ende der Tabelle angeben. Wenn eine hohe Anzahl von Zeilen in der Tabelle vorhanden ist, kann der Suchvorgang langsam sein.
  
Verwenden Sie eine Einschränkung, um nach einem Zeichenfolgen Präfix zum Scrollen wie folgt zu suchen. Zum Weiterleiten der Suche in einer Spalte in aufsteigender Reihenfolge und zur Rückwärtssuche für eine in absteigender Reihenfolge sortierte Spalte übergeben Sie eine Eigenschafts Einschränkungs Struktur im _lpRestriction_ -Parameter mit der Relation **RELOP_GE** und dem entsprechenden Property-Tag und Prefix, wobei das Format- _Tag_ **ge** - _Präfix_verwendet wird. 
  
Weitere Informationen zur Verwendung von Einschränkungs Strukturen zum Angeben eines Filters finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI verwendet die **IMAPITable:: FindRow** -Methode, um Zeilen zu finden, die mit einer Einschränkung übereinstimmen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

