---
title: MAPI-Fortschritt-Objekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e446004e-1ef2-4e58-b764-de7b4dcefaf1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c6079a62464231536c0fa6b5bacc291997fe38d9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567923"
---
# <a name="mapi-progress-objects"></a>MAPI-Fortschritt-Objekte

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Mit den Methoden und Daten eines Objekts des Fortschritts können Sie steuern, wie das Symbol Fortschritt meldet. Obwohl ein Client oder MAPI-Fortschritt-Objekt implementiert wird, die meisten von der Last sicherstellen, dass die Richtigkeit der Fortschrittsanzeige greift auf Dienstanbieter ab. Durch Angeben einer bestimmten Reihenfolge und der Wert für die Parameter, die an die Methoden des Fortschritts-Objekts übergeben werden, können Sie seine Genauigkeit sicherstellen.
  
Fortschritt-Objekte werden die folgenden Parameter übergeben:
  
- Eine Bitmaske von Flags, die mit [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) festgelegt und mit [IMAPIProgress::GetFlags](imapiprogress-getflags.md)abgerufen.
    
- Ein Mindestwert (lokaler und globaler) mit **SetLimits** festgelegt und mit [IMAPIProgress::GetMin](imapiprogress-getmin.md)abgerufen.
    
- Ein Höchstwert (lokaler und globaler) mit **SetLimits** festgelegt und mit [IMAPIProgress::GetMax](imapiprogress-getmax.md)abgerufen.
    
- Ein Wert, der angibt, die aktuelle Prozentwert der Fertigstellung des Vorgangs an [IMAPIProgress::Progress](imapiprogress-progress.md)übergeben.
    
- Die Anzahl der Objekte, die bisher verarbeitet wurden, an den **Fortschritt**übergeben.
    
- Anzahl der Gesamtanzahl der Objekte beteiligt, an den **Fortschritt**übergeben.
    
Alle-Dienstanbieter beginnen, ihre Fortschrittsanzeige Verarbeitung mit einem Aufruf von **IMAPIProgress::GetFlags** zum Abrufen vorhanden Flags festlegen. Die Kennzeichen können derzeit nur für MAPI_TOP_LEVEL festgelegt werden. Clients und MAPI-initialisieren das Flag MAPI_TOP_LEVEL, auf Dienstanbieter, ihn bei Bedarf zu löschen. 
  
Der Wert des Flags wird auf MAPI_TOP_LEVEL festgelegt, während der Arbeit mit Objekt der obersten Ebene des Vorgangs. Das übergeordnete Objekt ist das Objekt, das vom Client zum Beginnen eines Vorgangs aufgerufen wird. In einem Ordnerkopiervorgang ist dies der Ordner kopiert werden. In einem Ordner löschen-Vorgang ist dies der Ordner gelöscht wird. Wenn Sie einen Anruf an den Prozess eine niedrigere Level-Objekt oder Unterobjekts, deaktivieren Sie den Wert des Flags vornehmen. In sind einem Ordner kopieren Unterobjekte die Unterordner im Ordner kopiert werden. 
  
MAPI ermöglicht es Ihnen, unterscheiden von Objekten auf oberster Ebene und Unterobjekte mit dem MAPI_TOP_LEVEL-Flag, damit alle Objekte in einem Vorgang beteiligt können die gleiche [IMAPIProgress](imapiprogressiunknown.md) Implementierung Fortschritt, und verursacht dadurch so an, Symbol anzuzeigen Fahren Sie fort reibungslos in einer positive Richtung. Unabhängig davon, ob das MAPI_TOP_LEVEL-Flag festgelegt ist und wirkt sich auf die Einstellungen der anderen Parameter in nachfolgenden Aufrufe an das Objekt ausgeführt. 
  
Da nicht trivialen entsprechenden Parameterwerte für eine Fortschrittsanzeige auf allen Ebenen eines Vorgangs mit mehreren Ebenen festgelegt werden kann, festlegen, dass einige Dienstanbieter keine Fortschritt für Unterobjekte anzuzeigen. 
  
 **Um zu verhindern, dass der Fortschritt für Unterobjekte**
  
- Übergeben Sie NULL für den _LpProgress_ -Parameter im Aufruf ein Unterobjekt verarbeiten. Wenn Sie Ordner kopieren, ist dies der Anruf an einen Unterordner [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) -Methode. 
    
- Schreiben von speziellen Code zum bestimmen, wie den Parameter _LpProgress_ interpretiert werden. Da ein NULL-Wert für den Parameter _LpProgress_ auch bedeutet, dass der Client Fortschritt angezeigt werden soll, mithilfe der MAPI-Implementierung, ist die spezieller Code erforderlich sind, um zu bestimmen, wann den Parameter _LpProgress_ ignorieren und wann [aufrufen IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md).
    
Rufen Sie **IMAPIProgress::SetLimits** festlegen oder Entfernen des Kennzeichens MAPI_TOP_LEVEL und lokaler und globaler minimale und maximale Werte festlegen. Der Wert der Einstellung wirkt sich auf gibt an, ob Flags versteht Fortschritt-Objekt die minimale und maximale Werte lokal oder global sein. Wenn das Flag MAPI_TOP_LEVEL festgelegt ist, werden diese Werte als global gelten und werden verwendet, um den Status für den gesamten Vorgang zu berechnen. Fortschritt Objekte Initialisieren der globalen Mindestwert 0 und der globalen Höchstwert bis 1000. 
  
Wenn MAPI_TOP_LEVEL nicht festgelegt ist, wird die minimale und maximale Werte gelten als lokale und werden intern von Anbietern verwendet, um den Fortschritt für unteren Ebene Unterobjekte anzuzeigen. Fortschritt Objekte speichern die lokalen minimale und maximale Werte, sodass sie-Anbieter zurückgegeben werden können, wenn **GetMin** und **GetMax** aufgerufen werden. 
  
Der Wert, Anzahl der Objekte und Objekt insgesamt Parameter dienen als Eingabe für die **IMAPIProgress::Progress** -Methode. Der Value-Parameter, eine Zahl, die den Prozentsatz des Fortschritts, gibt ist erforderlich. Wenn das Flag MAPI_TOP_LEVEL festgelegt ist, können Sie auch die Anzahl der Objekte und ein Objekt insgesamt übergeben. Einige Clients verwenden diese Werte, um einen Ausdruck wie "5 Elemente nicht genügend 10 abgeschlossen" mit der Statusanzeige anzuzeigen. Fortschritt eines Vorgangs kann ausschließlich gemeldet werden, als Prozentsatz oder als Prozentsatz und im Hinblick auf die Anzahl der Elemente, die von der insgesamt zu verarbeitenden verarbeitet wurden. Beispielsweise kann, wenn Sie einen Anbieter für die Nachricht anmelden und Sie einen Kopiervorgang, der Kopieren von 10 Ordner durchgeführt werden, die Statusanzeige den Benutzer mit zusätzlichen Informationen bereitstellen, indem einen Ausdruck wie "1-10", "2 von 10", "3 von 10" anzeigen , und so weiter, bis der Vorgang abgeschlossen ist. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Statusanzeigen](mapi-progress-indicators.md)

