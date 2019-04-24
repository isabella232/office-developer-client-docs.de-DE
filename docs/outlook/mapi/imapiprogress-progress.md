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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3cf639286a504b9edb600214d13dbe50710e76a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270301"
---
# <a name="imapiprogressprogress"></a>IMAPIProgress::Progress

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Aktualisiert die Statusanzeige mit einer Anzeige des Fortschritts beim Abschließen des Vorgangs. 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a>Parameter

 _ulValue_
  
> in Eine Zahl, die die aktuelle Fortschritts Ebene angibt (berechnet aus den Parametern _ulCount_ und _ulTotal_ oder aus den Parametern _lpulMin_ und _lpulMax_ der [IMAPIProgress::](imapiprogress-setlimits.md) setlimits-Methode) zwischen dem globalen untere Grenze und die globale obere Grenze. 
    
 _ulCount_
  
> in Eine Zahl, die das aktuell verarbeitete Element relativ zum Gesamtwert angibt.
    
 _ulTotal_
  
> in Die Gesamtzahl der während des Vorgangs zu verarbeitenden Elemente.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Statusanzeige wurde erfolgreich aktualisiert.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Der Parameter _ulValue_ ist gleich dem globalen Minimalwert nur zu Beginn des Vorgangs und zum globalen Maximalwert nur nach Abschluss des Vorgangs. 
  
Verwenden Sie die _ulCount_ -und _ulTotal_ -Parameter, falls verfügbar, um eine optionale Meldung anzuzeigen, wie etwa "5 Elemente, die von 10 abgeschlossen wurden". Wenn _ulCount_ und _ulTotal_ auf 0 festgelegt sind, entscheiden Sie, ob die Statusanzeige visuell geändert werden soll. Einige Dienstanbieter haben diese Parameter auf 0 festgelegt, um anzugeben, dass Sie ein Unterobjekt verarbeiten, dessen Fortschritt relativ zu einem übergeordneten Objekt überwacht wird. In dieser Situation ist es sinnvoll, die Anzeige nur zu ändern, wenn das übergeordnete Objekt den Fortschritt meldet. Einige Dienstanbieter übergeben jedes Mal 0 für diese Parameter. 
  
Weitere Informationen zum Implementieren des **Fortschritts** und der anderen [IMAPIProgress](imapiprogressiunknown.md) -Methoden finden Sie unter [Implementieren einer Statusanzeige](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Nicht alle drei Parameter für **IMAPIProgress::P rogress** sind erforderlich. Der einzige erforderliche Parameter ist _ulValue_, eine Zahl, die den Prozentsatz des Fortschritts angibt. Wenn das MAPI_TOP_LEVEL-Flag festgelegt ist, können Sie auch eine Objektanzahl und ein Objekt insgesamt. Einige Implementierungen verwenden diese Werte, um einen Ausdruck wie "5 Elemente, die von 10 abgeschlossen wurden" mit der Statusanzeige anzuzeigen. 
  
Wenn Sie alle Nachrichten in einem einzelnen Ordner kopieren, legen Sie _ulTotal_ auf die Gesamtzahl der kopierten Nachrichten fest. Wenn Sie einen Ordner kopieren, legen Sie _ulTotal_ auf die Anzahl der Unterordner im Ordner fest. Wenn der zu kopierende Ordner keine Unterordner und nur Nachrichten enthält, legen Sie _ulTotal_ auf 1 fest. 
  
Weitere Informationen dazu, wie und wann Statusobjekte aufgerufen werden, finden Sie unter [Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Kommentar**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::P rogress  <br/> |MFCMAPI verwendet die **IMAPIProgress::P rogress** -Methode, um die MfcMapi-Statusleiste mit dem aktuellen prozentualen Fortschritt zu aktualisieren, berechnet von _uValue_ und den aktuellen maximalen und minimalen Werten.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md)
  
[Implementieren eines Statusindikators](implementing-a-progress-indicator.md)

