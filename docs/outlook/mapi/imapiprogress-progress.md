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
ms.openlocfilehash: 3fc72f008d1c2610de3c74762aabc6231dabbfbd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589056"
---
# <a name="imapiprogressprogress"></a>IMAPIProgress::Progress

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Aktualisiert die Statusanzeige mit einer Anzeige des Fortschritts, sobald sie zum Abschluss des Vorgangs vorgenommen wird. 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a>Parameter

 _ulValue_
  
> [in] Eine Zahl, die dem aktuellen Stand des Fortschritts (der Parameter _UlCount_ und _UlTotal_ oder der Parameter _LpulMin_ und _LpulMax_ der [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) -Methode berechnet) zwischen der globalen an Untergrenze und der globalen Obergrenze. 
    
 _ulCount_
  
> [in] Eine Zahl, die das Element derzeit verarbeitete relativ zur Summe angibt.
    
 _ulTotal_
  
> [in] Die Gesamtanzahl von Elementen, die während des Vorgangs verarbeitet werden.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Statusanzeige wurde erfolgreich aktualisiert.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Der Parameter _UlValue_ werden gleich dem globalen minimalen Wert nur am Anfang des Vorgangs und dem globalen Höchstwert nur nach Abschluss des Vorgangs. 
  
Verwenden Sie die Parameter _UlCount_ und _UlTotal_ , falls verfügbar, um eine optionale Nachricht wie "5 Elemente nicht genügend 10 abgeschlossen." angezeigt. Wenn _UlCount_ und _UlTotal_ auf 0 festgelegt sind, entscheiden Sie, ob die Statusanzeige visuell zu ändern. Einige Dienstanbieter legen Sie diesen Parameter auf 0, um anzugeben, dass sie ein Unterobjekt verarbeitet werden, deren Status relativ zu einem übergeordneten Objekt überwacht wird. In diesem Fall ist es sinnvoll, die Anzeige nur ändern, wenn das übergeordnete Objekt des Fortschritts meldet. Einige Dienstanbieter übergeben 0 für diese Parameter jedes Mal. 
  
Weitere Informationen zur Verwendung **des Fortschritts** und der andere [IMAPIProgress](imapiprogressiunknown.md) -Methoden implementieren finden Sie unter [Implementieren einer Statusanzeige](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Nicht alle drei Parameter zu **IMAPIProgress::Progress** sind erforderlich. Der einzige Parameter, der erforderlich ist ist _UlValue_, eine Zahl, die den Prozentsatz des Fortschritts angibt. Wenn das Flag MAPI_TOP_LEVEL festgelegt ist, können Sie auch die Anzahl der Objekte und ein Objekt insgesamt übergeben. Einige Implementierungen verwenden diese Werte, um einen Ausdruck wie "5 Elemente nicht genügend 10 abgeschlossen" mit der Statusanzeige anzuzeigen. 
  
Wenn Sie alle Nachrichten in einem gemeinsamen Ordner kopieren möchten, legen Sie _UlTotal_ auf die Gesamtzahl der kopierten Nachrichten. Wenn Sie einen Ordner kopieren, legen Sie _UlTotal_ auf die Anzahl der Unterordner im Ordner. Wenn der Ordner kopiert werden keine Unterordner und nur Nachrichten enthält, setzen Sie _UlTotal_ auf 1 fest. 
  
Weitere Informationen dazu, wie und wann ein Fortschritt-Objekt aufrufen finden Sie unter [Display eine Statusanzeige](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::Progress  <br/> |MFCMAPI (engl.) verwendet die **IMAPIProgress::Progress** -Methode zum Aktualisieren der Statusleiste MFCMAPI (engl.) mit den aktuellen Prozentsatz des Fortschritts, aus _uValue_ und die aktuellen Werte der maximal- und Minimalwerte berechnet.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md)
  
[Implementieren eines Statusindikators](implementing-a-progress-indicator.md)

