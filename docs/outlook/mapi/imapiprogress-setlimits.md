---
title: IMAPIProgressSetLimits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProgress.SetLimits
api_type:
- COM
ms.assetid: 63c9e316-ee53-4065-8154-449639643ff7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 91b12f28493cc443d71837a45b6bab9b988697d9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613912"
---
# <a name="imapiprogresssetlimits"></a>IMAPIProgress::SetLimits

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt die unteren und oberen Grenzwerte für die Anzahl der Elemente im Vorgang und die Flags fest, die steuern, wie Statusinformationen für den Vorgang berechnet werden.
  
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
  
> [in] Ein Zeiger auf eine Variable, die die Obergrenze der Elemente im Vorgang enthält.
    
 _lpulFlags_
  
> [in] Eine Bitmaske mit Flags, die die Vorgangsebene steuert, auf der Statusinformationen berechnet werden. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_TOP_LEVEL 
  
> Verwendet die Werte in den _UlCount-_ und _ulTotal-Parametern_ der [IMAPIProgress::P Rogress-Methode,](imapiprogress-progress.md) die das aktuell verarbeitete Element bzw. die Gesamtelemente angeben, um den Fortschritt des Vorgangs zu erhöhen. Wenn dieses Kennzeichen festgelegt ist, müssen die Werte der globalen unteren und oberen Grenzwerte festgelegt werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Dienstanbieter rufen die **IMAPIProgress::SetLimits-Methode** auf, um das MAPI_TOP_LEVEL-Flag festzulegen oder zu löschen und lokale und globale Mindest- und Höchstwerte festzulegen. Der Wert der Flageinstellung wirkt sich darauf aus, ob das Statusobjekt die minimalen und maximalen Werte als lokal oder global versteht. Wenn das flag MAPI_TOP_LEVEL festgelegt ist, werden diese Werte als global betrachtet und zum Berechnen des Fortschritts für den gesamten Vorgang verwendet. Statusobjekte initialisieren den globalen Minimalwert auf 1 und den globalen Maximalwert auf 1000. 
  
Wenn MAPI_TOP_LEVEL nicht festgelegt ist, werden die Mindest- und Höchstwerte als lokal betrachtet, und Anbieter verwenden sie intern, um den Fortschritt für untergeordnete Objekte auf niedrigerer Ebene anzuzeigen. Statusobjekte speichern nur die lokalen Mindest- und Höchstwerte, sodass sie an Anbieter zurückgegeben werden können, wenn die Methoden [IMAPIProgress::GetMin](imapiprogress-getmin.md) und [IMAPIProgress::GetMax](imapiprogress-getmax.md) aufgerufen werden. 
  
Weitere Informationen zum Implementieren von **SetLimits** und anderen [IMAPIProgress-Methoden](imapiprogressiunknown.md) finden Sie unter [Implementieren einer Statusanzeige.](implementing-a-progress-indicator.md)
  
Weitere Informationen dazu, wie und wann Statusobjekte aufgerufen werden, finden Sie unter [Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Kommentar**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::SetLimits  <br/> |MFCMAPI verwendet die **IMAPIProgress::SetLimits-Methode,** um die höchst- und minimalen Grenzwerte und Flags für das Statusobjekt festzulegen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md)
  
[Implementieren eines Statusindikators](implementing-a-progress-indicator.md)

