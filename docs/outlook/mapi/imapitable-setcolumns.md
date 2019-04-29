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
  
Definiert die Eigenschaften und die Reihenfolge der Eigenschaften, die als Spalten in der Tabelle angezeigt werden sollen.
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpPropTagArray_
  
> in Zeiger auf ein Array von Eigenschaftstags, das Eigenschaften angibt, die als Spalten in der Tabelle eingeschlossen werden sollen. Der Eigenschaftentyp Teil jedes Tags kann auf einen gültigen Typ oder auf **PR_NULL** festgelegt werden, um Platz für nachfolgende Ergänzungen zu reservieren. Der Parameter _lpPropTagArray_ kann nicht auf NULL festgelegt werden; jede Tabelle muss mindestens eine Spalte enthalten. 
    
 _ulFlags_
  
> in Bitmaske von Flags, die die Rückgabe eines asynchronen Aufrufs an SetColumns steuert, beispielsweise wenn SetColumns in Notification verwendet wird. **** **** Die folgenden Flags können festgelegt werden: 
    
TBL_ASYNC 
  
> Fordert, dass der Vorgang der Spalten Einstellung asynchron ausgeführt **** wird, sodass SetColumns potenziell zurückgegeben werden können, bevor der Vorgang vollständig abgeschlossen wurde. 
    
TBL_BATCH 
  
> Ermöglicht es der Tabelle, den Vorgang der Spalten Einstellung zu verschieben, bis die Daten tatsächlich erforderlich sind.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Spalten Einstellung war erfolgreich.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass die Spalten Einstellung gestartet wird. Entweder sollte der ausgeführte Vorgang abgeschlossen oder beendet werden.
    
## <a name="remarks"></a>Bemerkungen

Der Spaltensatz einer Tabelle ist die Gruppe von Eigenschaften, die die Spalten für die Zeilen in der Tabelle bilden. Für jeden Tabellentyp ist eine Standardspaltengruppe festgelegt. Der Standardspaltensatz besteht aus den Eigenschaften, die von der Tabellen Implementierung automatisch eingeschlossen werden. Tabellen Benutzer können diese Standardeinstellung ändern, indem Sie die **IMAPITable::** SetColumns-Methode aufrufen. Sie können anfordern, dass andere Spalten dem Standardsatz hinzugefügt werden, wenn die Tabellen Implementierung Sie unterstützt, dass Spalten entfernt werden, oder dass die Reihenfolge der Spalten geändert wird. **** SetColumns gibt die Spalten an, die mit jeder Zeile und der Reihenfolge dieser Spalten innerhalb der Zeile zurückgegeben werden. 
  
Der Erfolg des SetColumns-Vorgangs ist nur offensichtlich, nachdem ein weiterer Aufruf ausgeführt wurde, um die Daten der Tabelle abzurufen. **** Es werden dann Fehler gemeldet. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Einige Anbieter lassen einen **** SetColumns-Aufruf nur Tabellenspalten zu, die Teil der verfügbaren Spalten für eine Tabellenansicht sind. Andere Anbieter ermöglichen einen **** SetColumns-Aufruf zum Sortieren aller Tabellenspalten, einschließlich der Eigenschaften, die nicht im ursprünglichen Spaltensatz enthalten sind. 
  
Wenn TBL_BATCH für asynchrone Vorgänge festgelegt ist, sollten Anbieter einen Eigenschaftentyp von PT_ERROR und einen Eigenschaftswert von NULL für Spalten zurückgeben, die nicht unterstützt werden.
  
Sie müssen nicht auf das TBL_ASYNC-Flag Antworten, das die asynchrone Operation anfordert. Wenn Sie die asynchrone Spaltensatz Definition nicht unterstützen, führen Sie den Vorgang synchron aus. Wenn Sie das TBL_ASYNC-Flag unterstützen können und ein weiterer asynchroner Vorgang noch ausgeführt wird, geben Sie MAPI_E_BUSY zurück. Andernfalls wird S_OK zurückgegeben, unabhängig davon, ob Sie alle im Property-Tag-Array enthaltenen Eigenschaften unterstützen. Fehler, die aus nicht unterstützten Eigenschaften resultieren, sollten von **IMAPITable** -Methoden zurückgegeben werden, die Daten wie **QueryRows**abrufen. 
  
Generieren Sie keine Benachrichtigungen für Tabellenzeilen, die durch Aufrufe von **Restrict**ausgeblendet werden. 
  
Beim Senden von Tabellen Benachrichtigungen muss die Reihenfolge der Eigenschaften im **Row** -Element der [TABLE_NOTIFICATION](table_notification.md) -Struktur und der durch den letzten SetColumns-Aufruf angegebenen Reihenfolge mit dem Zeitpunkt übereinstimmen, zu dem die Benachrichtigungsanforderung **** gesendet wurde. 
  
