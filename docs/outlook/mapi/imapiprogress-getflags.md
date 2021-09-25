---
title: IMAPIProgressGetFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProgress.GetFlags
api_type:
- COM
ms.assetid: 7af74fcc-c0df-4f58-a2d4-0a79c96b2e81
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 186c120d603813a0b692b9a0349ac60adbef76c9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604878"
---
# <a name="imapiprogressgetflags"></a>IMAPIProgress::GetFlags

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt Flageinstellungen aus dem Statusobjekt für die Vorgangsebene zurück, für die Statusinformationen berechnet werden.
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> [out] Eine Bitmaske mit Flags, die die Vorgangsebene steuert, auf der Statusinformationen berechnet werden. Das folgende Flag kann zurückgegeben werden:
    
MAPI_TOP_LEVEL 
  
> Der Fortschritt wird für das Objekt der obersten Ebene berechnet, das objekt, das vom Client aufgerufen wird, um den Vorgang zu starten. Beispielsweise ist das Objekt der obersten Ebene in einem Ordnerkopiervorgang der Ordner, der kopiert wird. Wenn MAPI_TOP_LEVEL nicht festgelegt ist, wird der Fortschritt für ein Objekt der unteren Ebene oder ein Unterobjekt berechnet. Im Ordnerkopiervorgang ist ein Objekt der unteren Ebene einer der Unterordner in dem Ordner, der kopiert wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Flags-Wert wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

MapI ermöglicht es Dienstanbietern, zwischen Objekten der obersten Ebene und Unterobjekten mit dem Flag MAPI_TOP_LEVEL zu unterscheiden, sodass alle an einem Vorgang beteiligten Objekte dieselbe [IMAPIProgress-Implementierung](imapiprogressiunknown.md) verwenden können, um den Fortschritt anzuzeigen. Dadurch wird die Anzeige des Indikators in einer einzigen positiven Richtung reibungslos fortgesetzt. Ob das flag MAPI_TOP_LEVEL festgelegt ist, bestimmt, wie Dienstanbieter die anderen Parameter in nachfolgenden Aufrufen des Statusobjekts festlegen. 
  
Der von **GetFlags** zurückgegebene Wert wird zunächst vom Implementierer und anschließend vom Dienstanbieter über einen Aufruf der [IMAPIProgress::SetLimits-Methode](imapiprogress-setlimits.md) festgelegt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Initialisieren Sie das Flag immer auf MAPI_TOP_LEVEL und verlassen Sie sich dann auf Dienstanbieter, um es ggf. zu löschen. Dienstanbieter können das Flag löschen und zurücksetzen, indem sie die **IMAPIProgress::SetLimits-Methode** aufrufen. Weitere Informationen zum Implementieren von **GetFlags** und den anderen **IMAPIProgress-Methoden** finden Sie unter [Implementieren einer Statusanzeige.](implementing-a-progress-indicator.md)
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie eine Statusanzeige anzeigen, rufen Sie zum ersten Mal **IMAPIProgress auf::GetFlags** auf. Der zurückgegebene Wert sollte MAPI_TOP_LEVEL werden, da alle Implementierungen den Inhalt des  _lpulFlags-Parameters_ auf diesen Wert initialisieren. Weitere Informationen zur Abfolge der Aufrufe eines Statusobjekts finden Sie unter [Anzeigen einer Statusanzeige.](how-to-display-a-progress-indicator.md)
  
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

