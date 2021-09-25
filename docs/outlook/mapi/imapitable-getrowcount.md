---
title: IMAPITableGetRowCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.GetRowCount
api_type:
- COM
ms.assetid: 44a12c92-7462-4acf-9520-5d4c2d7f1d47
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ebb926c340b194aae06bb057edf5a4bd1efe20ea
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630649"
---
# <a name="imapitablegetrowcount"></a>IMAPITable::GetRowCount

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Gesamtzahl der Zeilen in der Tabelle zurück. 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> Reserviert; muss Null sein.
    
 _lpulCount_
  
> [out] Zeiger auf die Anzahl der Zeilen in der Tabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeilenanzahl wurde erfolgreich zurückgegeben.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Vorgang zum Abrufen der Zeilenanzahl gestartet wird. Entweder sollte der laufende Vorgang abgeschlossen werden können, oder er sollte beendet werden.
    
MAPI_E_NO_SUPPORT 
  
> Die Tabelle kann die Anzahl der Zeilen nicht berechnen.
    
MAPI_W_APPROX_COUNT 
  
> Der Aufruf war erfolgreich, es wurde jedoch eine ungefähre Zeilenanzahl zurückgegeben, da die genaue Zeilenanzahl aufgrund von Speichereinschränkungen möglicherweise nicht ermittelt werden konnte. Verwenden Sie das Makro **HR_FAILED, um** diese Warnung zu testen. Informationen zur Fehlerbehandlung finden Sie unter [Verwenden von Makros.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable::GetRowCount-Methode** ruft die Gesamtzahl der Zeilen in einer Tabelle ab. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn Sie die genaue Zeilenanzahl der Tabelle nicht ermitteln können, geben Sie MAPI_W_APPROX_COUNT und eine ungefähre Zeilenanzahl im Inhalt des  _lpulCount-Parameters_ zurück. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Verwenden Sie **GetRowCount,** um herauszufinden, wie viele Zeilen eine Tabelle enthält, bevor Sie die [IMAPITable::QueryRows-Methode](imapitable-queryrows.md) aufrufen, um die Daten abzurufen. Wenn weniger als 20 Zeilen in der Tabelle vorhanden sind, ist es sicher, **QueryPosition** aufzurufen, um die gesamte Tabelle abzurufen. Wenn mehr als 20 Zeilen in der Tabelle vorhanden sind, sollten Sie mehrere Aufrufe von **QueryPosition** durchführen und die Anzahl der in jedem Aufruf abgerufenen Zeilen begrenzen. 
  
Einige Tabellen unterstützen **GetRowCount** nicht und geben MAPI_E_NO_SUPPORT zurück. Wenn **GetRowCount** nicht unterstützt wird, besteht eine Alternative möglicherweise darin, [IMAPITable::QueryPosition](imapitable-queryposition.md)aufzurufen. Mit den Ergebnissen aus **QueryPosition** können Sie die Beziehung zwischen der aktuellen Zeile und der letzten Zeile bestimmen. 
  
Wenn **GetRowCount** MAPI_E_BUSY zurückgibt, weil es vorübergehend keine Zeilenanzahl abrufen kann, rufen Sie die [IMAPITable::WaitForCompletion-Methode](imapitable-waitforcompletion.md) auf. Wenn **WaitForCompletion** zurückgegeben wird, wiederholen Sie den Aufruf von **GetRowCount**. Eine weitere Möglichkeit zum Erkennen, ob ein asynchroner Vorgang ausgeführt wird, besteht darin, die [IMAPITable::GetStatus-Methode](imapitable-getstatus.md) aufzurufen und den Inhalt des  _lpulTableState-Parameters_ zu überprüfen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyFolderContents  <br/> |MFCMAPI verwendet die **IMAPITable::GetRowCount-Methode,** um zu bestimmen, wie viele Zeilen sich in der Quelltabelle befinden, damit Speicher zum Ausführen der Kopie zugewiesen werden kann.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::QueryPosition](imapitable-queryposition.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

