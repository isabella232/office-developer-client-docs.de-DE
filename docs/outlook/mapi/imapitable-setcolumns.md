---
title: IMAPITableSetColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.SetColumns
api_type:
- COM
ms.assetid: 9a39cf8d-df0f-493c-b272-f15c65b3f15e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 45ac1cd1a55bc320aba5a725c26b964226fa1245
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600862"
---
# <a name="imapitablesetcolumns"></a>IMAPITable::SetColumns

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert die bestimmten Eigenschaften und die Reihenfolge der Eigenschaften, die als Spalten in der Tabelle angezeigt werden sollen.
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpPropTagArray_
  
> [in] Zeiger auf ein Array von Eigenschaftentags, die Eigenschaften identifizieren, die als Spalten in der Tabelle eingeschlossen werden sollen. Der Eigenschaftstypteil jedes Tags kann auf einen gültigen Typ oder auf **PR_NULL** festgelegt werden, um Platz für nachfolgende Ergänzungen zu reservieren. Der  _parameter lpPropTagArray_ kann nicht auf NULL festgelegt werden; Jede Tabelle muss mindestens eine Spalte enthalten. 
    
 _ulFlags_
  
> [in] Bitmaske von Flags, die die Rückgabe eines asynchronen Aufrufs von **SetColumns** steuert, z. B. wenn **SetColumns** in der Benachrichtigung verwendet wird. Die folgenden Flags können festgelegt werden: 
    
TBL_ASYNC 
  
> Fordert an, dass der Spalteneinstellungsvorgang asynchron ausgeführt wird, **sodass SetColumns** möglicherweise zurückgegeben wird, bevor der Vorgang vollständig abgeschlossen ist. 
    
TBL_BATCH 
  
> Ermöglicht der Tabelle, den Spalteneinstellungsvorgang zu verschieben, bis die Daten tatsächlich erforderlich sind.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Vorgang zum Festlegen von Spalten war erfolgreich.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Vorgang zum Festlegen von Spalten gestartet wird. Entweder sollte der laufende Vorgang abgeschlossen werden können, oder er sollte beendet werden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Der Spaltensatz einer Tabelle ist die Gruppe von Eigenschaften, die die Spalten für die Zeilen in der Tabelle bilden. Für jeden Tabellentyp ist ein Standardspaltensatz festgelegt. Der Standardspaltensatz besteht aus den Eigenschaften, die der Tabellen implementer automatisch einschließt. Tabellenbenutzer können diesen Standardsatz ändern, indem sie die **IMAPITable::SetColumns-Methode** aufrufen. Sie können anfordern, dass andere Spalten zum Standardsatz hinzugefügt werden, wenn der Tabellen implementer unterstützt, dass Spalten entfernt oder die Reihenfolge der Spalten geändert werden. **SetColumns** gibt die Spalten an, die mit jeder Zeile zurückgegeben werden, und die Reihenfolge dieser Spalten in der Zeile. 
  
Der Erfolg des **SetColumns-Vorgangs** wird erst angezeigt, nachdem ein nachfolgender Aufruf zum Abrufen der Daten der Tabelle ausgeführt wurde. Anschließend werden alle Fehler gemeldet. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Einige Anbieter ermöglichen einem **SetColumns-Aufruf,** nur Tabellenspalten zu ordnen, die Teil der verfügbaren Spalten für eine Tabellenansicht sind. Andere Anbieter ermöglichen es einem **SetColumns-Aufruf,** alle Tabellenspalten zu ordnen, einschließlich derjenigen, die Eigenschaften enthalten, die nicht im ursprünglichen Spaltensatz enthalten sind. 
  
Wenn TBL_BATCH für asynchrone Vorgänge festgelegt ist, sollten Anbieter einen Eigenschaftstyp von PT_ERROR und einen Eigenschaftswert null für Spalten zurückgeben, die nicht unterstützt werden.
  
Sie müssen nicht auf das TBL_ASYNC Flag reagieren, das anfordert, dass der Vorgang asynchron ist. Wenn Sie die Definition des asynchronen Spaltensatzes nicht unterstützen, führen Sie den Vorgang synchron aus. Wenn Sie die TBL_ASYNC-Kennzeichnung unterstützen können und ein weiterer asynchroner Vorgang noch ausgeführt wird, geben Sie MAPI_E_BUSY zurück. Andernfalls geben Sie S_OK zurück, unabhängig davon, ob Sie alle im Eigenschaftentag-Array enthaltenen Eigenschaften unterstützen oder nicht. Fehler, die sich aus nicht unterstützten Eigenschaften ergeben, sollten von **IMAPITable-Methoden** zurückgegeben werden, die Daten abrufen, z. B. **QueryRows**. 
  
Generieren Sie keine Benachrichtigungen für Tabellenzeilen, die durch Aufrufe von **Restrict** aus der Ansicht ausgeblendet werden. 
  
