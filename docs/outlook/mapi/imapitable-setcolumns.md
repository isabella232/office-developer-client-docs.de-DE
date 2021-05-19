---
title: IMAPITableSetColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetColumns
api_type:
- COM
ms.assetid: 9a39cf8d-df0f-493c-b272-f15c65b3f15e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 897330feb216dbc3ab143378977c77141cf488f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416349"
---
# <a name="imapitablesetcolumns"></a>IMAPITable::SetColumns

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert die bestimmten Eigenschaften und die Reihenfolge der Eigenschaften, die in der Tabelle als Spalten angezeigt werden sollen.
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpPropTagArray_
  
> [in] Zeiger auf ein Array von Eigenschaftstags, die Eigenschaften identifizieren, die als Spalten in der Tabelle enthalten sein sollen. Der Eigenschaftentypteil jedes Tags kann auf einen  gültigen Typ festgelegt oder PR_NULL, um Platz für nachfolgende Ergänzungen zu reservieren. Der  _lpPropTagArray-Parameter_ kann nicht auf NULL festgelegt werden. Jede Tabelle muss mindestens eine Spalte enthalten. 
    
 _ulFlags_
  
> [in] Bitmaske von Flags, die die Rückgabe eines asynchronen Aufrufs von **SetColumns** steuert, z. B. wenn **SetColumns** in der Benachrichtigung verwendet wird. Die folgenden Kennzeichen können festgelegt werden: 
    
TBL_ASYNC 
  
> Fordert an, dass der Spalteneinstellungsvorgang asynchron ausgeführt wird, wodurch **SetColumns** möglicherweise zurückgesendet wird, bevor der Vorgang vollständig abgeschlossen ist. 
    
TBL_BATCH 
  
> Ermöglicht der Tabelle, den Spalteneinstellungsvorgang so lange zu verschieben, bis die Daten tatsächlich erforderlich sind.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Spalteneinstellungsvorgang war erfolgreich.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Spalteneinstellungsvorgang gestartet wird. Der ausgeführte Vorgang sollte entweder abgeschlossen oder beendet werden.
    
## <a name="remarks"></a>Hinweise

Der Spaltensatz einer Tabelle ist die Gruppe von Eigenschaften, aus der die Spalten für die Zeilen in der Tabelle besteht. Für jeden Tabellentyp ist ein Standardspaltensatz festgelegt. Der Standardspaltensatz besteht aus den Eigenschaften, die der Tabellen implementier automatisch enthält. Tabellenbenutzer können diesen Standardsatz ändern, indem sie die **IMAPITable::SetColumns-Methode** aufrufen. Sie können anfordern, dass dem Standardsatz weitere Spalten hinzugefügt werden, wenn der Tabellen implementier sie unterstützt, dass Spalten entfernt oder die Reihenfolge der Spalten geändert wird. **SetColumns** gibt die Spalten an, die mit jeder Zeile zurückgegeben werden, und die Reihenfolge dieser Spalten innerhalb der Zeile. 
  
Der Erfolg des **SetColumns-Vorgangs** wird erst sichtbar, nachdem ein nachfolgender Aufruf zum Abrufen der Daten der Tabelle erfolgt ist. Dann werden Fehler gemeldet. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Einige Anbieter lassen einen **SetColumns-Aufruf** zu, um nur Tabellenspalten zu bestellen, die Teil der verfügbaren Spalten für eine Tabellenansicht sind. Andere Anbieter ermöglichen einen **SetColumns-Aufruf,** um alle Tabellenspalten zu sortieren, einschließlich derjenigen, die Eigenschaften enthalten, die nicht im ursprünglichen Spaltensatz enthalten sind. 
  
Wenn TBL_BATCH für asynchrone Vorgänge festgelegt ist, sollten Anbieter den Eigenschaftstyp PT_ERROR und den Eigenschaftswert NULL für Spalten zurückgeben, die nicht unterstützt werden.
  
Sie müssen nicht auf das TBL_ASYNC reagieren, das anfordert, dass der Vorgang asynchron ist. Wenn Sie keine asynchrone Spaltensatzdefinition unterstützen, führen Sie den Vorgang synchron aus. Wenn Sie das TBL_ASYNC unterstützen können und ein weiterer asynchroner Vorgang noch ausgeführt wird, geben Sie die MAPI_E_BUSY. Andernfalls geben Sie S_OK zurück, unabhängig davon, ob Sie alle Eigenschaften unterstützen, die im Eigenschaftentagarray enthalten sind. Fehler, die sich aus nicht unterstützten Eigenschaften ergeben, sollten von **IMAPITable-Methoden** zurückgegeben werden, die Daten abrufen, z. B. **QueryRows**. 
  
Generieren Sie keine Benachrichtigungen für Tabellenzeilen, die durch Aufrufe von Restrict ausgeblendet **werden.** 
  
