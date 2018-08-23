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
ms.openlocfilehash: 2a50a5f536e337e5ca37e61f17d4dfd40aa9c51e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565333"
---
# <a name="imapitablefindrow"></a>IMAPITable::FindRow

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Findet die nächste Zeile in einer Tabelle, die bestimmte Suchkriterien entspricht, und verschiebt den Cursor auf diese Zeile.
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpRestriction_
  
> [in] Ein Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die den Suchkriterien beschreibt. 
    
 _BkOrigin_
  
> [in] Eine Textmarke, identifiziert die Zeile, in dem **FindRow** die Suche beginnen soll. Eine Textmarke kann mithilfe der [IMAPITable::CreateBookmark](imapitable-createbookmark.md) -Methode erstellt werden, oder eine der folgenden vordefinierten Werte übergeben werden kann. 
    
BOOKMARK_BEGINNING 
  
> Sucht vom Beginn der Tabelle. 
    
BOOKMARK_CURRENT 
  
> Sucht aus der Zeile in der Tabelle, in dem sich der Cursor befindet. 
    
BOOKMARK_END 
  
> Sucht vom Ende der Tabelle. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die die Richtung der Suche steuert. Das folgende Flag kann festgelegt werden:
    
DIR_BACKWARD 
  
> Sucht rückwärts aus der Zeile, die durch die Textmarke identifiziert.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Suchvorgang erfolgreich war.
    
MAPI_E_INVALID_BOOKMARK 
  
> Die Textmarke im _BkOrigin_ -Parameter ist ungültig oder, da es entfernt wurde, da sie nach der letzten Zeile angefordert wird. 
    
MAPI_E_NOT_FOUND 
  
> Es wurden keine Zeilen gefunden, die mit die Einschränkung übereinstimmen.
    
MAPI_W_POSITION_CHANGED
  
> Der Aufruf war erfolgreich, aber die Textmarke, die in den Vorgang verwendet wird nicht mehr in der gleichen Zeile als bei der letzten Verwendung festgelegt; Wenn die Textmarke nicht verwendet wurden, ist es nicht mehr in derselben Position wie bei der es erstellt wurde. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet. Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen. Finden Sie unter [Verwendung von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPITable** -Methode sucht nach der ersten Zeile in der Tabelle auf eine Gruppe von in der auf das durch den Parameter _LpRestriction_ **SRestriction** -Struktur beschriebenen Suchkriterien erfüllen. 
  
In der Regel sucht **FindRow** weiterleiten aus der angegebenen Textmarke. Der Aufrufer kann die Suche von der Bookmark rückwärts, indem das DIR_BACKWARD Flag im _UlFlags_ -Parameter festlegen. Suche vorwärts wird von der aktuellen Bookmark gestartet. sucht rückwärts startet aus der Zeile vor der Textmarke. Die Endposition der Suche wird unmittelbar vor die erste Zeile gefunden wird, dass die Einschränkung und sich vergewissert haben. 
  
Wenn die Zeile, die auf das durch die Textmarke im _BkOrigin_ -Parameter in der Tabelle nicht mehr vorhanden ist und die Tabelle eine neue Position für das Lesezeichen kann nicht hergestellt werden, gibt **FindRow** MAPI_E_INVALID_BOOKMARK zurück. Wenn die Zeile, die auf den _BkOrigin_ nicht mehr vorhanden ist und die Tabelle wird eine neue Position für das Lesezeichen herstellen, gibt **FindRow** MAPI_W_POSITION_CHANGED zurück. 
  
Wenn die Textmarke _BkOrigin_ übergebenen BOOKMARK_BEGINNING oder BOOKMARK_END ist, gibt **FindRow** MAPI_E_NOT_FOUND, wenn keine entsprechende Zeile gefunden wird. Wenn die Textmarke in _BkOrigin_ verwendete BOOKMARK_CURRENT ist, können **FindRow** MAPI_W_POSITION_CHANGED, aber nicht MAPI_E_INVALID_BOOKMARK zurück, da immer eine aktuellen Cursorposition ist. 
  
Die Spalte **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) ist erforderlich für alle Tabellen und alle Implementierungen von **FindRow** sind erforderlich, um eine Zeile basierend auf PR_INSTANCE_KEY Suchvorgänge unterstützt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Der Typ des Präfix suchen, die von **FindRow** durchgeführt ist nur nützlich, wenn die Suche die gleiche Richtung wie die Tabelle Organisation folgt. Um das erforderliche Verhalten zu erzielen, sollte die Vergleichsfunktion, durch die in der Eigenschaft Einschränkung Struktur übergeben **RELOP_GE** impliziert die gleichen Vergleichsfunktion sein, auf der die Sortierreihenfolge für die Tabelle basiert. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

**FindRow** können zur Unterstützung von Bildlauf basierend auf Zeichenfolgen vom Benutzer, insbesondere in Listenfeldern in Dialogfeldern Adresse eingegeben haben. Bei dieser Art von Bildlauf geben die Benutzer ein stetig länger Präfixen einen gewünschten String-Wert, und Sie können in regelmäßigen Abständen Ausstellen eines Anrufs **FindRow** , auf die erste Zeile zu wechseln, die mit das Präfix übereinstimmt. Die Richtung der Cursor springt welcher Richtung die Suche abhängt ist ausführen festgelegt. 
  
Um **FindRow**verwenden zu können, muss eine Textmarke festgelegt werden. Die Zeichenfolgensuche kann von alle Textmarken, einschließlich aus der vordefinierten Lesezeichen zurück, die die aktuelle Position und Anfang und Ende der Tabelle stammen. Wenn eine große Anzahl von Zeilen in der Tabelle vorhanden sind, kann der Suchvorgang langsam sein.
  
Verwenden Sie eine Einschränkung, um ein Präfix Zeichenfolge wie folgt einen Bildlauf zu erhalten. Übergeben Sie für die Suche nach vorne zu einer Spalte in aufsteigender Reihenfolge sortiert und für die Abwärtskompatibilität Suche auf eine Spalte in absteigender Reihenfolge sortiert eine Eigenschaft Einschränkung Struktur in der _LpRestriction_ -Parameter mit der Beziehung **RELOP_GE** und die entsprechenden Eigenschafts-Tag und Präfix, mit dem Format _Tag_ **GE** _Präfix_. 
  
Weitere Informationen zur Verwendung von Strukturen Einschränkung zum Angeben eines Filters finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI (engl.) wird die **IMAPITable** -Methode verwendet, um Zeilen zu finden, die eine Einschränkung entsprechen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

