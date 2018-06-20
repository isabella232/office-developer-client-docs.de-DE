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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 96fd317c28d95335a3acc5d0603298f2fe8345e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792467"
---
# <a name="imapitablequerycolumns"></a>IMAPITable::QueryColumns

  
  
**Betrifft**: Outlook 
  
Gibt eine Liste mit Spalten für die Tabelle zurück.
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Bitmaske aus Flags, die angibt, welche Spalte festlegen sollten zurückgegeben werden. Das folgende Flag kann festgelegt werden:
    
TBL_ALL_COLUMNS 
  
> Die Tabelle sollte alle Verfügbare Spalten zurückgegeben.
    
 _lpPropTagArray_
  
> [out] Legen Sie den Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die die Eigenschaftentags für die Spalte enthält. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Spalte wurde erfolgreich zurückgegeben.
    
MAPI_E_BUSY 
  
> Ein anderer Vorgang wird ausgeführt, die verhindert, die Spalte dass Abrufvorgang starten festgelegt. Entweder dürfen der Vorgang in Arbeit abgeschlossen oder angehalten werden sollte.
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::QueryColumns** -Methode kann EntityInstances abgerufen werden: 
  
- Die Standardspalte für eine Tabelle festlegen.
    
- Der aktuellen Spalte für eine Tabelle festlegen, wie durch einen Aufruf an die [IMAPITable::SetColumns](imapitable-setcolumns.md) -Methode festgelegt. 
    
- Die vollständige Spalte für eine Tabelle, die Spalten, die verfügbar sind, aber nicht unbedingt Teil der aktuellen Gruppe festgelegt.
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie nicht das TBL_ALL_COLUMNS-Flag festlegen, gibt **IMAPITable::QueryColumns** eine Tabelle Standard oder aktuellen Spalte festgelegt, je nachdem, ob die Tabelle durch einen Aufruf von **IMAPITable::SetColumns**betroffen ist. **SetColumns** ändert die Reihenfolge und Auswahl von Spalten in einer Tabelle Spalte festlegen. 
  
Wenn Sie das TBL_ALL_COLUMNS-Flag festlegen, gibt **QueryColumns** alle Spalten, die in der Tabelle Spalte festlegen, sondern können. 
  
Freigeben des Speichers für die Array-Tag-Eigenschaft durch den Parameter _LpPropTagArray_ auf das durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoSetColumns  <br/> |MFCMAPI (engl.) verwendet die **IMAPITable::QueryColumns** -Methode zum Abrufen der aktuellen Spalte für eine Tabelle festlegen, sodass der Benutzer bearbeitet werden kann.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

