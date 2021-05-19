---
title: Implementieren eines Fortschrittsindikators
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
# <a name="implementing-a-progress-indicator"></a>Implementieren eines Fortschrittsindikators

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Viele der von Clients initiierten Vorgänge dauern sehr viel Zeit. Einer der Eingabeparameter für diese potenziell langwierigen Vorgänge ist ein Zeiger auf ein Progress-Objekt – ein Objekt, das die [IMAPIProgress : IUnknown-Schnittstelle](imapiprogressiunknown.md) implementiert. Progress-Objekte steuern die Darstellung und Anzeige von Fortschrittsindikatoren und werden von Clients und von MAPI implementiert. Sie können auswählen, ob ein Progress-Objekt implementiert werden soll. Die MAPI-Implementierung steht Dienstanbietern zur Verfügung, wenn Sie sich dafür auswählen, keine Implementierung zu liefern. 
  
Progress-Objekte arbeiten mit den folgenden Datenteilen:
  
- Ein globaler Minimalwert, der beim Aufruf der [IMAPIProgress::P rogress-Methode](imapiprogress-progress.md) kleiner oder gleich dem Wert des  _ulValue-Parameters_ sein sollte. Zu Beginn des Vorgangs entspricht  _ulValue_ diesem Minimalwert. 
    
- Ein globaler Maximalwert, der beim Aufruf der **IMAPIProgress::P rogress-Methode** größer oder gleich dem  _ulValue-Parameter_ sein sollte. Am Ende des Vorgangs entspricht  _ulValue_ diesem Maximalwert. 
    
- Ein Flags-Wert, der angibt, ob der Fortschritt einem Element der obersten oder unteren Ebene entspricht.
    
- Ein Wert, der die aktuelle Fortschrittsstufe für den Vorgang angibt.
    
- Die Anzahl der aktuell verarbeiteten Elemente relativ zur Gesamtsumme.
    
- Die Gesamtanzahl der Während des Vorgangs zu verarbeitende Elemente.
    
Die Minimal- und Maximalwerte stellen den Anfang und das Ende des Vorgangs in numerischer Form dar. Verwenden Sie 1 für den anfänglichen Minimalwert und 1000 für den anfänglichen Maximalwert, und übergeben Sie diese Werte an Dienstanbieter in den [Methoden IMAPIProgress::GetMin](imapiprogress-getmin.md) und [IMAPIProgress::GetMax.](imapiprogress-getmax.md) Dienstanbieter setzen diese Werte zurück, wenn [sie IMAPIProgress::SetLimits aufrufen.](imapiprogress-setlimits.md) 
  
Der Flags-Wert wird von Dienstanbietern verwendet, um zu bestimmen, wie die anderen Werte festgelegt werden sollen. Initialisieren Sie den Flags-Wert, MAPI_TOP_LEVEL, und geben Sie diesen Wert in Ihrer Implementierung von **GetFlags** zurück, bis der Dienstanbieter ihn durch Aufrufen von **SetLimits zurück setzt.** 
  
Speichern Sie in der Implementierung der **SetLimits-Methode** lokale Kopien der einzelnen Parameter:  _lpulMin,_  _lpulMax_ und  _lpulFlags_. Diese Werte sollten sofort verfügbar sein, wenn ein Dienstanbieter Ihre **GetMin-,** **GetMax-** oder **GetFlags-Methoden** aufruft. 
  
Zum Aktualisieren der Anzeige des Statusindikators rufen Dienstanbieter Ihre **IMAPIProgress::P rogress-Methode** auf. Diese Methode enthält drei Parameter: einen Wert, eine Anzahl und eine Summe. Verwenden Sie den ersten Parameter  _ulValue,_ um die Statusanzeige zu zeigen. Der _ulValue-Parameter_ ist der Fortschrittsindikator und entspricht nur zu Beginn des Vorgangs global _ulMin_ und erst nach Abschluss des Vorgangs global _ulMax._ 
  
Verwenden Sie den zweiten und dritten Parameter  _ulCount_ und  _ulTotal_, falls verfügbar, um eine optionale Meldung wie "5 von 10 abgeschlossene Elemente" anzeigen zu können. Wenn der zweite und dritte Parameter auf 0 festgelegt sind, können Sie auswählen, ob die Statusanzeige visuell geändert werden soll. Einige Dienstanbieter legen diese Parameter auf Nullen fest, um anzugeben, dass sie ein Unterobjekt verarbeiten, dessen Fortschritt relativ zu einem übergeordneten Objekt überwacht wird. In dieser Situation ist es sinnvoll, die Anzeige nur zu ändern, wenn das übergeordnete Objekt den Fortschritt meldet. Einige Dienstanbieter übergeben für diese Parameter jedes Mal Nullen. 
  

