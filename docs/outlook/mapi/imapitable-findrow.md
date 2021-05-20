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
  
> [in] Eine Textmarke, die die Zeile identifiziert, in der **FindRow** mit der Suche beginnen soll. Eine Textmarke kann mit der [IMAPITable::CreateBookmark-Methode](imapitable-createbookmark.md) erstellt werden, oder einer der folgenden vordefinierten Werte kann übergeben werden. 
    
BOOKMARK_BEGINNING 
  
> Sucht vom Anfang der Tabelle aus. 
    
BOOKMARK_CURRENT 
  
> Sucht aus der Zeile in der Tabelle, in der sich der Cursor befindet. 
    
BOOKMARK_END 
  
> Sucht am Ende der Tabelle. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die die Richtung der Suche steuert. Das folgende Flag kann festgelegt werden:
    
DIR_BACKWARD 
  
> Sucht rückwärts aus der zeile, die durch die Textmarke identifiziert wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Findvorgang war erfolgreich.
    
MAPI_E_INVALID_BOOKMARK 
  
> Die Textmarke im  _BkOrigin-Parameter_ ist ungültig, weil sie entfernt wurde oder weil sie über die letzte angeforderte Zeile hinaus liegt. 
    
MAPI_E_NOT_FOUND 
  
> Es wurden keine Zeilen gefunden, die der Einschränkung entsprechen.
    
MAPI_W_POSITION_CHANGED
  
> Der Aufruf ist erfolgreich, aber die im Vorgang verwendete Textmarke wird nicht mehr in derselben Zeile wie bei der letzten Verwendung festgelegt. Wenn die Textmarke nicht verwendet wurde, befindet sie sich nicht mehr an derselben Position wie beim Erstellen. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro. Weitere [Informationen finden Sie unter Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::FindRow-Methode** sucht die erste Zeile in der Tabelle, um mit einer Reihe von Suchkriterien zu übereinstimmen, die in der **SRestriction-Struktur** beschrieben sind, auf die der  _lpRestriction-Parameter_ verweist. 
  
In der Regel **sucht FindRow** von der angegebenen Textmarke nach vorn. Der Aufrufer kann festlegen, dass die Suche von der Textmarke rückwärts bewegt wird, indem DIR_BACKWARD im  _ulFlags-Parameter festgelegt_ wird. Das Vorwärtssuchen beginnt mit der aktuellen Textmarke. Die Rückwärtssuche beginnt in der Zeile vor der Textmarke. Die Endposition der Suche befindet sich kurz vor der ersten Zeile, die die Einschränkung erfüllt hat. 
  
Wenn die Zeile, auf die die Textmarke im  _BkOrigin-Parameter_ verweist, nicht mehr in der Tabelle vorhanden ist und die Tabelle keine neue Position für die Textmarke einrichten kann, gibt **FindRow** MAPI_E_INVALID_BOOKMARK. Wenn die Zeile, auf die  _BkOrigin_ verweist, nicht mehr vorhanden ist und die Tabelle eine neue Position für die Textmarke einrichten kann, gibt **FindRow** MAPI_W_POSITION_CHANGED. 
  
Wenn die in  _BkOrigin_ übergebene Textmarke entweder BOOKMARK_BEGINNING oder BOOKMARK_END ist, gibt **FindRow** MAPI_E_NOT_FOUND zurück, wenn keine übereinstimmende Zeile gefunden wird. Wenn die in  _BkOrigin_ verwendete Textmarke BOOKMARK_CURRENT ist, kann **FindRow** MAPI_W_POSITION_CHANGED aber nicht MAPI_E_INVALID_BOOKMARK zurück, da immer eine aktuelle Cursorposition besteht. 
  
Die **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) -Eigenschaftsspalte ist für alle Tabellen erforderlich, und alle Implementierungen von **FindRow** sind erforderlich, um Aufrufe zu unterstützen, die eine Zeile basierend auf PR_INSTANCE_KEY. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Der Typ der Präfixsuche, die **von FindRow** ausgeführt wird, ist nur hilfreich, wenn die Suche dieselbe Richtung wie die Tabellenorganisation hat. Um das erforderliche Verhalten zu erreichen, sollte  die vergleichsfunktion, die von der RELOP_GE in der Eigenschaftseinschränkungsstruktur übergeben wird, dieselbe Vergleichsfunktion sein, auf der die Tabellensortierungsreihenfolge basiert. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können **FindRow verwenden,** um einen Bildlauf basierend auf vom Benutzer ein eingabebasierten Zeichenfolgen zu unterstützen, insbesondere in Listenfeldern innerhalb von Adressdialogfeldern. Bei dieser Art von Bildlauf geben Benutzer schrittweise längere Präfixe eines gewünschten Zeichenfolgenwerts ein, und Sie können regelmäßig einen **FindRow-Aufruf** durchführen, um zur ersten Zeile zu springen, die dem Präfix entspricht. Welche Richtung der Cursor springt, hängt davon ab, in welche Richtung die Suche ausgeführt werden soll. 
  
Um **FindRow verwenden zu** können, muss eine Textmarke festgelegt werden. Die Zeichenfolgensuche kann von beliebigen Textmarken stammen, einschließlich der vordefinierten Lesezeichen, die die aktuelle Position sowie den Anfang und das Ende der Tabelle angeben. Wenn eine große Anzahl von Zeilen in der Tabelle vorhanden ist, kann der Suchvorgang langsam sein.
  
Verwenden Sie eine Einschränkung, um ein Zeichenfolgenpräfix für den Bildlauf wie folgt zu finden. Übergeben Sie für die Vorwärtssuche für eine Spalte, die in aufsteigender Reihenfolge sortiert ist, und für die Rückwärtssuche in einer Spalte, die in absteigender Reihenfolge sortiert ist, eine Eigenschaftseinschränkungsstruktur im _lpRestriction-Parameter_ mit der Beziehung **RELOP_GE** und dem entsprechenden Eigenschaftentag und Präfix, indem Sie das _Formattag_ _GE-Präfix verwenden._  
  
Weitere Informationen zum Verwenden von Einschränkungsstrukturen zum Angeben eines Filters finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI verwendet die **IMAPITable::FindRow-Methode,** um Zeilen zu finden, die einer Einschränkung entsprechen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

