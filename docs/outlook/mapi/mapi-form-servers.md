---
title: MAPI-Formularserver
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 855292b8-028e-4c1e-87ed-3f20b9ba584a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3c95f6a1d4d50dd6552c6e786d17c40da14f3f3c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351485"
---
# <a name="mapi-form-servers"></a>MAPI-Formularserver

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Aus Sicht des Benutzers ist ein Formular in der Regel ein Eigenschaftenblatt für eine Nachricht oder ein Dateneingabeformular, mit dem Benutzer strukturierte Informationen eingeben können. Dabei kann es sich jedoch um eine beliebige Benutzeroberfläche handeln, die einer Nachrichtenklasse zugeordnet ist. Aus der Sicht des Programmierers besteht ein Formular aus:
  
- Ein Typ von MAPI-Nachricht mit einer eigenen Nachrichtenklasse und OLE-Bezeichner.
    
- Die ausführbare Datei, die den Formularserver implementiert.
    
- Eine Sammlung von MAPI-Eigenschaften, die vom Formularserver verwendet werden. Einige oder alle diese können für Messaging-Clients zur Verfügung stehen.
    
- Die Konfigurationsdatei, die das Formular beschreibt und vom Formular-Manager verwendet wird.
    
Da Formulare [IMessage](imessageimapiprop.md) -Objekte sind, weisen Sie Eigenschaften und Verhalten auf, die mit MAPI-Nachrichtenobjekten konsistent sind. Da Formulare jedoch benutzerdefinierte Eigenschaften, Steuerelemente und eine anwendungsspezifische Darstellung aufweisen können, sind die MAPI-Schnittstellen, die Formulare verwenden, generisch genug, um eine beliebige Schnittstelle zu ermöglichen, die erforderlich ist. Die tatsächliche Definition eines Formulars wird in einer Formularbibliothek gespeichert, die weiter unten in diesem Abschnitt erläutert wird. 
  
> [!NOTE]
> Genauer gesagt, sind alle Nachrichten Instanzen von MAPI-Formularen. In der Regel ist es jedoch einfacher, benutzerdefinierte Formulare als Sonderfälle von Nachrichten zu betrachten, da Formulare zum Erstellen und lesen typischer e-Mail-Nachrichten die am häufigsten verwendeten Formulare sind. Die Tatsache, dass alle Nachrichten wirklich nur Formulare sind, ermöglicht benutzerdefinierten Formularen den gleichen Status wie jede andere Nachricht im MAPI-System. 
  
Jedes Formular verfügt über eine Reihe von Eigenschaften, von denen einige in der Benutzeroberfläche des Formulars sichtbar sind. In der Regel werden die Eigenschaften mit Feldern in der Benutzeroberfläche des Formulars abgeglichen. Ein Bestellformular kann beispielsweise die Felder Item, Description, Price, Tax und subTotal enthalten. Diese Felder sind einfach visuelle Renderings von Formulareigenschaften mit denselben Namen. Clients ermitteln, welche Eigenschaften von einer bestimmten Nachrichtenklasse unterstützt werden, über die [IMAPIFormInfo:: CalcFormPropSet](imapiforminfo-calcformpropset.md) -Methode, die vom MAPI-Formular-Manager implementiert wird. 
  
Wie grundlegende Nachrichten können MAPI-Formulare alle Standardnachrichteneigenschaften wie den Absender, den beabsichtigten Empfänger und den Zeitpunkt enthalten, zu dem die Nachricht gesendet wurde. Formulare können auch eine beliebige Anzahl von benutzerdefinierten Eigenschaften enthalten, die für das Formular spezifisch sind. Beispielsweise kann ein Formular "Bug Report" benutzerdefinierte Eigenschaften für Bug-, Bug-und Produktversionen enthalten.
  
Zum Erstellen eines Formulars müssen Sie einen Formularserver implementieren. Der Formularserver ist die ausführbare Datei, die geladen wird, wenn ein Messaging Client eine Nachricht anzeigen muss, die vom Formularserver unterstützt wird. Der Formularserver erstellt wiederum Formularobjekte nach Bedarf, um bestimmte Nachrichten anzuzeigen und Benutzerinteraktionen mit diesen Nachrichten zu behandeln.
  
Jedem Formularserver ist eine Konfigurationsdatei zugeordnet. Diese Datei enthält Informationen, die den Formularserver zum Nutzen des Formular-Managers beschreiben. Der Formular-Manager verwendet diese Informationen, wenn der Formularserver in einer Formularbibliothek installiert wird.
  
Ausführliche Informationen zum Erstellen der Teile eines Formulars finden Sie unter [developING MAPI Form Servers](developing-mapi-form-servers.md).
  
Formularserver befolgen das Component Object Model (COM). Formularserver werden als eigenständige ausführbare Dateien ausgeführt, nicht als in-proc-Server. Weitere Informationen finden Sie im Abschnitt COM-und ActiveX-Objektdienste im Windows SDK.
  
Jeder Formularserver wird durch eine eindeutige Klassen-ID (CLSID) identifiziert. Es gibt immer eine 1:1-Zuordnung zwischen einem Klassenbezeichner und seiner Nachrichtenklasse. Dies bedeutet jedoch nicht, dass ein Formularserver nur mit Nachrichten einer Nachrichtenklasse arbeiten kann. Wenn kein Formularserver für die Zustellung einer Nachricht einer bestimmten Klasse verfügbar ist, sollte der verwendete Formular-Manager versuchen, einen Formularserver für eine Nachrichtenklasse zu finden, die höher in der Nachrichtenklassen Hierarchie ist. der mit dem Windows SDK mitgelieferte Standardformular-Manager macht dies. Ein solcher Formularserver kann wahrscheinlich nur eine Teilmenge der Eigenschaften der Nachricht Rendern (die von der übergeordneten Klasse unterstützt), aber es ist besser als Nothing. Was geschieht, wenn kein übereinstimmender Formularserver gefunden wird, ist ein Implementierungsdetail, das für den verwendeten Formular-Manager spezifisch ist. Wenn dies der Fall ist, werden vom standardmäßigen Formular-Manager keine Nachrichten geöffnet.
  
Weitere Informationen finden Sie unter [MAPI Message Classes](mapi-message-classes.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

