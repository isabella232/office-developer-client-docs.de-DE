---
title: IMAPIProgressGetMax
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMax
api_type:
- COM
ms.assetid: 88a910ed-b55a-4e5b-a43d-eb3ea795a70e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 64b6235151c7700a24992bc1d4394553a53c0464
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436202"
---
# <a name="imapiprogressgetmax"></a>IMAPIProgress::GetMax

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die maximale Anzahl von Elementen im Vorgang zurück, für die Statusinformationen angezeigt werden.
  
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
  
> Die maximale Anzahl von Elementen im Vorgang wurde abgerufen.
    
## <a name="remarks"></a>Hinweise

Der Maximalwert stellt das Ende des Vorgangs in numerischer Form dar. Der Wert kann ein globaler Maximalwert sein, der verwendet wird, um den Umfang der gesamten Statusanzeige darzustellen, oder ein lokaler Wert, der zum Darstellen eines Teils der Anzeige verwendet wird. 
  
Der Wert der Kennzeicheneinstellung wirkt sich darauf aus, ob das progress-Objekt den maximalen Wert als lokal oder global versteht. Wenn das MAPI_TOP_LEVEL festgelegt ist, wird der maximal zulässige Wert als global betrachtet und zum Berechnen des Fortschritts für den gesamten Vorgang verwendet. Wenn MAPI_TOP_LEVEL festgelegt ist, wird der maximal zulässige Wert als lokal betrachtet, und Anbieter verwenden ihn intern, um den Fortschritt für Unterobjekte auf niedrigerer Ebene anzeigen zu können. Progress-Objekte speichern den lokalen Maximalwert nur, um ihn über einen **GetMax-Aufruf** an einen Anbieter zurückzukehren. 
  
Weitere Informationen dazu, wie und wann Statusobjekte aufgerufen werden, finden Sie unter [Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md).
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Initialisieren Sie den Maximalwert auf 1000. Dienstanbieter können diesen Wert durch Aufrufen der [IMAPIProgress::SetLimits](imapiprogress-setlimits.md)-Methode zurücksetzen. Weitere Informationen zum Implementieren von **GetMax** und den anderen [IMAPIProgress-Methoden](imapiprogressiunknown.md) finden Sie unter [Implementing a Progress Indicator](implementing-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Kommentar**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMax  <br/> |MFCMAPI verwendet die **IMAPIProgress::GetMax-Methode,** um den maximalen Wert für das Progress-Objekt zu erhalten. Gibt 1000 zurück, es sei denn, mit der **IMAPIProgress::SetLimits-Methode** wurden zuvor Grenzwerte festgelegt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md)
  
[Implementieren eines Statusindikators](implementing-a-progress-indicator.md)

