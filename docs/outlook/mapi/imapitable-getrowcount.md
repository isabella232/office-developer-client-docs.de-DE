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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a591a49c1cb0ec936d09d59b4632d15e4842dd2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792468"
---
# <a name="imapitablegetrowcount"></a>IMAPITable::GetRowCount

  
  
**Betrifft**: Outlook 
  
Gibt die Gesamtzahl der Zeilen in der Tabelle zurück. 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> Reserviert. NULL muss sein.
    
 _lpulCount_
  
> [out] Zeiger auf die Anzahl der Zeilen in der Tabelle.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Anzahl der Zeilen wurde erfolgreich zurückgegeben.
    
MAPI_E_BUSY 
  
> Ein anderer Vorgang wird ausgeführt, die verhindert, den Vorgang Count Zeile nicht gestartet dass. Entweder dürfen der Vorgang in Arbeit abgeschlossen oder angehalten werden sollte.
    
MAPI_E_NO_SUPPORT 
  
> Die Tabelle kann die Anzahl der Zeilen nicht berechnen.
    
MAPI_W_APPROX_COUNT 
  
> Der Aufruf war erfolgreich, aber eine ungefähre Zeilenanzahl wurde zurückgegeben, da die genaue Zeilenanzahl nicht möglicherweise aufgrund der Speicherkapazität ermittelt werden kann. Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen. Finden Sie unter [Verwendung von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::GetRowCount** -Methode ruft die Gesamtzahl der Zeilen in einer Tabelle ab. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn Sie die Tabelle genauen Zeilenanzahl ermitteln können, zählen return MAPI_W_APPROX_COUNT und eine ungefähre Zeile in den Inhalt des Parameters _LpulCount_ . 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Verwendung **GetRowCount** um zu erfahren, wie viele Zeilen eine Tabelle enthält vor dem tätigen eines Anrufs auf [die QueryRows](imapitable-queryrows.md) zum Abrufen der Daten. Wenn weniger als 20 Zeilen in der Tabelle vorhanden sind, ist es sicherer **QueryPosition** zum Abrufen der gesamten Tabelle aufrufen. Wenn mehr als 20 Zeilen in der Tabelle vorhanden sind, sollten Sie mehrere Aufrufe von **QueryPosition** und die Anzahl der Zeilen, die in jedem Aufruf abgerufen. 
  
Einige Tabellen nicht unterstützen **GetRowCount** und MAPI_E_NO_SUPPORT zurückzugeben. Wenn **GetRowCount** nicht unterstützt wird, möglicherweise eine Alternative [IMAPITable::QueryPosition](imapitable-queryposition.md)aufrufen. Mit den Ergebnissen von **QueryPosition**können Sie die Beziehung zwischen der aktuellen Zeile und die letzte Zeile bestimmen. 
  
Wenn **GetRowCount** MAPI_E_BUSY zurückgegeben, da es vorübergehend nicht zum Abrufen der Zeilenanzahl ist, rufen Sie die [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) -Methode. Wenn **WaitForCompletion** zurückgegeben wird, wiederholen Sie den Anruf an **GetRowCount**. Eine andere Möglichkeit, erkennen, ob eine asynchrone Operation ausgeführt wird, ist die [IMAPITable::GetStatus](imapitable-getstatus.md) -Methode aufrufen, und überprüfen Sie den Inhalt des Parameters _LpulTableState_ . 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyFolderContents  <br/> |MFCMAPI (engl.) verwendet die **IMAPITable::GetRowCount** -Methode, um zu bestimmen, wie viele Zeilen in der Quelltabelle werden, damit Speicher zugewiesen werden kann, um den Kopiervorgang.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::QueryPosition](imapitable-queryposition.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

