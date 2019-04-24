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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0810ed7ce20bba95c4286e6e042065c0c2d1a802
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339865"
---
# <a name="imapiprogresssetlimits"></a>IMAPIProgress::SetLimits

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt die unteren und oberen Grenzwerte für die Anzahl der Elemente in dem Vorgang sowie die Flags fest, die Steuern, wie Fortschrittsinformationen für den Vorgang berechnet werden.
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulMin_
  
> in Ein Zeiger auf eine Variable, die den unteren Grenzwert von Elementen in dem Vorgang enthält.
    
 _lpulMax_
  
> in Ein Zeiger auf eine Variable, die die obere Grenze der Elemente in dem Vorgang enthält.
    
 _lpulFlags_
  
> in Eine Bitmaske von Flags, die die Vorgangsebene steuert, auf der die Statusinformationen berechnet werden. Das folgende Flag kann festgelegt werden:
    
MAPI_TOP_LEVEL 
  
> Verwendet die Werte in den Parametern _ulCount_ und _ulTotal_ der [IMAPIProgress::P rogress](imapiprogress-progress.md) -Methode, die das aktuell verarbeitete Element und die gesamten Elemente angeben, um den Fortschritt des Vorgangs zu erhöhen. Wenn dieses Flag festgelegt ist, müssen die Werte der globalen unteren und oberen Grenzen festgelegt werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Dienstanbieter rufen die **IMAPIProgress::** setlimits-Methode auf, um das MAPI_TOP_LEVEL-Flag festzulegen oder zu löschen und lokale und globale Mindest-und Maximalwerte festzulegen. Der Wert der Flag-Einstellung wirkt sich darauf aus, ob das Progress-Objekt den minimal-und Maximalwert für "lokal" oder "Global" versteht. Wenn das MAPI_TOP_LEVEL-Flag festgelegt ist, werden diese Werte als Global betrachtet und zum Berechnen des Fortschritts für den gesamten Vorgang verwendet. Progress-Objekte initialisieren den globalen Minimalwert auf 1 und den globalen Maximalwert auf 1000. 
  
Wenn MAPI_TOP_LEVEL nicht festgelegt ist, werden die minimal-und Maximalwerte als lokal betrachtet, und Anbieter verwenden Sie intern, um den Fortschritt für unter Objekte auf niedrigerer Ebene anzuzeigen. Progress-Objekte speichern die lokalen Mindest-und Maximalwerte nur, damit Sie an Anbieter zurückgegeben werden können, wenn die [IMAPIProgress:: GetMin](imapiprogress-getmin.md) und [IMAPIProgress:: GetMax](imapiprogress-getmax.md) -Methoden aufgerufen werden. 
  
Weitere Informationen zum Implementieren von setLimits und den anderen [IMAPIProgress](imapiprogressiunknown.md) -Methoden finden Sie unter [Implementieren einer Statusanzeige](implementing-a-progress-indicator.md). ****
  
Weitere Informationen dazu, wie und wann Statusobjekte aufgerufen werden, finden Sie unter [Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Kommentar**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress:: setLimits  <br/> |MFCMAPI verwendet die **IMAPIProgress::** setlimits-Methode, um die maximal-und minimal Grenzwerte und-Flags für das Progress-Objekt festzulegen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md)
  
[Implementieren eines Statusindikators](implementing-a-progress-indicator.md)

