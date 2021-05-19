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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419107"
---
# <a name="mapi-form-servers"></a>MAPI-Formularserver

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Aus Der Sicht des Benutzers ist ein Formular in der Regel ein Eigenschaftenblatt für eine Nachricht oder ein Dateneingabeformular, mit dem Benutzer strukturierte Informationen eingeben können. Es kann sich jedoch um eine beliebige Benutzeroberfläche handelt, die einer Nachrichtenklasse zugeordnet ist. Aus Der Sicht eines Programmierers besteht ein Formular aus:
  
- Ein Typ von MAPI-Nachricht mit eigener Nachrichtenklasse und OLE-ID.
    
- Die ausführbare Datei, die den Formularserver implementiert.
    
- Eine Auflistung von MAPI-Eigenschaften – benutzerdefinierter oder anderweitiger Art –, die vom Formularserver verwendet werden. Einige oder alle dieser Funktionen stehen Messagingclients möglicherweise zur Verwendung zur Verfügung.
    
- Die Konfigurationsdatei, die das Formular beschreibt und vom Formular-Manager verwendet wird.
    
Da Formulare [IMessage-Objekte](imessageimapiprop.md) sind, weisen sie Eigenschaften und Verhaltensweisen auf, die mit MAPI-Nachrichtenobjekten konsistent sind. Da Formulare jedoch über benutzerdefinierte Eigenschaften, Steuerelemente und ein anwendungsspezifisches Anzeigerendering verfügen können, sind die von Formularen verwendeten MAPI-Schnittstellen generisch genug, um eine beliebige Art von Schnittstelle zu ermöglichen, die benötigt wird. Die tatsächliche Definition eines Formulars wird in einer Formularbibliothek gespeichert, die weiter später in diesem Abschnitt erläutert wird. 
  
> [!NOTE]
> Genauer gesagt sind alle Nachrichten Instanzen von MAPI-Formularen. In der Regel ist es jedoch einfacher, benutzerdefinierte Formulare als Sonderfälle von Nachrichten zu verwenden, da Formulare zum Verfassen und Lesen typischer E-Mail-Nachrichten die am häufigsten verwendeten Formulare sind. Die Tatsache, dass alle Nachrichten wirklich nur Formulare sind, gibt benutzerdefinierten Formularen den gleichen Status wie jede andere Nachricht im MAPI-System. 
  
Jedes Formular verfügt über eine Reihe von Eigenschaften, von denen einige auf der Benutzeroberfläche des Formulars sichtbar sind. In der Regel werden Eigenschaften mit Feldern auf der Benutzeroberfläche des Formulars übereinstimmen. Beispielsweise kann ein Bestellformular die Felder Item, Description, Price, Tax und Subtotal enthalten. Diese Felder sind einfach visuelle Renderings von Formulareigenschaften mit denselben Namen. Clients ermitteln, welche Eigenschaften von einer bestimmten Nachrichtenklasse über die [IMAPIFormInfo::CalcFormPropSet-Methode](imapiforminfo-calcformpropset.md) unterstützt werden, die vom MAPI-Formular-Manager implementiert wird. 
  
Wie grundlegende Nachrichten können MAPI-Formulare alle Standardnachrichteneigenschaften enthalten, z. B. den Absender, den beabsichtigten Empfänger und das Senden der Nachricht. Formulare können auch eine beliebige Anzahl benutzerdefinierter Eigenschaften enthalten, die für das Formular spezifisch sind. Beispielsweise kann ein Formular "Fehlerbericht" benutzerdefinierte Eigenschaften für Fehlertyp, Fehlerschweregrad und Produktversion enthalten.
  
Zum Erstellen eines Formulars müssen Sie einen Formularserver implementieren. Der Formularserver ist die ausführbare Datei, die geladen wird, wenn ein Messagingclient eine Nachricht anzeigen muss, die dem vom Formularserver unterstützten Typ entspricht. Der Formularserver erstellt wiederum Formularobjekte nach Bedarf, um bestimmte Nachrichten anzeigen und Benutzerinteraktionen mit diesen Nachrichten verarbeiten zu können.
  
Jedem Formularserver ist eine Konfigurationsdatei zugeordnet. Diese Datei enthält Informationen, die den Formularserver zum Nutzen des Formular-Managers beschreiben. Der Formular-Manager verwendet diese Informationen beim Installieren des Formularservers in einer Formularbibliothek.
  
Weitere Informationen zum Erstellen der Teile eines Formulars finden Sie unter [Developing MAPI Form Servers](developing-mapi-form-servers.md).
  
Formularserver halten sich an das Component Object Model (COM). Formularserver werden als eigenständige ausführbare Dateien ausgeführt, nicht als In-Proc-Server. Weitere Informationen finden Sie im Abschnitt COM und ActiveX Object Services im Windows SDK.
  
Ein eindeutiger Klassenbezeichner (UNIQUE Class Identifier, CLSID) identifiziert jeden Formularserver. Es gibt immer eine 1:1-Zuordnung zwischen einem Klassenbezeichner und seiner Nachrichtenklasse. Dies bedeutet jedoch nicht, dass ein Formularserver nur mit Nachrichten einer Nachrichtenklasse funktionieren kann. Wenn kein Formularserver für den Dienst einer Nachricht einer bestimmten Klasse verfügbar ist, sollte der verwendete Formular-Manager versuchen, einen Formularserver für eine Nachrichtenklasse zu finden, die höher in der Nachrichtenklassenhierarchie ist. Der standardmäßige Formular-Manager, der mit dem Windows SDK bereitgestellt wird, führt dies aus. Ein solcher Formularserver kann wahrscheinlich nur eine Teilmenge der Eigenschaften der Nachricht rendern (die von der Superklasse unterstützten), aber er ist besser als nichts. Was geschieht, wenn überhaupt kein übereinstimmender Formularserver gefunden wird, ist ein implementierungsspezifisches Detail für den verwendeten Formular-Manager. Der Standardformular-Manager öffnet in diesem Fall keine Nachrichten.
  
Weitere Informationen finden Sie unter [MAPI Message Classes](mapi-message-classes.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

