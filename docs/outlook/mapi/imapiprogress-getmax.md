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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 64b6235151c7700a24992bc1d4394553a53c0464
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270203"
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
  
> Out Ein Zeiger auf die maximale Anzahl von Elementen in dem Vorgang.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die maximale Anzahl von Elementen in dem Vorgang wurde abgerufen.
    
## <a name="remarks"></a>Bemerkungen

Der Maximalwert stellt das Ende des Vorgangs in numerischer Form dar. Der Wert kann ein globaler Maximalwert sein, der verwendet wird, um den Umfang der gesamten Statusanzeige darzustellen, oder ein lokaler Wert, der zum Darstellen eines Teils der Anzeige verwendet wird. 
  
Der Wert der Flag-Einstellung wirkt sich darauf aus, ob das Progress-Objekt den Maximalwert auf "lokal" oder "Global" versteht. Wenn das MAPI_TOP_LEVEL-Flag festgelegt ist, wird der Höchstwert als Global betrachtet und zum Berechnen des Fortschritts für den gesamten Vorgang verwendet. Wenn MAPI_TOP_LEVEL nicht festgelegt ist, wird der Maximalwert als lokal betrachtet, und die Anbieter verwenden ihn intern, um den Fortschritt für unter Objekte auf niedrigerer Ebene anzuzeigen. Progress-Objekte speichern den lokalen Maximalwert nur, um ihn über einen **GetMax** -Aufruf an einen Anbieter zurückzugeben. 
  
Weitere Informationen dazu, wie und wann Statusobjekte aufgerufen werden, finden Sie unter [Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md).
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Initialisieren Sie den Höchstwert auf 1000. Dienstanbieter können diesen Wert durch Aufrufen der [IMAPIProgress::SetLimits](imapiprogress-setlimits.md)-Methode zurücksetzen. Weitere Informationen zum Implementieren von **GetMax** und den anderen [IMAPIProgress](imapiprogressiunknown.md) -Methoden finden Sie unter [Implementieren einer Statusanzeige](implementing-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Kommentar**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress:: GetMax  <br/> |MFCMAPI verwendet die **IMAPIProgress:: GetMax** -Methode, um den Maximalwert für das Progress-Objekt abzurufen. Gibt 1000 zurück, es sei denn, es wurden zuvor Werte mit der **IMAPIProgress::** setlimits-Methode festgelegt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md)
  
[Implementieren eines Statusindikators](implementing-a-progress-indicator.md)

