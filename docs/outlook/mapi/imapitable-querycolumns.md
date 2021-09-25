---
title: IMAPITableQueryColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.QueryColumns
api_type:
- COM
ms.assetid: d6341acc-c6ca-4605-93af-77230040339d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: edaacf40bac968b98352bf1b2dc19e01b76eb524
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567397"
---
# <a name="imapitablequerycolumns"></a>IMAPITable::QueryColumns

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine Liste der Spalten für die Tabelle zurück.
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Bitmaske mit Flags, die angibt, welcher Spaltensatz zurückgegeben werden soll. Das folgende Kennzeichen kann festgelegt werden:
    
TBL_ALL_COLUMNS 
  
> Die Tabelle sollte alle verfügbaren Spalten zurückgeben.
    
 _lpPropTagArray_
  
> [out] Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die die Eigenschaftentags für den Spaltensatz enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Spaltensatz wurde erfolgreich zurückgegeben.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Abrufvorgang für Spaltengruppen gestartet wird. Entweder sollte der laufende Vorgang abgeschlossen werden können, oder er sollte beendet werden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPITable::QueryColumns-Methode** kann aufgerufen werden, um Folgendes abzurufen: 
  
- Der Standardspaltensatz für eine Tabelle.
    
- Der aktuelle Spaltensatz für eine Tabelle, wie durch einen Aufruf der [IMAPITable::SetColumns-Methode](imapitable-setcolumns.md) festgelegt. 
    
- Der vollständige Spaltensatz für eine Tabelle, die verfügbaren Spalten, aber nicht unbedingt Teil des aktuellen Satzes.
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie das flag TBL_ALL_COLUMNS nicht festlegen, gibt **IMAPITable::QueryColumns** entweder den Standard- oder den aktuellen Spaltensatz einer Tabelle zurück, je nachdem, ob die Tabelle von einem Aufruf von **IMAPITable::SetColumns** betroffen ist. **SetColumns** ändert die Reihenfolge und Auswahl der Spalten im Spaltensatz einer Tabelle. 
  
Wenn Sie das flag TBL_ALL_COLUMNS festlegen, gibt **QueryColumns** alle Spalten zurück, die im Spaltensatz der Tabelle enthalten sein können. 
  
Geben Sie den Speicher für das Eigenschaftentagarray frei, auf das der  _Parameter lpPropTagArray_ verweist, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oSetColumns  <br/> |MFCMAPI verwendet die **IMAPITable::QueryColumns-Methode,** um den aktuellen Spaltensatz für eine Tabelle abzurufen, damit der Benutzer sie bearbeiten kann.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

