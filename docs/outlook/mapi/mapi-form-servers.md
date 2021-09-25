---
title: MAPI-Formularserver
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 855292b8-028e-4c1e-87ed-3f20b9ba584a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 10c71c9cebcc66542846c0631be31d6a893d82f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561242"
---
# <a name="mapi-form-servers"></a>MAPI-Formularserver

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Aus Sicht des Benutzers ist ein Formular in der Regel ein Eigenschaftenblatt für eine Nachricht oder ein Dateneingabeformular, mit dem Benutzer strukturierte Informationen eingeben können. Es kann jedoch eine beliebige Benutzeroberfläche sein, die einer Nachrichtenklasse zugeordnet ist. Aus der Sicht eines Programmierers besteht ein Formular aus:
  
- Ein Typ von MAPI-Nachricht mit eigener Nachrichtenklasse und OLE-ID.
    
- Die ausführbare Datei, die den Formularserver implementiert.
    
- Eine Sammlung benutzerdefinierter oder anderweitig verwendeter MAPI-Eigenschaften, die vom Formularserver verwendet werden. Einige oder alle sind möglicherweise für Messagingclients verfügbar.
    
- Die Konfigurationsdatei, die das Formular beschreibt und vom Formular-Manager verwendet wird.
    
Da Formulare [IMessage-Objekte](imessageimapiprop.md) sind, weisen sie Eigenschaften und Verhalten auf, die mit MAPI-Nachrichtenobjekten konsistent sind. Da Formulare jedoch benutzerdefinierte Eigenschaften, Steuerelemente und ein anwendungsspezifisches Anzeigerendering aufweisen können, sind die von Formularen verwendeten MAPI-Schnittstellen generisch genug, um alle erforderlichen Schnittstellen zuzulassen. Die tatsächliche Definition eines Formulars wird in einer Formularbibliothek gespeichert, die weiter unten in diesem Abschnitt erläutert wird. 
  
> [!NOTE]
> Genauer gesagt sind alle Nachrichten Instanzen von MAPI-Formularen. In der Regel ist es jedoch einfacher, sich benutzerdefinierte Formulare als Sonderfälle von Nachrichten vorzustellen, da Formulare zum Verfassen und Lesen von typischen E-Mail-Nachrichten die am häufigsten verwendeten Formulare sind. Die Tatsache, dass alle Nachrichten nur Formulare sind, gibt benutzerdefinierten Formularen den gleichen Status wie jede andere Nachricht im MAPI-System. 
  
Jedes Formular verfügt über eine Reihe von Eigenschaften, von denen einige auf der Benutzeroberfläche des Formulars sichtbar sind. In der Regel werden Eigenschaften mit Feldern in der Benutzeroberfläche des Formulars abgeglichen. Ein Bestellformular kann beispielsweise die Felder Item, Description, Price, Tax und Subtotal enthalten. Bei diesen Feldern handelt es sich lediglich um visuelle Renderings von Formulareigenschaften mit denselben Namen. Clients ermitteln, welche Eigenschaften von einer bestimmten Nachrichtenklasse über die [IMAPIFormInfo::CalcFormPropSet-Methode](imapiforminfo-calcformpropset.md) unterstützt werden, die vom MAPI-Formular-Manager implementiert wird. 
  
Wie grundlegende Nachrichten können MAPI-Formulare alle Standardnachrichteneigenschaften enthalten, z. B. den Absender, den beabsichtigten Empfänger und den Zeitpunkt, zu dem die Nachricht gesendet wurde. Formulare können auch eine beliebige Anzahl benutzerdefinierter Eigenschaften enthalten, die für das Formular spezifisch sind. Ein Formular "Fehlerbericht" kann beispielsweise benutzerdefinierte Eigenschaften für Bugtyp, Fehlerschweregrad und Produktversion enthalten.
  
Zum Erstellen eines Formulars müssen Sie einen Formularserver implementieren. Der Formularserver ist die ausführbare Datei, die geladen wird, wenn ein Messagingclient eine Nachricht anzeigen muss, die dem vom Formularserver unterstützten Typ entspricht. Der Formularserver erstellt wiederum Formularobjekte nach Bedarf, um bestimmte Nachrichten anzuzeigen und Benutzerinteraktionen mit diesen Nachrichten zu verarbeiten.
  
Jedem Formularserver ist eine Konfigurationsdatei zugeordnet. Diese Datei enthält Informationen, die den Formularserver zum Vorteil des Formular-Managers beschreiben. Der Formular-Manager verwendet diese Informationen beim Installieren des Formularservers in einer Formularbibliothek.
  
Ausführliche Informationen zum Erstellen der Teile eines Formulars finden Sie unter [Entwickeln von MAPI-Formularservern.](developing-mapi-form-servers.md)
  
Formularserver entsprechen dem Component Object Model (COM). Formularserver werden als eigenständige ausführbare Dateien und nicht als In-Proc-Server ausgeführt. Weitere Informationen finden Sie im Abschnitt COM und ActiveX Object Services im Windows SDK.
  
Ein eindeutiger Klassenbezeichner (UNIQUE Class Identifier, CLSID) identifiziert jeden Formularserver. Es gibt immer eine 1:1-Zuordnung zwischen einem Klassenbezeichner und dessen Nachrichtenklasse. Dies bedeutet jedoch nicht, dass ein Formularserver nur mit Nachrichten einer Nachrichtenklasse arbeiten kann. Wenn kein Formularserver zum Warten einer Nachricht einer bestimmten Klasse verfügbar ist, sollte der verwendete Formular-Manager versuchen, einen Formularserver für eine Nachrichtenklasse zu finden, die in der Nachrichtenklassenhierarchie höher ist. Dies geschieht durch den mit dem Windows SDK bereitgestellten Standardformular-Manager. Ein solcher Formularserver kann wahrscheinlich nur eine Teilmenge der Nachrichteneigenschaften rendern (diejenigen, die von der Oberklasse unterstützt werden), aber er ist besser als nichts. Was geschieht, wenn überhaupt kein übereinstimmender Formularserver gefunden wird, ist ein spezifisches Implementierungsdetail für den verwendeten Formular-Manager. Der Standardformular-Manager öffnet in diesem Fall keine Nachrichten.
  
Weitere Informationen finden Sie unter [MAPI-Nachrichtenklassen.](mapi-message-classes.md)
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

