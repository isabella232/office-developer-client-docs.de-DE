---
title: IMAPIProgressGetFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetFlags
api_type:
- COM
ms.assetid: 7af74fcc-c0df-4f58-a2d4-0a79c96b2e81
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 810192bfc85c9934a282f02a0839aaed539f744d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423643"
---
# <a name="imapiprogressgetflags"></a>IMAPIProgress::GetFlags

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt Kennzeicheneinstellungen aus dem Progress-Objekt für die Vorgangsebene zurück, auf der Fortschrittsinformationen berechnet werden.
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> [out] Eine Bitmaske mit Flags, die die Vorgangsebene steuert, auf der Fortschrittsinformationen berechnet werden. Das folgende Flag kann zurückgegeben werden:
    
MAPI_TOP_LEVEL 
  
> Der Fortschritt wird für das Objekt auf oberster Ebene berechnet, das vom Client zum Starten des Vorgangs aufgerufen wird. Das Objekt auf oberster Ebene in einem Ordnerkopievorgang ist beispielsweise der Ordner, der kopiert wird. Wenn MAPI_TOP_LEVEL nicht festgelegt ist, wird der Fortschritt für ein Objekt auf niedrigerer Ebene oder für ein Unterobjekt berechnet. Im Ordnerkopievorgang ist ein Objekt der unteren Ebene einer der Unterordner im Ordner, der kopiert wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Flags-Wert wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Hinweise

MIT MAPI können Dienstanbieter mit dem Flag MAPI_TOP_LEVEL zwischen Objekten der obersten Ebene und Unterobjekten unterscheiden, sodass alle an einem Vorgang beteiligten Objekte dieselbe [IMAPIProgress-Implementierung](imapiprogressiunknown.md) verwenden können, um den Fortschritt anzuzeigen. Dies bewirkt, dass die Anzeige des Indikators reibungslos in einer einzigen positiven Richtung fortgesetzt wird. Ob das MAPI_TOP_LEVEL festgelegt ist, bestimmt, wie Dienstanbieter die anderen Parameter in nachfolgenden Aufrufen des Progress-Objekts festlegen. 
  
Der von **GetFlags** zurückgegebene Wert wird zunächst vom Implementier und anschließend vom Dienstanbieter über einen Aufruf der [IMAPIProgress::SetLimits-Methode](imapiprogress-setlimits.md) festgelegt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Initialisieren Sie immer das Flag, MAPI_TOP_LEVEL und verlassen Sie sich dann auf Dienstanbieter, um es zu löschen, wenn dies angemessen ist. Dienstanbieter können das Flag löschen und zurücksetzen, indem sie die **IMAPIProgress::SetLimits-Methode** aufrufen. Weitere Informationen zum Implementieren von **GetFlags** und den anderen **IMAPIProgress-Methoden** finden Sie unter [Implementing a Progress Indicator](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie eine Statusanzeige anzeigen, rufen Sie im ERSTEN Schritt **IMAPIProgress::GetFlags auf.** Der zurückgegebene Wert sollte MAPI_TOP_LEVEL werden, da alle Implementierungen den Inhalt des  _lpulFlags-Parameters_ auf diesen Wert initialisieren. Weitere Informationen zur Reihenfolge der Aufrufe eines Statusobjekts finden Sie [unter Display a Progress Indicator](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Kommentar**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetFlags  <br/> |MFCMAPI verwendet die **IMAPIProgress::GetFlags-Methode,** um zu bestimmen, welche Flags festgelegt werden. Gibt MAPI_TOP_LEVEL zurück, es sei denn, Flags wurden mithilfe der **IMAPIProgress::SetLimits-Methode** festgelegt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md)
  
[Implementieren eines Statusindikators](implementing-a-progress-indicator.md)

