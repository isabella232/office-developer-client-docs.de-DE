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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8964ba8c4341bec431bdbc1690d639b345df8b1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792257"
---
# <a name="imapiprogressgetflags"></a>IMAPIProgress::GetFlags

  
  
**Betrifft**: Outlook 
  
Gibt kennzeichnen Einstellungen aus dem Fortschritt-Objekt für die Ebene des Vorgangs auf die Fortschrittsinformationen berechnet werden.
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> [out] Eine Bitmaske aus Flags, die die Ebene des Vorgangs steuert, welche Fortschritt Informationen berechnet wird. Das folgende Flag können zurückgegeben werden:
    
MAPI_TOP_LEVEL 
  
> Status wird für das Objekt der obersten Ebene, das Objekt berechnet wird, die durch den Client auf die Operation beginnen aufgerufen wird. Beispielsweise ist das Objekt der obersten Ebene in einem Ordnerkopiervorgang den Ordner, der kopiert wird. Wenn MAPI_TOP_LEVEL nicht festgelegt ist, wird für einen niedrigeren Level-Objekt oder Unterobjekts Fortschritt berechnet. In den Ordnerkopiervorgang ist eine niedrigere Level-Objekt eine Unterordner in den Ordner, der kopiert wird.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Wert des Flags wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Hinweise

MAPI-Dienstanbieter zur Unterscheidung zwischen Objekte der obersten Ebene ermöglicht und Unterobjekte mit dem MAPI_TOP_LEVEL-Flag, damit alle Objekte in einem Vorgang beteiligt können die gleiche [IMAPIProgress](imapiprogressiunknown.md) -Implementierung, Status angezeigt. Daraufhin wird die Anzeige Indikator reibungslos in einer Richtung positive fortfahren. Ob das Flag MAPI_TOP_LEVEL festgelegt ist bestimmt, wie-Dienstanbieter die anderen Parameter in nachfolgenden Aufrufe der Fortschritt-Objekts festlegen. 
  
Der Wert von **"GetFlags"** wird zunächst von der Implementierung und anschließend vom Dienstanbieter durch einen Aufruf an die [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) -Methode festgelegt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Initialisieren Sie das Flag MAPI_TOP_LEVEL immer, und klicken Sie dann stützen Sie sich auf Dienstanbieter, ihn bei Bedarf zu löschen. Dienstanbieter können deaktivieren und das Flag zurücksetzen, indem Sie die **IMAPIProgress::SetLimits** -Methode aufrufen. Weitere Informationen zum Implementieren von **"GetFlags"** und die anderen **IMAPIProgress** Methoden finden Sie unter [Implementieren einer Statusanzeige](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie eine Statusanzeige anzeigen, stellen Sie Ihre erste Aufruf einen Anruf an **IMAPIProgress::GetFlags**. Der zurückgegebene Wert sollte MAPI_TOP_LEVEL, da allen Implementierungen den Inhalt des Parameters _LpulFlags_ auf diesen Wert initialisieren. Weitere Informationen zur Reihenfolge der Aufrufe eines Objekts Fortschritt finden Sie unter [Display eine Statusanzeige](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetFlags  <br/> |MFCMAPI (engl.) wird die **IMAPIProgress::GetFlags** -Methode verwendet, um zu bestimmen, welche Attribute festgelegt sind. Gibt MAPI_TOP_LEVEL zurück, es sei denn, Flags mit der **IMAPIProgress::SetLimits** -Methode festgelegt wurden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress: IUnknown](imapiprogressiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md)
  
[Implementieren eine Statusanzeige](implementing-a-progress-indicator.md)

