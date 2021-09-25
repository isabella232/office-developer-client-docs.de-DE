---
title: IMAPIProgressGetMax
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProgress.GetMax
api_type:
- COM
ms.assetid: 88a910ed-b55a-4e5b-a43d-eb3ea795a70e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1a56ad2d5cd1753b9ed07352174855c28ba373ae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564162"
---
# <a name="imapiprogressgetmax"></a>IMAPIProgress::GetMax

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die maximale Anzahl von Elementen in dem Vorgang zurück, für die Statusinformationen angezeigt werden.
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a>Parameter

 _lpulMax_
  
> [out] Ein Zeiger auf die maximale Anzahl von Elementen im Vorgang.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die maximale Anzahl von Elementen in dem Vorgang wurde abgerufen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Der Maximalwert stellt das Ende des Vorgangs in numerischer Form dar. Der Wert kann ein globaler Maximalwert sein, der verwendet wird, um den Umfang der gesamten Statusanzeige darzustellen, oder ein lokaler Wert, der zum Darstellen eines Teils der Anzeige verwendet wird. 
  
Der Wert der Kennzeicheneinstellung wirkt sich darauf aus, ob das Statusobjekt den maximalen Wert als lokal oder global versteht. Wenn das flag MAPI_TOP_LEVEL festgelegt ist, wird der Maximalwert als global betrachtet und zum Berechnen des Fortschritts für den gesamten Vorgang verwendet. Wenn MAPI_TOP_LEVEL nicht festgelegt ist, wird der Maximalwert als lokal betrachtet, und Anbieter verwenden ihn intern, um den Fortschritt für untergeordnete Objekte auf niedrigerer Ebene anzuzeigen. Statusobjekte speichern den lokalen Maximalwert nur, um ihn über einen **GetMax-Aufruf** an einen Anbieter zurückzugeben. 
  
Weitere Informationen dazu, wie und wann Statusobjekte aufgerufen werden, finden Sie unter [Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md).
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Initialisieren Sie den Maximalwert auf 1000. Dienstanbieter können diesen Wert durch Aufrufen der [IMAPIProgress::SetLimits](imapiprogress-setlimits.md)-Methode zurücksetzen. Weitere Informationen zum Implementieren von **GetMax** und den anderen [IMAPIProgress-Methoden](imapiprogressiunknown.md) finden Sie unter [Implementieren einer Statusanzeige.](implementing-a-progress-indicator.md)
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Kommentar**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMax  <br/> |MFCMAPI verwendet die **IMAPIProgress::GetMax-Methode,** um den Maximalwert für das Statusobjekt abzurufen. Gibt 1000 zurück, es sei denn, mit der **IMAPIProgress::SetLimits-Methode** wurden zuvor Grenzwerte festgelegt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md)
  
[Implementieren eines Statusindikators](implementing-a-progress-indicator.md)

