---
title: MAPI-Fortschrittsobjekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e446004e-1ef2-4e58-b764-de7b4dcefaf1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f47abaa8892d6deadbe89eb6c05a152c84f7377f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579572"
---
# <a name="mapi-progress-objects"></a>MAPI-Fortschrittsobjekte

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Mit den Methoden und Daten eines Statusobjekts können Sie steuern, wie der Indikator den Fortschritt meldet. Obwohl ein Client oder eine MAPI das Statusobjekt implementiert, liegt der Großteil der Aufgabe, die Korrektheit der Statusanzeige sicherzustellen, bei Dienstanbietern. Sie können die Genauigkeit garantieren, indem Sie eine bestimmte Reihenfolge und einen bestimmten Wert für die Parameter angeben, die an Progress-Objektmethoden übergeben werden.
  
Die folgenden Parameter werden an Statusobjekte übergeben:
  
- Eine Bitmaske von Flags, die mit [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) festgelegt und mit [IMAPIProgress::GetFlags](imapiprogress-getflags.md)abgerufen wird.
    
- Ein Minimalwert (lokal und global), mit **SetLimits** festgelegt und mit [IMAPIProgress abgerufen::GetMin](imapiprogress-getmin.md).
    
- Ein Maximalwert (lokal und global), mit **SetLimits** festgelegt und mit [IMAPIProgress abgerufen::GetMax](imapiprogress-getmax.md).
    
- Ein Wert, der den aktuellen Prozentsatz des Abschlusses des Vorgangs angibt, der an [IMAPIProgress::P Rogress](imapiprogress-progress.md)übergeben wird.
    
- Eine Anzahl der Objekte, die bisher verarbeitet wurden, die an **Progress** übergeben wurden.
    
- Eine Anzahl der Objekte, die an den Vorgang beteiligt sind, die an **Progress** übergeben werden.
    
Alle Dienstanbieter beginnen ihre Verarbeitung der Statusanzeige mit einem Aufruf von **IMAPIProgress::GetFlags,** um die aktuelle Flags-Einstellung abzurufen. Derzeit können die Flags nur auf MAPI_TOP_LEVEL festgelegt werden. Clients und MAPI initialisieren das Flag für MAPI_TOP_LEVEL und verlassen sich dabei darauf, dass Dienstanbieter es ggf. löschen. 
  
Der Flags-Wert wird auf MAPI_TOP_LEVEL festgelegt, während Sie mit dem Objekt der obersten Ebene im Vorgang arbeiten. Das Objekt der obersten Ebene ist das Objekt, das vom Client aufgerufen wird, um einen Vorgang zu starten. Bei einem Ordnerkopiervorgang ist dies der Ordner, der kopiert wird. Bei einem Ordnerlöschvorgang ist dies der Ordner, der gelöscht wird. Wenn Sie einen Aufruf zum Verarbeiten eines Objekts der unteren Ebene oder eines untergeordneten Objekts ausführen, löschen Sie den Flags-Wert. Bei einem Ordnerkopiervorgang sind Unterobjekte die Unterordner, die sich in dem Ordner befinden, der kopiert wird. 
  
MapI ermöglicht es Ihnen, zwischen Objekten auf oberster Ebene und Unterobjekten mit dem flag MAPI_TOP_LEVEL zu unterscheiden, sodass alle Objekte, die an einem Vorgang beteiligt sind, dieselbe [IMAPIProgress-Implementierung](imapiprogressiunknown.md) verwenden können, um den Fortschritt anzuzeigen, wodurch die Anzeige des Indikators reibungslos in eine einzige positive Richtung fortgesetzt wird. Ob das flag MAPI_TOP_LEVEL festgelegt ist, wirkt sich auf die Einstellungen der anderen Parameter in nachfolgenden Aufrufen des Statusobjekts aus. 
  
Da es nichttrivial sein kann, geeignete Parameterwerte für eine Statusanzeige auf allen Ebenen eines Vorgangs mit mehreren Ebenen festzulegen, entscheiden sich einige Dienstanbieter dafür, den Fortschritt für Unterobjekte nicht anzuzeigen. 
  
 **So vermeiden Sie das Anzeigen des Fortschritts für Unterobjekte**
  
- Übergeben Sie NULL für den  _parameter lpProgress_ im Aufruf zum Verarbeiten eines Unterobjekts. Wenn Sie beispielsweise Ordner kopieren, ist dies der Aufruf der [IMAPIFolder::CopyFolder-Methode](imapifolder-copyfolder.md) eines Unterordners. 
    
- Schreiben Sie speziellen Code, um zu bestimmen, wie der  _lpProgress-Parameter_ interpretiert wird. Da ein NULL-Wert für den  _lpProgress-Parameter_ auch bedeuten kann, dass der Client den Fortschritt mithilfe der MAPI-Implementierung anzeigen soll, ist spezieller Code erforderlich, um zu bestimmen, wann der  _parameter lpProgress_ ignoriert werden soll und wann [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md)aufgerufen werden soll.
    
Rufen Sie **IMAPIProgress::SetLimits** auf, um das MAPI_TOP_LEVEL-Flag festzulegen oder zu löschen und lokale und globale Mindest- und Höchstwerte festzulegen. Der Wert der Flags-Einstellung wirkt sich darauf aus, ob das Statusobjekt die minimalen und maximalen Werte als lokal oder global versteht. Wenn das flag MAPI_TOP_LEVEL festgelegt ist, werden diese Werte als global betrachtet und zum Berechnen des Fortschritts für den gesamten Vorgang verwendet. Statusobjekte initialisieren den globalen Minimalwert auf 0 und den globalen Maximalwert auf 1000. 
  
Wenn MAPI_TOP_LEVEL nicht festgelegt ist, werden die Mindest- und Höchstwerte als lokal betrachtet und intern von Anbietern verwendet, um den Fortschritt für untergeordnete Objekte auf niedrigerer Ebene anzuzeigen. Fortschrittsobjekte speichern nur die lokalen Mindest- und Höchstwerte, sodass sie an Anbieter zurückgegeben werden können, wenn **GetMin** und **GetMax** aufgerufen werden. 
  
Die Parameter "Value", "object count" und "object total" werden in die **IMAPIProgress::P Rogress-Methode** eingegeben. Der Wertparameter, eine Zahl, die den Prozentsatz des Fortschritts angibt, ist erforderlich. Wenn das flag MAPI_TOP_LEVEL festgelegt ist, können Sie auch eine Objektanzahl und eine Objektgesamtsumme übergeben. Einige Clients verwenden diese Werte, um einen Ausdruck wie "5 von 10 abgeschlossene Elemente" mit der Statusanzeige anzuzeigen. Der Fortschritt eines Vorgangs kann streng als Prozentsatz oder Prozentsatz und in Bezug auf die Anzahl der Elemente gemeldet werden, die von der zu verarbeitenden Summe verarbeitet wurden. Wenn Sie beispielsweise ein Nachrichtenspeicheranbieter sind und einen Kopiervorgang ausführen, der 10 Ordner kopiert, kann die Statusanzeige dem Benutzer zusätzliche Informationen bereitstellen, indem ein Ausdruck wie "1 von 10", "2 von 10", "3 von 10" usw. angezeigt wird, bis der Vorgang abgeschlossen ist. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Fortschrittsindikatoren](mapi-progress-indicators.md)