Beim Senden von Tabellenbenachrichtigungen müssen  die Reihenfolge der Eigenschaften im Zeilenm member der [TABLE_NOTIFICATION-Struktur](table_notification.md) und die durch den letzten **SetColumns-Aufruf** angegebene Reihenfolge mit dem Zeitpunkt identisch sein, zu dem die Benachrichtigungsanforderung gesendet wurde. 
  
Ein weiteres Flag, TBL_BATCH, ermöglicht Anrufern anzugeben, dass der Tabellen implementierer die Auswertung der Ergebnisse des Vorgangs auf einen späteren Zeitpunkt zurückdingen kann. Wenn möglich, sollten Anrufer dieses Flag festlegen, da der Batchvorgang die Leistung verbessert.
  
Für Anrufer ist es häufig praktisch, einige Spalten im abgerufenen Zeilensatz für Werte zu reservieren, die später hinzugefügt werden. Aufrufer tun **dies, indem PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) an den gewünschten Positionen im Eigenschaftstagarray platziert werden, das an **SetColumns übergeben wird;** Die Tabelle gibt dann die PR_NULL **an** diesen Positionen in allen Zeilen zurück, die mit **QueryRows abgerufen werden.**
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Beim Erstellen des Eigenschaftentagarrays für den  _lpPropTagArray-Parameter_ müssen Sie die Tags in der Reihenfolge sortieren, in der die Spalten in der Tabellenansicht angezeigt werden sollen. 
  
Sie können mehrwertige Eigenschaften angeben, die in den Spaltensatz eingeschlossen werden sollen, indem Sie das Kennzeichen der mehrwertigen Instanz oder MVI_FLAG Eigenschaftstags anwenden. Legen Sie dieses Flag durch Übergeben des Eigenschaftstags für die einwertig version der Eigenschaft als Parameter an das MVI_PROP makro wie folgt:
  
```
MVI_PROP(ulPropTag)

```

Das MVI_PROP-Makro wird MVI_FLAG eigenschaft festlegen und das Tag in ein mehrwertiges Tag umfunktioniert. Wenn Sie fälschlicherweise versuchen, MVI_PROP einer einwertigen Eigenschaft auf aufruft, ignoriert MAPI den Aufruf und belassen das Eigenschaftstag unverändert. 
  
Sie können Eigenschaftstags, die auf PR_NULL festgelegt sind, in das Eigenschaftentagarray **hinzufügen,** um Platz im Spaltensatz zu reservieren. Wenn Sie Speicherplatz reservieren, können Sie einem Spaltensatz hinzufügen, ohne ein neues Eigenschaftentagarray zuweisen zu müssen. 
  
Wenn der Aufruf von **SetColumns** eine Änderung der Reihenfolge der Spalten einer Tabelle bewirkt und eine oder mehrere dieser Spalten eine mehrwertige Eigenschaft darstellen, kann die Anzahl der Zeilen in der Tabelle erhöht werden. In diesem Fall werden alle Lesezeichen für die Tabelle verworfen. Weitere Informationen dazu, wie sich mehrwertige Spalten auf Tabellen auswirken, finden Sie unter [Working with Multivalued Columns](working-with-multivalued-columns.md).
  
Das Festlegen von Spalten ist standardmäßig ein synchroner Vorgang. Sie können jedoch zulassen, dass die Tabelle den Vorgang so lange verschiebt, bis die Daten benötigt werden, indem Sie TBL_BATCH festlegen. Das Festlegen dieses Kennzeichens kann die Leistung verbessern. Ein weiteres Flag, TBL_ASYNC, macht den Vorgang asynchron, sodass **SetColumns** zurückgeben kann, bevor der Vorgang abgeschlossen ist. Rufen Sie [IMAPITable::GetStatus](imapitable-getstatus.md)auf, um zu bestimmen, wann der Abschluss erfolgt.
  
Wenn ein Aufruf von **SetColumns** MAPI_E_BUSY, der angibt, dass ein anderer Vorgang das Starten des Vorgangs verhindert, können Sie [IMAPITable::Abort](imapitable-abort.md) aufrufen, um den ausgeführten Vorgang zu beenden. 
  
Sie können auch [HrAddColumnsEx aufrufen,](hraddcolumnsex.md) um einen Spaltensatz zu ändern. Der Unterschied zwischen **HrAddColumnsEx und** **IMAPITable::SetColumns** ist, dass **HrAddColumnsEx** weniger flexibel ist. Es können nur Spalten hinzugefügt werden. Die zusätzlichen Spalten werden am Anfang des Spaltensatzs platziert. alle vorhandenen Spalten werden nach diesen Spalten angezeigt. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oSetColumns  <br/> |MFCMAPI verwendet die **IMAPITable::SetColumns-Methode,** um die gewünschten Spalten für die Tabelle festlegen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[HrQueryAllRows](hrqueryallrows.md)
  
[IMAPITable::Abort](imapitable-abort.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SPropTagArray](sproptagarray.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

