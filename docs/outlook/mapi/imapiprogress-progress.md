---
title: IMAPIProgressProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProgress.Progress
api_type:
- COM
ms.assetid: edbf7623-a64e-43b8-8379-e3cde2433d91
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 92da3cc185fec19fc8cb1e7e7089ba029cd95cb3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620961"
---
# <a name="imapiprogressprogress"></a>IMAPIProgress::Progress

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Aktualisiert die Statusanzeige mit einer Anzeige des Fortschritts beim Abschluss des Vorgangs. 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a>Parameter

 _ulValue_
  
> [in] Eine Zahl, die den aktuellen Status (berechnet aus den  _Parametern ulCount_ und  _ulTotal_ oder aus den  _Parametern lpulMin_ und  _lpulMax_ der [IMAPIProgress::SetLimits-Methode)](imapiprogress-setlimits.md) zwischen dem globalen Untergrenzwert und dem globalen oberen Grenzwert angibt. 
    
 _ulCount_
  
> [in] Eine Zahl, die das aktuell verarbeitete Element relativ zur Summe angibt.
    
 _ulTotal_
  
> [in] Die Gesamtzahl der Elemente, die während des Vorgangs verarbeitet werden sollen.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Statusanzeige wurde erfolgreich aktualisiert.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Der  _ulValue-Parameter_ entspricht nur zu Beginn des Vorgangs dem globalen Minimalwert und erst nach Abschluss des Vorgangs dem globalen Maximalwert. 
  
Verwenden Sie die  _UlCount-_ und  _ulTotal-Parameter,_ falls verfügbar, um eine optionale Meldung anzuzeigen, z. B. "5 von 10 abgeschlossene Elemente". Wenn  _ulCount_ und  _ulTotal_ auf 0 festgelegt sind, entscheiden Sie, ob die Statusanzeige visuell geändert werden soll. Einige Dienstanbieter legen diese Parameter auf 0 fest, um anzugeben, dass sie ein Unterobjekt verarbeiten, dessen Fortschritt relativ zu einem übergeordneten Objekt überwacht wird. In diesem Fall ist es sinnvoll, die Anzeige nur zu ändern, wenn das übergeordnete Objekt den Fortschritt meldet. Einige Dienstanbieter übergeben jedes Mal 0 für diese Parameter. 
  
Weitere Informationen zum Implementieren von **Progress** und den anderen [IMAPIProgress-Methoden](imapiprogressiunknown.md) finden Sie unter [Implementieren einer Statusanzeige.](implementing-a-progress-indicator.md)
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Nicht alle drei Parameter für **IMAPIProgress::P Rogress** sind erforderlich. Der einzige parameter, der erforderlich ist, ist  _ulValue_, eine Zahl, die den Prozentsatz des Fortschritts angibt. Wenn das flag MAPI_TOP_LEVEL festgelegt ist, können Sie auch eine Objektanzahl und eine Objektgesamtsumme übergeben. Einige Implementierungen verwenden diese Werte, um einen Ausdruck wie "5 abgeschlossene Elemente von 10" mit der Statusanzeige anzuzeigen. 
  
Wenn Sie alle Nachrichten in einem einzigen Ordner kopieren, legen Sie  _"ulTotal"_ auf die Gesamtzahl der zu kopierenden Nachrichten fest. Wenn Sie einen Ordner kopieren, legen Sie  _"ulTotal"_ auf die Anzahl der Unterordner im Ordner fest. Wenn der zu kopierende Ordner keine Unterordner und nur Nachrichten enthält, legen Sie  _"ulTotal"_ auf 1 fest. 
  
Weitere Informationen dazu, wie und wann Statusobjekte aufgerufen werden, finden Sie unter [Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Kommentar**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::P rogress  <br/> |MFCMAPI verwendet die **IMAPIProgress::P Rogress-Methode,** um die MFCMAPI-Statusleiste mit dem aktuellen Prozentsatz des Fortschritts zu aktualisieren, der aus  _uValue_ und den aktuellen Maximal- und Mindestwerten berechnet wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md)
  
[Implementieren eines Statusindikators](implementing-a-progress-indicator.md)

