---
title: Implementieren einer Statusanzeige
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a062a88-e87e-4c0c-944e-544a8f080930
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6972c960705c336aa6ff96d81b48ccbd490a22ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435096"
---
# <a name="implementing-a-progress-indicator"></a>Implementieren einer Statusanzeige

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Viele der von Clients initiierten Vorgänge nehmen eine beträchtliche Zeit in Anspruch. Einer der Eingabeparameter für diese potenziell langwierigen Vorgänge ist ein Zeiger auf ein Progress-Objekt, ein Objekt, das die [IMAPIProgress: IUnknown](imapiprogressiunknown.md) -Schnittstelle implementiert. Progress-Objekte steuern das Erscheinungsbild und die Anzeige von Fortschrittsindikatoren und werden von Clients und von MAPI implementiert. Sie können auswählen, ob ein Progress-Objekt implementiert werden soll. Die MAPI-Implementierung steht für Dienstanbieter zur Verfügung, wenn Sie keine Implementierung angeben. 
  
Progress-Objekte können mit den folgenden Daten Teilen verwendet werden:
  
- Ein globaler Mindestwert, der bei Aufruf der [IMAPIProgress::P rogress](imapiprogress-progress.md) -Methode kleiner oder gleich dem Wert des _ulValue_ -Parameters sein muss. Zu Beginn des Vorgangs entspricht _ulValue_ diesem Minimalwert. 
    
- Ein globaler Maximalwert, der bei Aufruf der **IMAPIProgress::P rogress** -Methode größer oder gleich dem _ulValue_ -Parameter sein sollte. Am Ende des Vorgangs entspricht _ulValue_ diesem Maximalwert. 
    
- Ein Flags-Wert, der angibt, ob der Fortschritt einem Element auf oberster oder niedrigerer Ebene entspricht.
    
- Ein Wert, der die aktuelle Statusstufe für den Vorgang angibt.
    
- Die Anzahl der derzeit verarbeiteten Elemente im Verhältnis zu der Summe.
    
- Die Gesamtzahl der während des Vorgangs zu verarbeitenden Elemente.
    
Die Mindest-und Höchstwerte stellen den Anfang und das Ende des Vorgangs in numerischer Form dar. Verwenden Sie 1 für den anfänglichen Minimalwert und 1000 für den anfänglichen Maximalwert, und übergeben Sie diese Werte an Dienstanbieter in den Methoden [IMAPIProgress:: GetMin](imapiprogress-getmin.md) und [IMAPIProgress:: GetMax](imapiprogress-getmax.md) . Dienstanbieter setzen diese Werte zurück, wenn Sie [IMAPIProgress::](imapiprogress-setlimits.md)setlimits aufrufen. 
  
Der Flags-Wert wird von Dienstanbietern verwendet, um zu bestimmen, wie die anderen Werte festgelegt werden sollen. Initialisieren Sie den Flags-Wert in MAPI_TOP_LEVEL, und geben Sie diesen Wert **** in der Implementierung von GetFlags zurück, bis der Dienstanbieter es durch Aufrufen von setlimits erneut festlegt. **** 
  
Speichern Sie in ihrer Implementierung **** der setlimits-Methode lokale Kopien der einzelnen Parameter: _lpulMin_, _lpulMax_und _lpulFlags_. Diese Werte sollten leicht verfügbar sein, wenn ein Dienstanbieter Ihre **GetMin**-, **GetMax**- **** oder GetFlags-Methoden aufruft. 
  
Um die Anzeige der Statusanzeige zu aktualisieren, rufen Dienstanbieter Ihre **IMAPIProgress::P rogress** -Methode auf. Für diese Methode gibt es drei Parameter: einen Wert, eine Anzahl und eine Summe. Verwenden Sie den ersten Parameter _ulValue_, um die Statusanzeige anzuzeigen. Der _ulValue_ -Parameter ist die Statusanzeige und ist gleich Global _ulMin_ nur am Anfang des Vorgangs und gleich globaler _ulMax_ nur nach Abschluss des Vorgangs. 
  
Verwenden Sie die zweite und dritte Parameters, _ulCount_ und _ulTotal_, falls verfügbar, um eine optionale Meldung wie "5 Elemente, die von 10 abgeschlossen" anzuzeigen. Wenn der zweite und der dritte Parameter auf 0 festgelegt sind, können Sie auswählen, ob die Statusanzeige visuell geändert werden soll. Einige Dienstanbieter legen diese Parameter auf NULL fest, um anzugeben, dass Sie ein Unterobjekt verarbeiten, dessen Fortschritt relativ zu einem übergeordneten Objekt überwacht wird. In dieser Situation ist es sinnvoll, die Anzeige nur zu ändern, wenn das übergeordnete Objekt den Fortschritt meldet. Einige Dienstanbieter übergeben Nullen für diese Parameter jedes Mal. 
  