Ein weiteres Flag, TBL_BATCH, ermöglicht es Aufrufern, anzugeben, dass die Tabellen Implementierung die Auswertung der Ergebnisse des Vorgangs bis zu einem späteren Zeitpunkt zurückstellen kann. Wenn möglich, sollten Anrufer dieses Flag festlegen, da der Batchvorgang die Leistung verbessert.
  
Es ist oft hilfreich, wenn Anrufer einige Spalten im abgerufenen Zeilensatz für Werte reservieren, die später hinzugefügt werden sollen. Anrufer tun dies, indem Sie **PR_NULL** ([pidtagnull (](pidtagnull-canonical-property.md)) an den gewünschten Positionen im Property Tag-Array an **** SetColumns übergeben; die Tabelle übergibt dann **PR_NULL** an diesen Positionen in allen Zeilen, die mit **QueryRows**abgerufen werden.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Beim Erstellen des Eigenschaftentag Arrays für den Parameter _lpPropTagArray_ ordnen Sie die Tags in der Reihenfolge an, in der die Spalten in der Tabellenansicht angezeigt werden sollen. 
  
Sie können mehrwertige Eigenschaften angeben, die in den Spaltensatz eingeschlossen werden sollen, indem Sie das Flag für mehrwertige Instanzen oder MVI_FLAG-Konstante auf das Property-Tag anwenden. Legen Sie dieses Flag fest, indem Sie das Property-Tag für die einwertige Version der Eigenschaft wie folgt als Parameter an das MVI_PROP-Makro übergeben:
  
```
MVI_PROP(ulPropTag)

```

Das MVI_PROP-Makro legt MVI_FLAG für die Eigenschaft fest, wobei das Tag in ein mehrwertiges Tag verwandelt wird. Wenn Sie fälschlicherweise versuchen, MVI_PROP für eine einwertige Eigenschaft aufzurufen, ignoriert MAPI den Aufruf und lässt das Tag der Eigenschaft unverändert. 
  
Sie können Eigenschaftstags, die auf **PR_NULL** festgelegt sind, im Property-Tag-Array einfügen, um Platz im Spaltensatz zu reservieren. Durch das Reservieren von Speicherplatz können Sie zu einem Spaltensatz hinzufügen, ohne ein neues Property-Tag-Array zuweisen zu müssen. 
  
Wenn der Aufruf von **** SetColumns eine Änderung an der Reihenfolge der Spalten einer Tabelle bewirkt und eine oder mehrere dieser Spalten eine mehrwertige Eigenschaft darstellen, ist es möglich, dass die Anzahl der Zeilen in der Tabelle erhöht wird. In diesem Fall werden alle Lesezeichen für die Tabelle verworfen. Weitere Informationen zur Auswirkung von mehrwertigen Spalten auf Tabellen finden Sie unter [Working with](working-with-multivalued-columns.md)mehr-Valued Columns.
  
Das Festlegen von Spalten ist standardmäßig ein synchroner Vorgang. Sie können jedoch zulassen, dass die Tabelle den Vorgang so lange verschiebt, bis die Daten erforderlich sind, indem Sie das TBL_BATCH-Flag festlegen. Durch Festlegen dieses Flags kann die Leistung verbessert werden. Ein weiteres Flag, TBL_ASYNC, macht den Vorgang asynchron **** , sodass SetColumns zurückgegeben werden können, bevor der Vorgang abgeschlossen ist. Um zu bestimmen, wann der Abschluss auftritt, rufen Sie [IMAPITable:: GetStatus](imapitable-getstatus.md)auf.
  
Wenn ein Aufruf von **** SetColumns MAPI_E_BUSY zurückgibt, was bedeutet, dass ein anderer Vorgang das Starten des Vorgangs verhindert, können Sie [IMAPITable:: Abort](imapitable-abort.md) aufrufen, um den laufenden Vorgang zu beenden. 
  
Sie können auch [HrAddColumnsEx](hraddcolumnsex.md) aufrufen, um einen Spaltensatz zu ändern. Der Unterschied zwischen **HrAddColumnsEx** und **IMAPITable::** SetColumns besteht darin, dass **HrAddColumnsEx** nicht so flexibel ist; Es können nur Spalten hinzugefügt werden. Die zusätzlichen Spalten werden am Anfang des Spaltensatzes angeordnet; alle vorhandenen Spalten werden nach diesen Spalten angezeigt. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl::D oSetColumns  <br/> |MFCMAPI verwendet die **IMAPITable::** SetColumns-Methode, um die gewünschten Spalten für die Tabelle festzulegen.  <br/> |
   
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

