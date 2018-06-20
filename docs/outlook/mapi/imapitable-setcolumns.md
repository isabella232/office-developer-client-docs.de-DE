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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9eeab1e1186aeb5a9b458facd59bd4cc155e8014
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792470"
---
# <a name="imapitablesetcolumns"></a>IMAPITable::SetColumns

  
  
**Betrifft**: Outlook 
  
Definiert die jeweiligen Eigenschaften und die Reihenfolge der Eigenschaften als Spalten in der Tabelle angezeigt werden.
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpPropTagArray_
  
> [in] Zeiger auf ein Array von Eigenschaftentags, identifiziert Eigenschaften als Spalten in der Tabelle eingeschlossen werden sollen. Der Eigenschaft Typ Teil jedes Tag kann ein gültiger Typ oder **PR_NULL** Reservieren von Speicherplatz für nachfolgende Ergänzungen festgelegt werden. Der _LpPropTagArray_ -Parameter kann nicht auf NULL festgelegt werden. Jede Tabelle muss mindestens eine Spalte haben. 
    
 _ulFlags_
  
> [in] Bitmaske aus Flags, die steuert die Rückgabe von einen asynchronen Aufruf an **SetColumns**, beispielsweise wenn **SetColumns** in der Benachrichtigung verwendet wird. Die folgenden Kennzeichen können festgelegt werden: 
    
TBL_ASYNC 
  
> Anforderungen, die der Vorgang der Spalte Einstellung werden ausgeführt, asynchron verursacht **SetColumns** , potenziell zurückzugeben, bevor der Vorgang vollständig abgeschlossen wurde. 
    
TBL_BATCH 
  
> Ermöglicht die Tabelle, um den Vorgang der Spalte Einstellung verschieben, bis die Daten tatsächlich erforderlich ist.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Spalte Einstellung Vorgang erfolgreich war.
    
MAPI_E_BUSY 
  
> Ein anderer Vorgang wird ausgeführt, die verhindert, die Spalte festlegen Vorgang dass gestartet wird. Entweder dürfen der Vorgang in Arbeit abgeschlossen oder angehalten werden sollte.
    
## <a name="remarks"></a>Hinweise

Die Spalte einer Tabelle ist die Gruppe von Eigenschaften, die die Spalten für die Zeilen in der Tabelle bilden. Es ist eine Standardspalte für jede Art von Tabelle festgelegt. Die standardspaltensammlung besteht aus den Eigenschaften, die der Tabelle Implementierer automatisch enthält. Benutzer können diese durch Aufrufen der Methode **IMAPITable::SetColumns** Standard ändern. Sie können anfordern, dass weitere Spalten hinzugefügt werden, auf den Standardwert festgelegt, wenn die Tabelle-Implementierung unterstützt diese Spalten entfernt werden soll, oder die Reihenfolge der Spalten geändert werden. **SetColumns** gibt die Spalten, die zurückgegeben werden mit jeder Zeile und die Reihenfolge der diese Spalten in der Zeile an. 
  
Der Erfolg des Vorgangs **SetColumns** wird deutlich, nachdem ein nachfolgender Aufruf ausgeführt wurde, um die Daten der Tabelle abzurufen. Es ist, dass Fehler gemeldet werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Einige Anbieter zulassen Gespräch **SetColumns** bestellen nur die Spalten, die Teil der Spalten für eine Tabellenansicht verfügbaren sind. Andere Anbieter zulassen Gespräch **SetColumns** , um alle Spalten der Tabelle, einschließlich derjenigen, die Eigenschaften nicht in der ursprünglichen Spalte Sammlung enthält bestellen. 
  
TBL_BATCH für asynchrone Vorgänge festgelegt ist, sollte Anbieter zurückgeben, der Eigenschaftentyp PT_ERROR und den Wert einer Eigenschaft NULL für Spalten, die nicht unterstützt werden.
  
Sie müssen nicht reagieren Sie auf die Kennzeichnung des TBL_ASYNC anfordern, dass der Vorgang asynchron sein. Wenn Sie asynchrone Set-Spaltendefinition nicht unterstützen, führen Sie den Vorgang synchron. Wenn Sie das Kennzeichen TBL_ASYNC und eine andere asynchrone unterstützen können wird Vorgang noch ausgeführt, MAPI_E_BUSY zurück. Geben Sie andernfalls S_OK zurück, unabhängig davon, ob Sie alle Eigenschaften in Array der Tag-Eigenschaft enthalten unterstützen. Fehler aufgrund von nicht unterstützten Eigenschaften sollte **IMAPITable** Methoden zurückgegeben werden, die Daten enthält, wie **QueryRows**abrufen. 
  
Generieren Sie Benachrichtigungen für Zeilen, in denen ausgeblendet sind nicht aus der Ansicht durch **Restrict**Aufrufe. 
  
