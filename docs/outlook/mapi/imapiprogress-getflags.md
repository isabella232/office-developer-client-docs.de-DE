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
ms.openlocfilehash: 810192bfc85c9934a282f02a0839aaed539f744d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270267"
---
# <a name="imapiprogressgetflags"></a>IMAPIProgress::GetFlags

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt Flageinstellungen aus dem Progress-Objekt für die Vorgangsebene zurück, auf der die Statusinformationen berechnet werden.
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> Out Eine Bitmaske von Flags, die die Vorgangsebene steuert, auf der die Statusinformationen berechnet werden. Das folgende Flag kann zurückgegeben werden:
    
MAPI_TOP_LEVEL 
  
> Der Fortschritt wird für das Objekt der obersten Ebene, das Objekt, das vom Client zum Starten des Vorgangs aufgerufen wird, berechnet. Beispielsweise ist das Objekt der obersten Ebene in einem Ordner Kopiervorgang der Ordner, der kopiert wird. Wenn MAPI_TOP_LEVEL nicht festgelegt ist, wird Progress für ein Objekt auf niedrigerer Ebene oder ein Subobjekt berechnet. Im Ordner Kopiervorgang ist ein Objekt auf niedrigerer Ebene einer der Unterordner in dem Ordner, der kopiert wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Flags-Wert wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Mit MAPI können Dienstanbieter zwischen Objekten auf oberster Ebene und Unterobjekten mit dem MAPI_TOP_LEVEL-Flag differenzieren, sodass alle an einem Vorgang beteiligten Objekte dieselbe [IMAPIProgress](imapiprogressiunknown.md) -Implementierung zum Anzeigen des Fortschritts verwenden können. Dadurch wird die Anzeige des Indikators reibungslos in eine einzelne positive Richtung fortgesetzt. Ob das MAPI_TOP_LEVEL-Flag festgelegt ist, bestimmt, wie Dienstanbieter die anderen Parameter in nachfolgenden Aufrufen des Progress-Objekts festlegen. 
  
Der von GetFlags zurückgegebene Wert wird anfänglich durch den Implementierer und anschließend durch den Dienstanbieter durch einen Aufruf der [IMAPIProgress::](imapiprogress-setlimits.md) setlimits-Methode festgelegt. **** 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Initialisieren Sie das Flag immer für MAPI_TOP_LEVEL, und verlassen Sie sich dann auf Dienstanbieter, um es bei Bedarf zu löschen. Dienstanbieter können das Flag löschen und zurücksetzen, indem Sie die **IMAPIProgress::** setlimits-Methode aufrufen. Weitere Informationen zum Implementieren von GetFlags und den anderen **IMAPIProgress** -Methoden finden Sie unter [Implementieren einer Statusanzeige](implementing-a-progress-indicator.md). ****
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie eine Statusanzeige anzeigen, machen Sie Ihren ersten Aufruf einen Aufruf von **IMAPIProgress::** GetFlags. Der zurückgegebene Wert sollte MAPI_TOP_LEVEL sein, da alle Implementierungen den Inhalt des _lpulFlags_ -Parameters auf diesen Wert initialisieren. Weitere Informationen zur Abfolge von Aufrufen eines Progress-Objekts finden Sie unter [Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Kommentar**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress:: GetFlags  <br/> |MFCMAPI verwendet die **IMAPIProgress::** GetFlags-Methode, um zu bestimmen, welche Flags festgelegt sind. Gibt MAPI_TOP_LEVEL zurück, es sei denn, Flags wurden mithilfe der **IMAPIProgress::** setlimits-Methode festgelegt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md)
  
[Implementieren eines Statusindikators](implementing-a-progress-indicator.md)

