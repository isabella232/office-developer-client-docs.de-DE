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
  
> Reserviert; muss null sein.
    
 _lpulCount_
  
> [out] Zeiger auf die Anzahl der Zeilen in der Tabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeilenanzahl wurde erfolgreich zurückgegeben.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Zeilenanzahlabrufvorgang gestartet wird. Der ausgeführte Vorgang sollte entweder abgeschlossen oder beendet werden.
    
MAPI_E_NO_SUPPORT 
  
> Die Anzahl der Zeilen kann in der Tabelle nicht berechnet werden.
    
MAPI_W_APPROX_COUNT 
  
> Der Aufruf war erfolgreich, es wurde jedoch eine ungefähre Zeilenanzahl zurückgegeben, da die genaue Zeilenanzahl möglicherweise aufgrund von Speichereinschränkungen nicht bestimmt werden konnte. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro. Weitere [Informationen finden Sie unter Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::GetRowCount-Methode** ruft die Gesamtanzahl der Zeilen in einer Tabelle ab. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn Sie die genaue Zeilenanzahl der Tabelle nicht ermitteln können, geben MAPI_W_APPROX_COUNT und eine ungefähre Zeilenanzahl im Inhalt des  _lpulCount-Parameters_ zurück. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Verwenden **Sie GetRowCount,** um herauszufinden, wie viele Zeilen eine Tabelle enthält, bevor Sie die [IMAPITable::QueryRows-Methode](imapitable-queryrows.md) aufrufen, um die Daten abzurufen. Wenn die Tabelle weniger als 20 Zeilen enthält, ist es sicher, **QueryPosition zum** Abrufen der gesamten Tabelle auf aufruft. Wenn die Tabelle mehr als 20 Zeilen enthält, sollten Sie mehrere Aufrufe von **QueryPosition** ausführen und die Anzahl der in jedem Aufruf abgerufenen Zeilen begrenzen. 
  
Einige Tabellen unterstützen **GetRowCount nicht und** geben MAPI_E_NO_SUPPORT. Wenn **GetRowCount** nicht unterstützt wird, kann eine Alternative zum Aufrufen von [IMAPITable::QueryPosition sein.](imapitable-queryposition.md) Mit den Ergebnissen von **QueryPosition** können Sie die Beziehung zwischen der aktuellen und der letzten Zeile bestimmen. 
  
Wenn **GetRowCount** MAPI_E_BUSY, da vorübergehend keine Zeilenanzahl abgerufen werden kann, rufen Sie die [IMAPITable::WaitForCompletion-Methode](imapitable-waitforcompletion.md) auf. Wenn **WaitForCompletion zurückgegeben** wird, wiederholen Sie den Aufruf von **GetRowCount**. Eine weitere Möglichkeit, um zu erkennen, ob ein asynchroner Vorgang ausgeführt wird, ist das Aufrufen der [IMAPITable::GetStatus-Methode](imapitable-getstatus.md) und das Überprüfen des Inhalts des _lpulTableState-Parameters._ 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyFolderContents  <br/> |MFCMAPI verwendet die **IMAPITable::GetRowCount-Methode,** um zu bestimmen, wie viele Zeilen sich in der Quelltabelle befinden, damit Arbeitsspeicher zum Ausführen der Kopie zugewiesen werden kann.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::QueryPosition](imapitable-queryposition.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