Beim Senden von Tabellenbenachrichtigungen müssen die Reihenfolge der Eigenschaften im **Zeilenelement** der [TABLE_NOTIFICATION-Struktur](table_notification.md) und die durch den letzten **SetColumns-Aufruf** angegebene Reihenfolge mit dem Zeitpunkt übereinstimmen, zu dem die Benachrichtigungsanforderung gesendet wurde. 
  
Mit einem anderen Flag, TBL_BATCH, können Aufrufer angeben, dass der Tabellen implementer die Auswertung der Ergebnisse des Vorgangs bis zu einem späteren Zeitpunkt zurückstellen kann. Aufrufer sollten dieses Kennzeichen nach Möglichkeit festlegen, da der Batchvorgang die Leistung verbessert.
  
Häufig ist es für Aufrufer praktisch, einige Spalten in der abgerufenen Zeile zu reservieren, die für Werte festgelegt sind, die später hinzugefügt werden sollen. Callers do this by placing **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) at the desired positions in the property tag array passed to **SetColumns**; Die Tabelle übergibt dann **PR_NULL** an diesen Positionen in allen Zeilen zurück, die mit **QueryRows** abgerufen wurden.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Ordnen Sie beim Erstellen des Eigenschaftentagarrays für den  _LpPropTagArray-Parameter_ die Tags in der Reihenfolge an, in der die Spalten in der Tabellenansicht angezeigt werden sollen. 
  
Sie können mehrwertige Eigenschaften angeben, die in den Spaltensatz eingeschlossen werden sollen, indem Sie das Flag für die mehrwertige Instanz oder MVI_FLAG Konstante auf das Eigenschaftentag anwenden. Legen Sie dieses Kennzeichen fest, indem Sie das Eigenschaftstag für die einwertige Version der Eigenschaft wie folgt als Parameter an das makro MVI_PROP übergeben:
  
```
MVI_PROP(ulPropTag)

```

Das MVI_PROP-Makro legt MVI_FLAG für die Eigenschaft fest und wandelt das Tag in ein mehrwertiges Tag um. Wenn Sie fälschlicherweise versuchen, MVI_PROP für eine einwertige Eigenschaft aufzurufen, ignoriert MAPI den Aufruf und lässt das Eigenschaftstag unverändert. 
  
Sie können Eigenschaftentags, die auf **PR_NULL** festgelegt sind, in das Eigenschaftentagarray einschließen, um Platz im Spaltensatz zu reservieren. Durch das Reservieren von Leerzeichen können Sie einem Spaltensatz hinzufügen, ohne ein neues Eigenschaftentagarray zuordnen zu müssen. 
  
Wenn der Aufruf von **SetColumns** eine Änderung der Reihenfolge der Spalten einer Tabelle bewirkt und eine oder mehrere dieser Spalten eine mehrwertige Eigenschaft darstellen, kann die Anzahl der Zeilen in der Tabelle erhöht werden. In diesem Fall werden alle Textmarken für die Tabelle verworfen. Weitere Informationen dazu, wie sich mehrwertige Spalten auf Tabellen auswirken, finden Sie unter [Arbeiten mit mehrwertigen Spalten.](working-with-multivalued-columns.md)
  
Das Festlegen von Spalten ist standardmäßig ein synchroner Vorgang. Sie können jedoch zulassen, dass die Tabelle den Vorgang so lange zurückstellt, bis die Daten benötigt werden, indem Sie das flag TBL_BATCH festlegen. Das Festlegen dieses Kennzeichens kann die Leistung verbessern. Ein weiteres Flag, TBL_ASYNC, macht den Vorgang asynchron, **sodass SetColumns** zurückgegeben werden kann, bevor der Vorgang abgeschlossen ist. Um zu bestimmen, wann der Abschluss erfolgt, rufen Sie [IMAPITable::GetStatus](imapitable-getstatus.md)auf.
  
Wenn ein Aufruf von **SetColumns** MAPI_E_BUSY zurückgibt und angibt, dass ein anderer Vorgang den Start des Vorgangs verhindert, können Sie [IMAPITable::Abort](imapitable-abort.md) aufrufen, um den laufenden Vorgang zu beenden. 
  
Sie können [hrAddColumnsEx](hraddcolumnsex.md) auch aufrufen, um einen Spaltensatz zu ändern. Der Unterschied zwischen **HrAddColumnsEx** und **IMAPITable::SetColumns** besteht darin, dass **HrAddColumnsEx** weniger flexibel ist; Sie kann nur Spalten hinzufügen. Die zusätzlichen Spalten werden am Anfang des Spaltensatzes platziert. Alle vorhandenen Spalten werden nach diesen Spalten angezeigt. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oSetColumns  <br/> |MFCMAPI verwendet die **IMAPITable::SetColumns-Methode,** um die gewünschten Spalten für die Tabelle festzulegen.  <br/> |
   
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

