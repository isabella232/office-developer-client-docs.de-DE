---
title: IMAPITableQueryColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryColumns
api_type:
- COM
ms.assetid: d6341acc-c6ca-4605-93af-77230040339d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d142e19fc4721cec4dde0df7fc030a001121da63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410105"
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
  
> [in] Bitmaske von Flags, die angibt, welcher Spaltensatz zurückgegeben werden soll. Das folgende Flag kann festgelegt werden:
    
TBL_ALL_COLUMNS 
  
> Die Tabelle sollte alle verfügbaren Spalten zurückgeben.
    
 _lpPropTagArray_
  
> [out] Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die die Eigenschaftstags für den Spaltensatz enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Spaltensatz wurde erfolgreich zurückgegeben.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Spaltensatzabrufvorgang gestartet wird. Der ausgeführte Vorgang sollte entweder abgeschlossen oder beendet werden.
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::QueryColumns-Methode** kann aufgerufen werden, um: 
  
- Der Standardspaltensatz für eine Tabelle.
    
- Die aktuelle Spalte, die für eine Tabelle festgelegt ist, wie sie durch einen Aufruf der [IMAPITable::SetColumns-Methode festgelegt](imapitable-setcolumns.md) wurde. 
    
- Der vollständige Spaltensatz für eine Tabelle, die spalten, die verfügbar sind, aber nicht unbedingt Teil der aktuellen Gruppe sind.
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie das flag TBL_ALL_COLUMNS nicht festlegen, gibt **IMAPITable::QueryColumns** entweder den Standard- oder aktuellen Spaltensatz einer Tabelle zurück, je nachdem, ob die Tabelle durch einen Aufruf von **IMAPITable::SetColumns** beeinflusst wurde. **SetColumns** ändert die Reihenfolge und Auswahl von Spalten im Spaltensatz einer Tabelle. 
  
Wenn Sie das TBL_ALL_COLUMNS festlegen, gibt **QueryColumns** alle Spalten zurück, die im Spaltensatz der Tabelle enthalten sein können. 
  
Gibt den Arbeitsspeicher für das Eigenschaftentagarray frei, auf das der  _lpPropTagArray-Parameter_ verweist, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oSetColumns  <br/> |MFCMAPI verwendet die **IMAPITable::QueryColumns-Methode,** um den aktuellen Spaltensatz für eine Tabelle abzurufen, damit der Benutzer ihn bearbeiten kann.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

