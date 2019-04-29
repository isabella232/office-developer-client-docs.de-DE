---
title: IMAPITableGetRowCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetRowCount
api_type:
- COM
ms.assetid: 44a12c92-7462-4acf-9520-5d4c2d7f1d47
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b13bf3bdd8392efc42ad189e48dffad8636f0708
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425603"
---
# <a name="imapitablegetrowcount"></a>IMAPITable::GetRowCount

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Gesamtanzahl der Zeilen in der Tabelle zurück. 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> Reserviert muss NULL sein.
    
 _lpulCount_
  
> Out Zeiger auf die Anzahl der Zeilen in der Tabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeilenanzahl wurde erfolgreich zurückgegeben.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Abrufvorgang für die Zeilenanzahl gestartet wird. Entweder sollte der ausgeführte Vorgang abgeschlossen oder beendet werden.
    
MAPI_E_NO_SUPPORT 
  
> Die Tabelle kann die Anzahl der Zeilen nicht berechnen.
    
MAPI_W_APPROX_COUNT 
  
> Der Aufruf war erfolgreich, aber eine ungefähre Zeilenanzahl wurde zurückgegeben, da die genaue Zeilenanzahl aufgrund von Arbeitsspeichereinschränkungen nicht bestimmt werden konnte. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro. Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable:: GetRowCount** -Methode ruft die Gesamtanzahl der Zeilen in einer Tabelle ab. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn Sie die genaue Zeilenanzahl der Tabelle nicht bestimmen können, geben Sie MAPI_W_APPROX_COUNT und eine ungefähre Zeilenanzahl im Inhalt des _lpulCount_ -Parameters zurück. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Verwenden **** Sie GetRowCount, um herauszufinden, wie viele Zeilen eine Tabelle enthält, bevor Sie die [IMAPITable:: QueryRows](imapitable-queryrows.md) -Methode aufrufen, um die Daten abzurufen. Wenn die Tabelle weniger als zwanzig Zeilen enthält, können Sie **QueryPosition** aufrufen, um die gesamte Tabelle abzurufen. Wenn in der Tabelle mehr als zwanzig Zeilen vorhanden sind, sollten Sie mehrere Aufrufe an **QueryPosition** durchführen und die Anzahl der in jedem Aufruf abgerufenen Zeilen begrenzen. 
  
Einige Tabellen unterstützen **GetRowCount** nicht und geben MAPI_E_NO_SUPPORT zurück. Wenn **GetRowCount** nicht unterstützt wird, können Sie [IMAPITable:: QueryPosition](imapitable-queryposition.md)aufrufen. Mit den Ergebnissen aus **QueryPosition**können Sie die Beziehung zwischen der aktuellen Zeile und der letzten Zeile bestimmen. 
  
Wenn **GetRowCount** MAPI_E_BUSY zurückgibt, da es vorübergehend nicht in der Lage ist, eine Zeilenanzahl abzurufen, rufen Sie die [IMAPITable:: WaitForCompletion](imapitable-waitforcompletion.md) -Methode auf. Wiederholen Sie den Aufruf von getRowCount, **** Wenn **WaitForCompletion** zurückgegeben wird. Sie können auch feststellen, ob eine asynchrone Operation ausgeführt wird, indem Sie die [IMAPITable:: GetStatus](imapitable-getstatus.md) -Methode aufrufen und den Inhalt des _lpulTableState_ -Parameters überprüfen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |CopyFolderContents  <br/> |MFCMAPI verwendet die **IMAPITable:: GetRowCount** -Methode, um zu bestimmen, wie viele Zeilen sich in der Quelltabelle befinden, damit der Arbeitsspeicher für die Kopie reserviert werden kann.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::QueryPosition](imapitable-queryposition.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

