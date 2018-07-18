---
title: Übersicht über den MAPI-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7cbc79f-3d60-4f21-a378-7b0088ee8ad3
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 15a53a0bb16db3683e4c1320ac2e54648c8c697b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793081"
---
# <a name="mapi-service-provider-overview"></a>Übersicht über den MAPI-Anbieter

  
  
**Betrifft**: Outlook 
  
Zwischen den MAPI-Subsystems und die messaging-Systemen sind die verschiedenen-Dienstanbieter. Dienstanbieter sind wie Treibern, die MAPI-Clientanwendungen mit einem zugrunde liegenden messaging-System eine Verbindung herstellen. Es gibt drei Arten von Anbietern: e-Mail-Anbieter, Adressbuch oder Verzeichnis, und Nachricht Transportanbieter. MAPI unterstützt jede Art von Dienst unabhängig voneinander, aktivieren einen Hersteller, um eine oder mehrere benutzerdefinierte Dienstanbieter anbieten. Beispielsweise könnten ein Hersteller Adressbuch-Dienstanbieter zu erstellen, ein Verzeichnis corporate Telefonbuch der Mitarbeiter verwendet, oder einen Nachrichtenanbieter erstellen, der eine vorhandene Datenbank verwendet wird.
  
Dienstanbieter sind in der Regel für bestimmte Messagingsystemen von Softwareentwicklern, die mit Erfahrung oder Kenntnisse spezielle geschrieben ein bestimmtes System. Beispielsweise verwenden den Microsoft Outlook 2013 und Microsoft Outlook 2010-Mobile-Dienste ein Adressbuchanbieter einer mobilen Adressbuch in Outlook verfügbar machen. 
  
MAPI stellt Clientanwendungen eine einheitliche Ansicht der Address Book und Transport Informationen zu Anbietern. Dieser integrierte Ansatz verhindert, dass die Client-Anwendung müssen Sie sich an den entsprechenden Anbieter zuzuordnen. Es wird auch verhindert, dass den Benutzer zwischen mehreren Adressbuch aushandeln und transport-Anbieter-Adressierungsschemas müssen. Jedoch Speicherinformationen Anbieter Nachricht ist nicht vereinheitlicht und Clients, die mehrere Anbieter Nachricht verwenden die Verantwortung für einzeln berühren.
  
Der Dienstanbieter arbeiten mit MAPI erstellen und Senden von Nachrichten auf folgende Weise: Nachrichten werden mithilfe eines Formulars, die geeignet für den bestimmten Typ oder der Nachricht-Klasse erstellt. Viele Nachrichten werden mit dem Formular standard Hinweis vorgenommen, die im Lieferumfang des MAPI-Subsystems, entweder durch den Benutzer einer Clientanwendung oder programmgesteuert ohne Benutzereingriff. Die abgeschlossene Nachricht an einen oder mehrere Empfänger adressiert ist – einen Benutzer oder eine Gruppe von Benutzern festgelegt und die Nachricht empfängt. Ein Empfänger kann oder möglicherweise keinen Eintrag in einem Verzeichnis, die eines der installierten adressbuchanbietern implementierte besitzt. Empfänger, die nicht mit einer installierten Adressbuchanbieter verknüpft sind werden benutzerdefinierte Empfänger oder einmal-Adressen bezeichnet. Eine einmalige Adresse werden temporäre, dauert nur, bis die Nachricht gesendet wird. 
  
Wenn die Client-Anwendung die Nachricht sendet, der Nachricht Speicheranbieter überprüft, ob jeden Empfänger über eine eindeutige und gültige Adresse verfügt und die Nachricht enthält alle Informationen für die Übertragung erforderlich. Ist eine Frage zu einem Empfänger (beispielsweise, wenn mehrere Empfänger mit dem gleichen Namen vorhanden sind), übernimmt ein Adressbuchanbieter Auflösen der Mehrdeutigkeit von. Die Nachricht wird in der ausgehenden Warteschlange platziert. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Features und die Architektur](mapi-features-and-architecture.md)

