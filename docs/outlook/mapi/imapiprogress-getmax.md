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
ms.openlocfilehash: 2dadad410b9aaf1401d792de373e561c29183a12
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567237"
---
# <a name="imapiprogressgetmax"></a>IMAPIProgress::GetMax

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt die maximale Anzahl von Elementen in den Vorgang für den Fortschritt Informationen angezeigt werden.
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a>Parameter

 _lpulMax_
  
> [out] Ein Zeiger auf die maximale Anzahl von Elementen in den Vorgang.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die maximale Anzahl von Elementen in der Vorgang wurde abgerufen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Der maximale Wert stellt das Ende des Vorgangs in numerische Form dar. Der Wert kann einen globalen Höchstwert zur Darstellung des Bereichs der gesamte Fortschrittsanzeige oder ein lokaler Wert, der zum Darstellen eines Teils der Anzeige sein. 
  
Der Wert der Einstellung Flag wirkt sich auf, ob das Objekt Fortschritt den Höchstwert lokal oder global sein versteht. Wenn das Flag MAPI_TOP_LEVEL festgelegt ist, der maximale Wert gilt als globale und wird verwendet, um den Status für den gesamten Vorgang zu berechnen. Wenn MAPI_TOP_LEVEL nicht festgelegt ist, der maximale Wert gilt als lokale und Anbieter mit es intern Fortschritt für unteren Ebene Unterobjekte angezeigt werden sollen. Fortschritt Objekte speichern den lokalen Höchstwert nur, um einen Anbieter durch einen Aufruf **GetMax** wiederherzustellen. 
  
Weitere Informationen dazu, wie und wann ein Fortschritt-Objekt aufrufen finden Sie unter [Display eine Statusanzeige](how-to-display-a-progress-indicator.md).
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Initialisieren Sie den Höchstwert bis 1000 ein. Dienstanbieter können durch Aufrufen der Methode [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) dieser Wert zurückgesetzt. Weitere Informationen zum Implementieren von **GetMax** und anderen [IMAPIProgress](imapiprogressiunknown.md) Methoden finden Sie unter [Implementieren einer Statusanzeige](implementing-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMax  <br/> |MFCMAPI (engl.) verwendet die **IMAPIProgress::GetMax** -Methode, um den Höchstwert für den Fortschritt-Objekt abzurufen. Gibt 1000 zurück, es sei denn, Grenzwerte zuvor mit der **IMAPIProgress::SetLimits** -Methode festgelegt wurden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md)
  
[Implementieren eines Statusindikators](implementing-a-progress-indicator.md)

