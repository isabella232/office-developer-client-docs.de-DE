---
title: MAPI-Formular-Servern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 855292b8-028e-4c1e-87ed-3f20b9ba584a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0b73e246ad5e396ef67e89bff5f1e04a47f6ebcb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569925"
---
# <a name="mapi-form-servers"></a>MAPI-Formular-Servern

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Aus Sicht des Benutzers ist ein Formular in der Regel ein Eigenschaftenblatt für eine Nachricht oder ein Formular zur Dateneingabe, mit dem Benutzer strukturierten Informationen eingeben kann. Es kann jedoch Benutzeroberfläche, die eine Nachrichtenklasse zugeordnet ist. Aus Sicht des ein Programmierer besteht aus einem Formular:
  
- Ein Typ von MAPI-Nachricht mit einem eigenen Nachrichtenklasse und OLE-Bezeichner.
    
- Die ausführbare Datei, die den Formular Server implementiert wird.
    
- Eine Auflistung von MAPI-Eigenschaften – benutzerdefinierte oder anderweitig –, die der Formular Server verwendet. Einige oder alle dieser möglicherweise messaging-Clients für die Verwendung zur Verfügung.
    
- Die Konfigurationsdatei, die beschreibt des Formulars und wird von der Formular-Manager.
    
Da Formulare [IMessage](imessageimapiprop.md) -Objekte sind, verfügen sie über Eigenschaften und Verhalten, das mit MAPI-Message Objekte konsistent ist. Da Formulare haben können benutzerdefinierte Eigenschaften, Steuerelemente und eine Anzeige gerendert, in der anwendungsspezifische ist, sind die MAPI-Schnittstellen, die mit forms generisch genug gestatten irgendeine der Schnittstelle, die benötigt werden. Die tatsächliche Definition eines Formulars wird in einer Formularbibliothek gespeichert, der weiter unten in diesem Abschnitt erläutert wird. 
  
> [!NOTE]
> Genauer gesagt, werden alle Nachrichten werden Instanzen des MAPI-Formulare. Jedoch ist es in der Regel einfacher als Sonderfälle von Nachrichten, seit Formularen zum Verfassen von benutzerdefinierten Formularen vorstellen, und Lesen Standard-e-Mail-Nachrichten werden die am häufigsten Formulare verwendeten. Die Tatsache, dass alle Nachrichten wirklich nur Formulare gibt benutzerdefinierte sind forms denselben Status wie alle anderen Nachrichten im MAPI-System. 
  
Jedes Formular verfügt über eine Reihe von Eigenschaften, von die einige in der Benutzeroberfläche des Formulars angezeigt werden. In der Regel werden die Eigenschaften für Felder in der Benutzeroberfläche des Formulars abgeglichen. Beispielsweise könnte ein Formular Purchase Order die Felder Element, Beschreibung, Preis, steuern und Teilergebnis aufweisen. Diese Felder sind einfach visual Anzeigen der Eigenschaften des Formulars mit den gleichen Namen. Clients festzustellen, welche Eigenschaften von einer bestimmten Nachrichtenklasse durch die Methode [IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md) unterstützt werden die von der MAPI-Formular-Manager implementiert wird. 
  
MAPI-Formulare können grundlegende Nachrichten, die standard-Nachrichteneigenschaften wie den Absender des Empfängers enthalten und wenn die Nachricht gesendet wurde. Formulare können auch eine beliebige Anzahl von benutzerdefinierten Eigenschaften enthalten, die Sie dem Formular spezifisch sind. Beispielsweise kann ein Formular "Fehlerbericht" benutzerdefinierte Eigenschaften für den Fehlertyp, Schweregrad und Version des Produkts enthalten.
  
Um ein Formular erstellen, müssen Sie einen Formular Server implementieren. Der Formular-Server ist die ausführbare Datei aus, die geladen wird, wenn ein messaging-Client muss eine Meldung angezeigt, die den Typ, der vom Formular Server unterstützt wird. Der Formular-Server erstellt wiederum Formularobjekte nach Bedarf zum Anzeigen bestimmter Nachrichten und Benutzerinteraktionen mit diesen Nachrichten behandeln.
  
Jedes Formular Server verfügt über eine Konfigurationsdatei zugeordnet. Diese Datei enthält Informationen, die den Formular Server für den Formular-Manager beschreibt. Der Formular-Manager verwendet diese Informationen bei der Installation des Servers Formular in einer Formularbibliothek.
  
Weitere Informationen zum Erstellen von der Teilen eines Formulars finden Sie unter [Entwickeln von MAPI-Formulars Servern](developing-mapi-form-servers.md).
  
Formular Servern entsprechen an Component Object Model (COM). Bilden von Servern, die als eigenständige ausführbare Datei, nicht als prozessinternen Server ausgeführt. Weitere Informationen finden Sie unter den Abschnitt COM und ActiveX-Objekt Services im Windows SDK.
  
Eine eindeutige Klassen-ID (CLSID) identifiziert jedes Formular-Server. Es ist immer eine Zuordnung zwischen einem Klassenbezeichner und deren Nachrichtenklasse. Dies bedeutet nicht jedoch, dass ein Formular Server nur mit einer Nachrichtenklasse Nachrichten arbeiten kann. Wenn kein Server Formular für eine Nachricht einer bestimmten Klasse service verfügbar ist, sollte der Formular-Manager verwendeten versuchen, ein Formular für eine Nachrichtenklasse weiter oben in der Nachricht Klassenhierarchie gefunden; der standardmäßigen Formular-Manager mit dem Windows SDK bereitgestellt wird. Ein solcher Formular Server werden wahrscheinlich nur eine Teilmenge der Nachrichteneigenschaften (derjenigen, die von der übergeordneten Klasse unterstützt) gerendert ist, es aber besser als nichts. Was geschieht, wenn kein übereinstimmender Formular Server überhaupt gefunden wird ist Implementierungsdetail an den Formular-Manager verwendet wird. der Standard-Formular-Manager wird Nachrichten nicht geöffnet, wenn dies der Fall ist.
  
Weitere Informationen finden Sie unter [MAPI Message Classes](mapi-message-classes.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

