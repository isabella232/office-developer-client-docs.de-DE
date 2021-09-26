---
title: IMAPIProgressGetMin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProgress.GetMin
api_type:
- COM
ms.assetid: caceddf1-0f7c-47b5-97bf-17ffe3440a6c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 288c25e5dad204e0c5351c675c95d11c8ba497b0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620975"
---
# <a name="imapiprogressgetmin"></a>IMAPIProgress::GetMin

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Mindestwert in der [IMAPIProgress::SetLimits](imapiprogress-setlimits.md)-Methode an, für die Statusinformationen angezeigt werden. 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a>Parameter

 _lpulMin_
  
> [out] Ein Verweis auf die minimale Anzahl von Elementen in dem Vorgang.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die minimale Anzahl von Elementen in dem Vorgang wurde abgerufen.
    
## <a name="remarks"></a>Hinweise

Der Mindestwert stellt den Beginn des Vorgangs in numerischer Form dar. Der Wert kann ein globaler Maximalwert sein, der verwendet wird, um den Umfang der gesamten Statusanzeige darzustellen, oder ein lokaler Wert, der zum Darstellen eines Teils der Anzeige verwendet wird. 
  
Der Wert der Flageinstellung wirkt sich darauf aus, ob das Statusobjekt versteht, dass der Mindestwert lokal oder global ist. Wenn das MAPI_TOP_LEVEL-Flag festgelegt ist, wird der Mindestwert als global betrachtet und zum Berechnen des Status für den gesamten Vorgang verwendet. Wenn MAPI_TOP_LEVEL nicht festgelegt ist, wird der Mindestwert als lokal betrachtet und von Anbietern intern verwendet, um den Status von Unterobjekten auf niedrigeren Ebenen anzuzeigen. Statusobjekte speichern den lokalen Mindestwert nur, um diesen an einen Anbieter über einen **GetMin**-Aufruf zurückzugeben. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Initialisieren Sie den Mindestwert auf 1. Dienstanbieter können diesen Wert durch Aufrufen der **IMAPIProgress::SetLimits**-Methode zurücksetzen. Weitere Informationen zum Implementieren von **GetMin** und der anderen [IMAPIProgress](imapiprogressiunknown.md)-Methoden finden Sie unter [Implementieren eines Statusindikators](implementing-a-progress-indicator.md).
  
Weitere Informationen dazu, wie und wann Statusobjekte aufgerufen werden, finden Sie unter [Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Kommentar**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMin  <br/> |MFCMAPI verwendet die **IMAPIProgress::GetMin**-Methode, um den kleinsten Wert für die Statusanzeige abzurufen. Gibt 1 zurück, es sei denn, zuvor wurden durch Aufrufen der **IMAPIProgress::SetLimits**-Methode Einschränkungen festgelegt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md)
  
[Implementieren eines Statusindikators](implementing-a-progress-indicator.md)

