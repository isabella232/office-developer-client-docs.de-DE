---
title: MAPI-fortSchritts Objekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e446004e-1ef2-4e58-b764-de7b4dcefaf1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 73d905028f8f62ad8cbb9da9b1ad61b8cab1065e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340075"
---
# <a name="mapi-progress-objects"></a>MAPI-fortSchritts Objekte

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Mit den Methoden und Daten eines Progress-Objekts können Sie steuern, wie der Indikator den Fortschritt meldet. Obwohl ein Client oder MAPI das Progress-Objekt implementiert, fällt der größte Teil der Last der Sicherstellung der Richtigkeit der Fortschrittsanzeige auf Dienstanbieter. Sie können die Genauigkeit sicherstellen, indem Sie eine bestimmte Reihenfolge und einen bestimmten Wert für die Parameter angeben, die an Progress-Objektmethoden übergeben werden.
  
Die folgenden Parameter werden an Progress-Objekte übergeben:
  
- Eine Bitmaske von Flags, die mit [IMAPIProgress::](imapiprogress-setlimits.md) setlimits festgelegt und mit [IMAPIProgress::](imapiprogress-getflags.md)GetFlags abgerufen werden.
    
- Ein Minimalwert (lokal und Global), festgelegt **** mit setlimits und abgerufen mit [IMAPIProgress:: GetMin](imapiprogress-getmin.md).
    
- Ein Maximalwert (lokal und Global), festgelegt **** mit setlimits und abgerufen mit [IMAPIProgress:: GetMax](imapiprogress-getmax.md).
    
- Ein Wert, der den aktuellen Prozentsatz des Abschlusses des Vorgangs angibt, der an [IMAPIProgress::P rogress](imapiprogress-progress.md)übergeben wird.
    
- Die Anzahl der Objekte, die bisher verarbeitet wurden und an **Progress**übergeben wurden.
    
- Die Anzahl der am Vorgang beteiligten Objekte, die an den **Fortschritt**übergeben wurden.
    
Alle Dienstanbieter beginnen Ihre Statusanzeige Verarbeitung mit einem Aufruf von **IMAPIProgress::** GetFlags zum Abrufen der aktuellen Flags-Einstellung. Derzeit können die Flags nur auf MAPI_TOP_LEVEL festgelegt werden. Clients und MAPI initialisieren die Kennzeichnung für MAPI_TOP_LEVEL, wobei Sie von Dienstanbietern abhängig sind, um Sie bei Bedarf zu löschen. 
  
Der Flags-Wert wird auf MAPI_TOP_LEVEL festgelegt, während Sie mit dem Objekt der obersten Ebene im Vorgang arbeiten. Das Objekt der obersten Ebene ist das Objekt, das vom Client zum Starten eines Vorgangs aufgerufen wird. In einem Ordner Kopiervorgang ist dies der Ordner, der kopiert wird. In einem Ordner Löschvorgang ist dies der Ordner, der gelöscht wird. Wenn Sie einen Aufruf ausführen, um ein Objekt auf niedrigerer Ebene oder ein SubObject zu verarbeiten, löschen Sie den Flags-Wert. In einem Ordner Kopiervorgang sind unter Objekte die Unterordner, die sich im zu kopierenden Ordner befinden. 
  
MAPI ermöglicht es Ihnen, zwischen Objekten auf oberster Ebene und Unterobjekten mit dem MAPI_TOP_LEVEL-Flag zu unterscheiden, sodass alle an einem Vorgang beteiligten Objekte dieselbe [IMAPIProgress](imapiprogressiunknown.md) -Implementierung zum Anzeigen des Fortschritts verwenden können, wodurch die Anzeige des Indikators gehen Sie reibungslos in eine einzige positive Richtung. Ob das MAPI_TOP_LEVEL-Flag festgelegt ist, wirkt sich auf die Einstellungen der anderen Parameter in nachfolgenden Aufrufen des Progress-Objekts aus. 
  
Da es nicht trivial sein kann, geeignete Parameterwerte für eine Statusanzeige auf allen Ebenen eines mehrstufigen Vorgangs festzulegen, wählen einige Dienstanbieter aus, den Fortschritt für unter Objekte nicht anzuzeigen. 
  
 **So vermeiden Sie den Fortschritt für unter Objekte**
  
- Übergeben Sie NULL für den _lpProgress_ -Parameter im Aufruf, um ein Unterobjekt zu verarbeiten. Wenn Sie beispielsweise Ordner kopieren, ist dies der Aufruf der [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md) -Methode eines Unterordners. 
    
- Schreiben Sie speziellen Code, um zu bestimmen, wie der _lpProgress_ -Parameter interpretiert werden soll. Da ein NULL-Wert für den _lpProgress_ -Parameter auch bedeuten kann, dass der Client den Fortschritt mithilfe der MAPI-Implementierung anzeigen soll, ist spezieller Code erforderlich, um zu bestimmen, wann der _lpProgress_ -Parameter ignoriert werden soll und wann er aufgerufen [werden soll. IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md).
    
Rufen Sie **IMAPIProgress::** setlimits auf, um das MAPI_TOP_LEVEL-Flag festzulegen oder zu löschen und lokale und globale Mindest-und Maximalwerte festzulegen. Der Wert der Flags-Einstellung wirkt sich darauf aus, ob das Progress-Objekt den minimal-und Maximalwert für lokal oder Global versteht. Wenn das MAPI_TOP_LEVEL-Flag festgelegt ist, werden diese Werte als Global betrachtet und zum Berechnen des Fortschritts für den gesamten Vorgang verwendet. Progress-Objekte initialisieren den globalen Minimalwert auf 0 und den globalen Maximalwert auf 1000. 
  
Wenn MAPI_TOP_LEVEL nicht festgelegt ist, werden die minimal-und Maximalwerte als lokal betrachtet und intern von Anbietern verwendet, um den Fortschritt für unter Objekte auf niedrigerer Ebene anzuzeigen. Progress-Objekte speichern die lokalen Mindest-und Maximalwerte nur, damit Sie an Anbieter zurückgegeben werden können, wenn **GetMin** und **GetMax** aufgerufen werden. 
  
Die Parameter value, Object Count und Object Total sind Eingabe für die **IMAPIProgress::P rogress** -Methode. Der value-Parameter, eine Zahl, die den Prozentsatz des Fortschritts angibt, ist erforderlich. Wenn das MAPI_TOP_LEVEL-Flag festgelegt ist, können Sie auch eine Objektanzahl und ein Objekt insgesamt. Einige Clients verwenden diese Werte, um einen Ausdruck wie "5 aus 10 abgeschlossenen Elementen" mit der Statusanzeige anzuzeigen. Der Fortschritt eines Vorgangs kann ausschließlich als Prozentsatz oder als Prozentsatz und im Hinblick auf die Anzahl der Elemente, die aus der zu verarbeitenden Summe verarbeitet wurden, angegeben werden. Wenn Sie beispielsweise ein Nachrichtenspeicher Anbieter sind und einen Kopiervorgang durchführen, der 10 Ordner kopiert, kann die Statusanzeige dem Benutzer zusätzliche Informationen zur Verfügung stellen, indem ein Ausdruck wie "1 von 10", "2 von 10", "3 von 10" angezeigt wird. usw., bis der Vorgang abgeschlossen ist. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-fortSchrittsIndikatoren](mapi-progress-indicators.md)

