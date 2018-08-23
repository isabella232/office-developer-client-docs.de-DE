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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 010f69b70324d4280a34d2fe06d670e07d922d86
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586774"
---
# <a name="imapiprogresssetlimits"></a>IMAPIProgress::SetLimits

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Legt die oberen und unteren Grenzwerten für die Anzahl der Elemente in den Vorgang und die Kennzeichen, die steuern, wie die Statusinformationen für den Vorgang berechnet wird.
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulMin_
  
> [in] Ein Zeiger auf eine Variable, die die untere Grenze von Elementen in den Vorgang enthält.
    
 _lpulMax_
  
> [in] Ein Zeiger auf eine Variable, die den oberen Grenzwert von Elementen in den Vorgang enthält.
    
 _lpulFlags_
  
> [in] Eine Bitmaske aus Flags, die die Ebene des Vorgangs steuert, welche Fortschritt Informationen berechnet wird. Das folgende Flag kann festgelegt werden:
    
MAPI_TOP_LEVEL 
  
> Verwendet die Werte in der [IMAPIProgress::Progress](imapiprogress-progress.md) -Methode _UlCount_ und _UlTotal_ -Parameter, die derzeit verarbeiteten Element und die gesamte Elemente, die jeweils auf Inkrement Bearbeitung auf den Vorgang anzugeben. Wenn dieses Flag festgelegt ist, können die Werte der globalen unteren und oberen Grenzwerte festgelegt werden soll. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Dienstanbieter rufen die **IMAPIProgress::SetLimits** -Methode festlegen oder Entfernen des Kennzeichens MAPI_TOP_LEVEL und lokaler und globaler minimale und maximale Werte festlegen. Der Wert der Einstellung Flag bestimmt, ob das Fortschritt Objekt lokal oder global werden der höchste und der niedrigste versteht. Wenn das Flag MAPI_TOP_LEVEL festgelegt ist, werden diese Werte als global gelten und werden verwendet, um den Status für den gesamten Vorgang zu berechnen. Fortschritt Objekte Initialisieren der globalen Mindestwert 1 und der globalen Höchstwert bis 1000. 
  
Wenn MAPI_TOP_LEVEL nicht festgelegt ist, werden der höchste und der niedrigste als lokale betrachtet und Anbieter für deren Verwendung intern für unteren Ebene Unterobjekte Status angezeigt. Fortschritt Objekte speichern die lokalen minimale und maximale Werte, sodass sie-Anbieter zurückgegeben werden können, wenn die Methoden [IMAPIProgress::GetMin](imapiprogress-getmin.md) und [IMAPIProgress::GetMax](imapiprogress-getmax.md) aufgerufen werden. 
  
Weitere Informationen zum Implementieren von **SetLimits** und anderen [IMAPIProgress](imapiprogressiunknown.md) Methoden finden Sie unter [Implementieren einer Statusanzeige](implementing-a-progress-indicator.md).
  
Weitere Informationen dazu, wie und wann ein Fortschritt-Objekt aufrufen finden Sie unter [Display eine Statusanzeige](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::SetLimits  <br/> |MFCMAPI (engl.) verwendet die **IMAPIProgress::SetLimits** -Methode, um die maximal- und Minimalwerte Grenzwerte und die Kennzeichen für den Fortschritt-Objekt festzulegen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md)
  
[Implementieren eines Statusindikators](implementing-a-progress-indicator.md)

