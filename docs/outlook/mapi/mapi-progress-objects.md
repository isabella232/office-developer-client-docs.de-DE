---
title: MAPI-Fortschrittsobjekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e446004e-1ef2-4e58-b764-de7b4dcefaf1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 73d905028f8f62ad8cbb9da9b1ad61b8cab1065e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422026"
---
# <a name="mapi-progress-objects"></a>MAPI-Fortschrittsobjekte

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Mit den Methoden und Daten eines Progress-Objekts können Sie steuern, wie der Fortschritt der Indikatorberichte ausgeführt wird. Obwohl ein Client oder eine MAPI das Progress-Objekt implementiert, liegt der Großteil der Last der Sicherstellung der Korrektheit der Statusanzeige bei Dienstanbietern. Sie können ihre Genauigkeit garantieren, indem Sie eine bestimmte Reihenfolge und einen bestimmten Wert für die Parameter angeben, die an progress-Objektmethoden übergeben werden.
  
Die folgenden Parameter werden an Statusobjekte übergeben:
  
- Eine Bitmaske mit Flags, die mit [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) festgelegt und mit [IMAPIProgress::GetFlags abgerufen wird.](imapiprogress-getflags.md)
    
- Ein Minimalwert (lokal und global), der mit **SetLimits festgelegt** und mit [IMAPIProgress::GetMin abgerufen wird.](imapiprogress-getmin.md)
    
- Ein Maximalwert (lokal und global), der mit **SetLimits festgelegt** und mit [IMAPIProgress::GetMax abgerufen wird.](imapiprogress-getmax.md)
    
- Ein Wert, der den aktuellen Prozentsatz des Abschlusses des Vorgangs [angibt, der an IMAPIProgress::P rogress übergeben wird.](imapiprogress-progress.md)
    
- Eine Anzahl der Objekte, die bisher verarbeitet wurden und an **Progress übergeben wurden.**
    
- Eine Anzahl der Objekte, die an dem Vorgang beteiligt sind und an **Progress übergeben werden.**
    
Alle Dienstanbieter beginnen ihre Statusanzeigeverarbeitung mit einem Aufruf von **IMAPIProgress::GetFlags,** um die aktuelle Flagseinstellung abzurufen. Derzeit können die Flags nur auf MAPI_TOP_LEVEL. Clients und MAPI initialisieren das Flag für MAPI_TOP_LEVEL und verlassen sich dabei auf Dienstanbieter, um es gegebenenfalls zu löschen. 
  
Der Flags-Wert ist auf MAPI_TOP_LEVEL festgelegt, während Sie mit dem Objekt auf oberster Ebene in dem Vorgang arbeiten. Das Objekt auf oberster Ebene ist das Objekt, das vom Client aufgerufen wird, um einen Vorgang zu starten. Bei einem Ordnerkopievorgang ist dies der zu kopierende Ordner. In einem Ordnerlöschvorgang ist dies der zu löschende Ordner. Wenn Sie einen Aufruf zum Verarbeiten eines Objekts auf niedrigerer Ebene oder eines Unterobjekts starten, löschen Sie den Flags-Wert. Bei einem Ordnerkopievorgang sind Unterobjekte die Unterordner, die sich im zu kopierenden Ordner befinden. 
  
MIT MAPI können Sie mit dem flag MAPI_TOP_LEVEL zwischen Objekten auf oberster Ebene und Unterobjekten unterscheiden, sodass alle an einem Vorgang beteiligten Objekte dieselbe [IMAPIProgress-Implementierung](imapiprogressiunknown.md) verwenden können, um den Fortschritt anzuzeigen, wodurch die Anzeige der Anzeige in einer einzigen positiven Richtung reibungslos fortgesetzt wird. Ob das MAPI_TOP_LEVEL festgelegt ist, wirkt sich auf die Einstellungen der anderen Parameter in nachfolgenden Aufrufen des Progress-Objekts aus. 
  
Da es nichttrivial sein kann, geeignete Parameterwerte für eine Statusanzeige auf allen Ebenen eines mehrstufigen Vorgangs zu festlegen, wählen einige Dienstanbieter den Fortschritt für Unterobjekte nicht aus. 
  
 **So vermeiden Sie den Fortschritt für Unterobjekte**
  
- Übergeben Sie NULL für den  _lpProgress-Parameter_ im Aufruf zum Verarbeiten eines Unterobjekts. Wenn Sie z. B. Ordner kopieren, ist dies der Aufruf der [IMAPIFolder::CopyFolder-Methode eines](imapifolder-copyfolder.md) Unterordners. 
    
- Schreiben Sie speziellen Code, um zu bestimmen, wie der  _lpProgress-Parameter interpretiert_ wird. Da ein NULL-Wert für den  _lpProgress-Parameter_ auch bedeuten kann, dass der Client mithilfe der MAPI-Implementierung den Fortschritt anzeigen soll, ist spezieller Code erforderlich, um zu bestimmen, wann der  _lpProgress-Parameter_ ignoriert werden soll und wann [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md)aufruft.
    
Rufen **Sie IMAPIProgress::SetLimits** auf, um das MAPI_TOP_LEVEL-Flag und lokale und globale Mindest- und Höchstwerte zu setzen oder zu löschen. Der Wert der Flags-Einstellung wirkt sich darauf aus, ob das progress-Objekt die minimalen und maximalen Werte als lokal oder global versteht. Wenn das MAPI_TOP_LEVEL festgelegt ist, werden diese Werte als global betrachtet und zur Berechnung des Fortschritts für den gesamten Vorgang verwendet. Progress-Objekte initialisieren den globalen Minimalwert auf 0 und den globalen Maximalwert auf 1000. 
  
Wenn MAPI_TOP_LEVEL nicht festgelegt ist, werden die Mindest- und Höchstwerte als lokal betrachtet und intern von Anbietern verwendet, um den Fortschritt für Unterobjekte auf niedrigerer Ebene anzeigen zu können. Progress-Objekte speichern nur die lokalen Mindest- und Höchstwerte, sodass sie an Anbieter zurückgegeben werden können, wenn **GetMin** und **GetMax** aufgerufen werden. 
  
Die Parameter value, object count und object total sind Eingaben für die **IMAPIProgress::P rogress-Methode.** Der Wertparameter, eine Zahl, die den Prozentsatz des Fortschritts angibt, ist erforderlich. Wenn das MAPI_TOP_LEVEL festgelegt ist, können Sie auch eine Objektanzahl und eine Objektsumme übergeben. Einige Clients verwenden diese Werte, um einen Ausdruck wie "5 von 10 abgeschlossene Elemente" mit der Statusanzeige zu zeigen. Der Fortschritt eines Vorgangs kann ausschließlich als Prozentsatz oder Prozentsatz und in Bezug auf die Anzahl der Elemente gemeldet werden, die aus dem zu verarbeitende Gesamtwert verarbeitet wurden. Wenn Sie beispielsweise ein Nachrichtenspeicheranbieter sind und einen Kopiervorgang ausführen, der 10 Ordner kopiert, kann die Statusanzeige dem Benutzer zusätzliche Informationen liefern, indem ein Ausdruck wie "1 von 10", "2 von 10", "3 von 10" und so weiter angezeigt wird, bis der Vorgang abgeschlossen ist. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Fortschrittsindikatoren](mapi-progress-indicators.md)

