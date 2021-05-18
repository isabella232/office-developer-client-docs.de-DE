---
title: IMAPIProgressSetLimits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.SetLimits
api_type:
- COM
ms.assetid: 63c9e316-ee53-4065-8154-449639643ff7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0810ed7ce20bba95c4286e6e042065c0c2d1a802
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421466"
---
# <a name="imapiprogresssetlimits"></a>IMAPIProgress::SetLimits

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt die unteren und oberen Grenzwerte für die Anzahl der Elemente im Vorgang und die Flags fest, die steuern, wie Fortschrittsinformationen für den Vorgang berechnet werden.
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulMin_
  
> [in] Ein Zeiger auf eine Variable, die die untere Grenze der Elemente im Vorgang enthält.
    
 _lpulMax_
  
> [in] Ein Zeiger auf eine Variable, die die obere Grenze der Elemente im Vorgang enthält.
    
 _lpulFlags_
  
> [in] Eine Bitmaske mit Flags, die die Vorgangsebene steuert, auf der Fortschrittsinformationen berechnet werden. Das folgende Flag kann festgelegt werden:
    
MAPI_TOP_LEVEL 
  
> Verwendet die Werte in den _UlCount-_ und _ulTotal-Parametern_ der [IMAPIProgress::P rogress-Methode,](imapiprogress-progress.md) die das aktuell verarbeitete Element bzw. die Gesamtelemente angeben, um den Fortschritt des Vorgangs zu erhöhen. Wenn dieses Flag festgelegt ist, müssen die Werte der globalen unteren und oberen Grenzwerte festgelegt werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Dienstanbieter rufen die **IMAPIProgress::SetLimits-Methode** auf, um das flag MAPI_TOP_LEVEL und lokale und globale Mindest- und Höchstwerte zu setzen oder zu löschen. Der Wert der Flageinstellung wirkt sich darauf aus, ob das progress-Objekt die minimalen und maximalen Werte als lokal oder global versteht. Wenn das MAPI_TOP_LEVEL festgelegt ist, werden diese Werte als global betrachtet und zur Berechnung des Fortschritts für den gesamten Vorgang verwendet. Progress-Objekte initialisieren den globalen Minimalwert auf 1 und den globalen Maximalwert auf 1000. 
  
Wenn MAPI_TOP_LEVEL festgelegt ist, werden die Mindest- und Höchstwerte als lokal betrachtet, und Anbieter verwenden sie intern, um den Fortschritt für Unterobjekte auf niedrigerer Ebene zu anzeigen. Progress-Objekte speichern nur die lokalen Minimal- und Maximalwerte, sodass sie an Anbieter zurückgegeben werden können, wenn die [Methoden IMAPIProgress::GetMin](imapiprogress-getmin.md) und [IMAPIProgress::GetMax](imapiprogress-getmax.md) aufgerufen werden. 
  
Weitere Informationen zum Implementieren von **SetLimits** und den anderen [IMAPIProgress-Methoden](imapiprogressiunknown.md) finden Sie unter [Implementing a Progress Indicator](implementing-a-progress-indicator.md).
  
Weitere Informationen dazu, wie und wann Statusobjekte aufgerufen werden, finden Sie unter [Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Kommentar**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::SetLimits  <br/> |MFCMAPI verwendet die **IMAPIProgress::SetLimits-Methode,** um die maximalen und minimalen Grenzwerte und Flags für das Progress-Objekt zu festlegen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md)
  
[Implementieren eines Statusindikators](implementing-a-progress-indicator.md)

