---
title: Implementieren einer Statusanzeige
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3a062a88-e87e-4c0c-944e-544a8f080930
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 831523a9ce7c9b0713b86289ddc3fef7a423d5b8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556455"
---
# <a name="implementing-a-progress-indicator"></a>Implementieren einer Statusanzeige

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Viele der von Clients initiierten Vorgänge dauern sehr viel Zeit. Einer der Eingabeparameter für diese potenziell langwierigen Vorgänge ist ein Zeiger auf ein Statusobjekt – ein Objekt, das die [IMAPIProgress : IUnknown-Schnittstelle](imapiprogressiunknown.md) implementiert. Statusobjekte steuern die Darstellung und Anzeige von Statusanzeigen und werden von Clients und mapi implementiert. Sie können auswählen, ob ein Statusobjekt implementiert werden soll. Die MAPI-Implementierung kann von Dienstanbietern verwendet werden, wenn Sie keine Implementierung bereitstellen möchten. 
  
Statusobjekte arbeiten mit den folgenden Daten:
  
- Ein globaler Minimalwert, der beim Aufrufen der [IMAPIProgress::P Rogress-Methode](imapiprogress-progress.md) kleiner oder gleich dem Wert des  _ulValue-Parameters_ sein sollte. Am Anfang des Vorgangs ist  _ulValue_ gleich diesem Minimalwert. 
    
- Ein globaler Maximalwert, der beim Aufrufen der **IMAPIProgress::P Rogress-Methode** größer oder gleich dem  _ulValue-Parameter_ sein sollte. Am Ende des Vorgangs ist  _ulValue_ gleich diesem Maximalwert. 
    
- Ein Kennzeichenwert, der angibt, ob der Fortschritt einem Element der obersten oder unteren Ebene entspricht.
    
- Ein Wert, der die aktuelle Statusstufe für den Vorgang angibt.
    
- Die Anzahl der aktuell verarbeiteten Elemente relativ zur Summe.
    
- Die Gesamtzahl der Elemente, die während des Vorgangs verarbeitet werden sollen.
    
Die Mindest- und Höchstwerte stellen den Anfang und das Ende des Vorgangs in numerischer Form dar. Verwenden Sie 1 für den anfänglichen Minimalwert und 1000 für den anfänglichen Maximalwert, und übergeben Sie diese Werte an Dienstanbieter in den Methoden [IMAPIProgress::GetMin](imapiprogress-getmin.md) und [IMAPIProgress::GetMax.](imapiprogress-getmax.md) Dienstanbieter setzen diese Werte zurück, wenn sie [IMAPIProgress::SetLimits](imapiprogress-setlimits.md)aufrufen. 
  
Der Kennzeichenwert wird von Dienstanbietern verwendet, um zu bestimmen, wie die anderen Werte festgelegt werden sollen. Initialisieren Sie den Flags-Wert auf MAPI_TOP_LEVEL und geben Sie diesen Wert in Ihrer Implementierung von **GetFlags zurück,** bis der Dienstanbieter ihn durch Aufrufen von **SetLimits** zurücksetzt. 
  
Speichern Sie in der Implementierung der **SetLimits** -Methode lokale Kopien der einzelnen Parameter:  _lpulMin_,  _lpulMax_ und  _lpulFlags_. Diese Werte sollten verfügbar sein, wenn ein Dienstanbieter Ihre **GetMin-,** **GetMax-** oder **GetFlags-Methoden aufruft.** 
  
Um die Anzeige der Statusanzeige zu aktualisieren, rufen Dienstanbieter Ihre **IMAPIProgress::P Rogress-Methode** auf. Für diese Methode gibt es drei Parameter: einen Wert, eine Anzahl und eine Summe. Verwenden Sie den ersten Parameter,  _ulValue,_ um die Statusanzeige anzuzeigen. Der _ulValue-Parameter_ ist die Statusanzeige und entspricht nur am Anfang des Vorgangs dem globalen _ulMin_ und erst nach Abschluss des Vorgangs dem globalen _ulMax._ 
  
Verwenden Sie den zweiten und dritten Parameter,  _ulCount_ und  _ulTotal,_ falls verfügbar, um eine optionale Meldung anzuzeigen, z. B. "5 von 10 abgeschlossene Elemente". Wenn der zweite und dritte Parameter auf 0 festgelegt sind, können Sie auswählen, ob die Statusanzeige visuell geändert werden soll. Einige Dienstanbieter legen diese Parameter auf Nullen fest, um anzugeben, dass sie ein Unterobjekt verarbeiten, dessen Fortschritt relativ zu einem übergeordneten Objekt überwacht wird. In diesem Fall ist es sinnvoll, die Anzeige nur zu ändern, wenn das übergeordnete Objekt den Fortschritt meldet. Einige Dienstanbieter übergeben jedes Mal Nullen für diese Parameter. 
  

