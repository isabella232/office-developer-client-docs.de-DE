---
title: IMAPIProgressGetMin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMin
api_type:
- COM
ms.assetid: caceddf1-0f7c-47b5-97bf-17ffe3440a6c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ab92aee6a8254a16c48352e371b711932bbe7427
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792259"
---
# <a name="imapiprogressgetmin"></a>IMAPIProgress::GetMin

  
  
**Betrifft**: Outlook 
  
Gibt den kleinsten Wert in der [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) -Methode für die Fortschritt Informationen angezeigt werden. 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a>Parameter

 _lpulMin_
  
> [out] Ein Zeiger auf die minimale Anzahl von Elementen in den Vorgang.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die minimale Anzahl von Elementen in der Vorgang wurde abgerufen.
    
## <a name="remarks"></a>Bemerkungen

Der Mindestwert stellt den Anfang des Vorgangs in numerische Form dar. Der Wert kann einen globalen Höchstwert zur Darstellung des Bereichs der gesamte Fortschrittsanzeige oder ein lokaler Wert, der zum Darstellen eines Teils der Anzeige sein. 
  
Der Wert der Einstellung Flag bestimmt, ob das Objekt Fortschritt den Mindestwert lokal oder global sein versteht. Wenn das Flag MAPI_TOP_LEVEL festgelegt ist, wird der Mindestwert gilt als globale und wird verwendet, um den Status für den gesamten Vorgang zu berechnen. Wenn MAPI_TOP_LEVEL nicht festgelegt ist, gilt der Mindestwert lokalen und Anbieter mit es intern Fortschritt für unteren Ebene Unterobjekte angezeigt werden sollen. Fortschritt Objekte speichern den lokalen Mindestwert nur, um einen Anbieter durch einen Aufruf **GetMin** wiederherzustellen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Initialisieren Sie den kleinsten Wert auf 1. Dienstanbieter können durch Aufrufen der Methode **IMAPIProgress::SetLimits** dieser Wert zurückgesetzt. Weitere Informationen zum Implementieren von **GetMin** und anderen [IMAPIProgress](imapiprogressiunknown.md) Methoden finden Sie unter [Implementieren einer Statusanzeige](implementing-a-progress-indicator.md).
  
Weitere Informationen dazu, wie und wann ein Fortschritt-Objekt aufrufen finden Sie unter [Display eine Statusanzeige](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMin  <br/> |MFCMAPI (engl.) verwendet die **IMAPIProgress::GetMin** -Methode, um den kleinsten Wert für die Statusanzeige zu erhalten. Gibt 1 zurück, es sei denn, Grenzwerte zuvor durch Aufrufen der Methode **IMAPIProgress::SetLimits** festgelegt wurden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md)
  
[Implementieren eines Statusindikators](implementing-a-progress-indicator.md)