Beim Senden von Benachrichtigungen der Tabelle, die Reihenfolge der Eigenschaften in der **Zeile** Mitglied der [TABLE_NOTIFICATION](table_notification.md) -Struktur und der Reihenfolge vom angegebenen muss des letzten Aufrufs **SetColumns** mit dem Zeitpunkt der Erstellung, die die Benachrichtigung anfordern gesendet wurde. 
  
Eine andere Kennzeichnung, TBL_BATCH, ermöglicht es dem Aufrufer anzugeben, dass der Tabelle Implementierer verzögern kann die Ergebnisse des Vorgangs bis zu einem späteren Zeitpunkt auswerten. Wann immer möglich, sollten Aufrufer dieses Flag festgelegt, da im Batchmodus Vorgang verbessert die Leistung.
  
Häufig ist es sinnvoll für Anrufer, reservieren einige Spalten in der abgerufenen Rowset für Werte, die später hinzugefügt werden. Anrufer Zweck zu diesem Platzieren von **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) an den gewünschten Positionen im Array Eigenschaft-Tag **SetColumns**übergeben; die Tabelle wird dann wieder Durchgang **PR_NULL** an diese Positionen in allen Zeilen mit **QueryRows**abgerufen.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Beim Erstellen des Arrays-Tag-Eigenschaft für den Parameter _LpPropTagArray_ Reihenfolge, die Tags in der Reihenfolge, in der Sie die Spalten in der Tabelle angezeigt werden sollen. 
  
Mehrwertige Eigenschaften, die in der Spalte festlegen, indem die mehrwertige Instanzenflag oder MVI_FLAG-Konstante, um das Eigenschafts-Tag anwenden enthalten sein können angegeben werden. Legen Sie dieses Flag, indem das Eigenschafts-Tag für die ein einwertiges Version der-Eigenschaft als Parameter an das Makro MVI_PROP wie folgt:
  
```
MVI_PROP(ulPropTag)

```

Das Makro MVI_PROP wird für die Eigenschaft, aktivieren das Tag in einem mehrwertigen Tag MVI_FLAG festgelegt. Wenn Sie versehentlich MVI_PROP für eine Eigenschaft einwertig aufrufen versuchen, MAPI den Anruf ignoriert und das Eigenschafts-Tag unverändert lassen. 
  
Sie können durch Festlegen auf **PR_NULL** im Array Tag-Eigenschaft wird in der Spalte Menge Speicherplatz reservieren Eigenschaftentags einschließen. Reservieren von Speicherplatz, können Sie eine Spalte festgelegt, ohne dass eine neue Eigenschaft Tag eines Arrays hinzuzufügen. 
  
Wenn der Aufruf **SetColumns** , eine Änderung Reihenfolge einer Tabelle Spalten veranlasst und eine oder mehrere dieser Spalten eine mehrwertige Eigenschaft darstellen, ist es möglich, für die Anzahl der Zeilen in der Tabelle zu erhöhen. In diesem Fall werden alle Textmarken für die Tabelle verworfen. Weitere Informationen dazu, wie Sie mehrwertige Spalten Tabellen beeinflussen, finden Sie unter [Arbeiten mit Spalten mit mehreren Werten](working-with-multivalued-columns.md).
  
Festlegen von Spalten ist standardmäßig eine synchrone Operation. Sie können jedoch die Tabelle, um den Vorgang zu verschieben, solange die Daten benötigt werden, indem Sie das TBL_BATCH-Flag festlegen. Wenn Sie dieses Flag kann die Leistung verbessert. Einer anderen Kennzeichnung, TBL_ASYNC, wird den Vorgang asynchron, sodass **SetColumns** , zurückzugeben, bevor der Vorgang abgeschlossen ist. Um zu bestimmen, tritt Abschluss, rufen Sie [IMAPITable::GetStatus](imapitable-getstatus.md).
  
Ein Aufruf von **SetColumns** zurück MAPI_E_BUSY, was bedeutet, dass ein anderer Vorgang den Vorgang gestartet wird, verhindert können Sie [IMAPITable::Abort](imapitable-abort.md) , um den Vorgang in Arbeit abzubrechen aufrufen. 
  
Sie können auch [HrAddColumnsEx](hraddcolumnsex.md) zum Ändern einer Spalte aufrufen. Der Unterschied zwischen **HrAddColumnsEx** und **IMAPITable::SetColumns** ist, dass **HrAddColumnsEx** weniger flexibel ist. Es kann nur Spalten hinzufügen. Am Anfang des Satzes Spalte werden die zusätzlichen Spalten angeordnet. nach dieser Spalten werden alle vorhandene Spalten angezeigt. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoSetColumns  <br/> |MFCMAPI (engl.) verwendet die **IMAPITable::SetColumns** -Methode, um die gewünschten Spalten für die Tabelle festgelegt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[HrQueryAllRows](hrqueryallrows.md)
  
[IMAPITable::Abort](imapitable-abort.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[Methode IMAPITable:: Restrict](imapitable-restrict.md)
  
[SortTable](imapitable-sorttable.md)
  
[SPropTagArray](sproptagarray.md)
  
[SPropValue](spropvalue.md)
  
[' Srowset '](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

