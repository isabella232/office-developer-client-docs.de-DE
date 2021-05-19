---
title: IMAPIProgressProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.Progress
api_type:
- COM
ms.assetid: edbf7623-a64e-43b8-8379-e3cde2433d91
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3cf639286a504b9edb600214d13dbe50710e76a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435495"
---
# <a name="imapiprogressprogress"></a>IMAPIProgress::Progress

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Aktualisiert die Statusanzeige mit einer Anzeige des Fortschritts, der zum Abschluss des Vorgangs erfolgt. 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a>Parameter

 _ulValue_
  
> [in] Eine Zahl, die die aktuelle Fortschrittsstufe (berechnet aus den  _Parametern ulCount_ und  _ulTotal_ oder  _den Parametern lpulMin_ und  _lpulMax_ der [IMAPIProgress::SetLimits-Methode)](imapiprogress-setlimits.md) zwischen dem globalen unteren Grenzwert und dem globalen oberen Grenzwert angibt. 
    
 _ulCount_
  
> [in] Eine Zahl, die das aktuell verarbeitete Element relativ zur Gesamtsumme angibt.
    
 _ulTotal_
  
> [in] Die Gesamtanzahl der Während des Vorgangs zu verarbeitende Elemente.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Statusanzeige wurde erfolgreich aktualisiert.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Der  _ulValue-Parameter_ entspricht dem globalen Minimalwert nur zu Beginn des Vorgangs und dem globalen Maximalwert erst nach Abschluss des Vorgangs. 
  
Verwenden Sie  _die ulCount-_ und  _ulTotal-Parameter,_ wenn verfügbar, um eine optionale Meldung wie "5 von 10 abgeschlossene Elemente" anzeigen zu können. Wenn  _ulCount_ und  _ulTotal_ auf 0 festgelegt sind, entscheiden Sie, ob die Statusanzeige visuell geändert werden soll. Einige Dienstanbieter legen diese Parameter auf 0 fest, um anzugeben, dass sie ein Unterobjekt verarbeiten, dessen Fortschritt relativ zu einem übergeordneten Objekt überwacht wird. In dieser Situation ist es sinnvoll, die Anzeige nur zu ändern, wenn das übergeordnete Objekt den Fortschritt meldet. Einige Dienstanbieter übergeben jedes Mal 0 für diese Parameter. 
  
Weitere Informationen zum Implementieren von **Progress** und den anderen [IMAPIProgress-Methoden](imapiprogressiunknown.md) finden Sie unter [Implementing a Progress Indicator](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Nicht alle drei Parameter für **IMAPIProgress::P rogress** sind erforderlich. Der einzige erforderliche Parameter ist  _ulValue_, eine Zahl, die den Prozentsatz des Fortschritts angibt. Wenn das MAPI_TOP_LEVEL festgelegt ist, können Sie auch eine Objektanzahl und eine Objektsumme übergeben. Einige Implementierungen verwenden diese Werte, um einen Ausdruck wie "5 von 10 abgeschlossene Elemente" mit der Statusanzeige zu zeigen. 
  
Wenn Sie alle Nachrichten in einem einzigen Ordner kopieren, legen Sie  _ulTotal_ auf die Gesamtanzahl der zu kopierende Nachrichten festgelegt. Wenn Sie einen Ordner kopieren, legen Sie  _ulTotal_ auf die Anzahl der Unterordner im Ordner festgelegt. Wenn der zu kopierende Ordner keine Unterordner und nur Nachrichten enthält, legen Sie  _ulTotal_ auf 1. 
  
Weitere Informationen dazu, wie und wann Statusobjekte aufgerufen werden, finden Sie unter [Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Kommentar**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::P rogress  <br/> |MFCMAPI verwendet die **IMAPIProgress::P rogress-Methode,** um die MFCMAPI-Statusleiste mit dem aktuellen Fortschrittsprozentsatz zu aktualisieren, der aus  _uValue_ und den aktuellen Maximal- und Minimalwerten berechnet wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md)
  
[Implementieren eines Statusindikators](implementing-a-progress-indicator.md)

