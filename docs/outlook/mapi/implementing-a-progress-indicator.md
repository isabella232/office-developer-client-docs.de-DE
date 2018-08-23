---
title: Implementieren eines Statusindikators
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a062a88-e87e-4c0c-944e-544a8f080930
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1a359ec413da91b3e2819978e80ea0a921f6b245
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587124"
---
# <a name="implementing-a-progress-indicator"></a>Implementieren eines Statusindikators

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Viele Vorgänge, die von Clients initiiert beanspruchen sehr viel Zeit. Einer der Eingabeparameter für diese Vorgänge potenziell langen ist ein Zeiger auf ein Objekt Fortschritt – ein Objekt, das implementiert die [IMAPIProgress: IUnknown](imapiprogressiunknown.md) Schnittstelle. Fortschritt Objekte Steuern der Darstellung und Anzeige von Statusanzeigen und von Clients und von MAPI implementiert werden. Sie können auswählen, ob einem Fortschritt-Objekt implementiert werden soll oder nicht. Die MAPI-Implementierung ist verfügbar für Dienstanbieter zu verwenden, wenn Sie festlegen, dass keine Implementierung bereitstellen. 
  
Fortschritt Objekte arbeiten Sie mit der folgenden Datenelemente:
  
- Eine globale Mindestwert, der Ihre [IMAPIProgress::Progress](imapiprogress-progress.md) -Methode aufgerufen wird, kleiner oder gleich dem Wert des Parameters _UlValue_ sein sollte. Am Anfang des Vorgangs werden diese Minimalwert _UlValue_ . 
    
- Einen globalen maximale Wert, der die **IMAPIProgress::Progress** -Methode aufgerufen wird, größer als oder gleich dem Parameter _UlValue_ sein sollte. Am Ende des Vorgangs werden diese Maximalwert _UlValue_ . 
    
- Ein Kennzeichen Wert gibt an, ob der Status von oben entspricht oder niedrigerer Ebene item.
    
- Ein Wert, der angibt, die aktuelle Stufe des Fortschritt für den Vorgang.
    
- Die Anzahl der derzeit verarbeiteten Elemente relativ zur Summe.
    
- Die Gesamtanzahl von Elementen, die während des Vorgangs verarbeitet werden.
    
Die minimale und maximale Werte darstellen Anfang und Ende des Vorgangs in numerische Form. Verwenden Sie 1 für die anfängliche Mindestwert und 1000 Höchstwert für die anfängliche, diese Werte in den Methoden [IMAPIProgress::GetMin](imapiprogress-getmin.md) und [IMAPIProgress::GetMax](imapiprogress-getmax.md) Dienstanbietern übergeben. Dienstanbieter setzen Sie diese Werte beim Aufruf von [IMAPIProgress::SetLimits](imapiprogress-setlimits.md)zurück. 
  
Der Wert des Flags wird vom Dienstanbieter verwendet, um zu bestimmen, wie sie die anderen Werte festlegen sollten. Den Wert des Flags auf MAPI_TOP_LEVEL zu initialisieren und Rückgabewert dieses in die Implementierung von **"GetFlags"** , bis der Dienstanbieter durch Aufrufen von **SetLimits**zurückgesetzt. 
  
Speichern Sie lokale Kopien der einzelnen Parameter in der Implementierung der **SetLimits** -Methode: _LpulMin_, _LpulMax_und _LpulFlags_. Diese Werte sollten sofort verfügbar sein, bei ein Dienstanbieter Ihrer **GetMin**, **GetMax**oder **"GetFlags"** aufruft. 
  
Dienstanbieter Aufrufen **IMAPIProgress::Progress** Methode, um die Anzeige der Statusanzeige zu aktualisieren. Es gibt drei Parameter an diese Methode: ein Wert, der die Anzahl und insgesamt. Verwenden Sie den ersten Parameter _UlValue_, um die Statusanzeige anzuzeigen. Der Parameter _UlValue_ wird die Statusanzeige und werden nur globale _UlMin_ am Anfang des Vorgangs gleich und gleich globale _UlMax_ nur nach Abschluss des Vorgangs. 
  
Verwenden Sie die zweite und dritte Parameter sowie die _UlCount_ und _UlTotal_, falls verfügbar, um eine optionale Nachricht wie "5 Elemente nicht genügend 10 abgeschlossen." angezeigt Wenn die zweite und dritte Parameter auf 0 festgelegt sind, können Sie, ob er die Statusanzeige visuell zu ändern. Einige Dienstanbieter legen Sie diesen Parameter auf Nullen, um anzugeben, dass sie ein Unterobjekt verarbeitet werden, deren Status relativ zu einem übergeordneten Objekt überwacht wird. In diesem Fall ist es sinnvoll, die Anzeige nur ändern, wenn das übergeordnete Objekt des Fortschritts meldet. Einige Dienstanbieter übergeben Nullen für diese Parameter jedes Mal. 
  

