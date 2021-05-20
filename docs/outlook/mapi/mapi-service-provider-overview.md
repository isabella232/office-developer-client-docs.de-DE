---
title: Übersicht über den MAPI-Dienstanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7cbc79f-3d60-4f21-a378-7b0088ee8ad3
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: bc25158daa9579b5cd6cebe1eee878bf087762a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431428"
---
# <a name="mapi-service-provider-overview"></a>Übersicht über den MAPI-Dienstanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zwischen dem MAPI-Subsystem und den Messagingsystemen befinden sich die verschiedenen Dienstanbieter. Dienstanbieter sind wie Treiber, die MAPI-Clientanwendungen mit einem zugrunde liegenden Messagingsystem verbinden. Es gibt drei Arten von Anbietern: Nachrichtenspeicheranbieter, Adressbuch- oder Verzeichnisanbieter und Nachrichtentransportanbieter. MAPI unterstützt jeden Diensttyp unabhängig, sodass ein Anbieter einen oder mehrere benutzerdefinierte Dienstanbieter anbieten kann. Beispielsweise kann ein Anbieter einen Adressbuchanbieter erstellen, der ein Unternehmenstelefonbuchverzeichnis von Mitarbeitern verwendet, oder einen Nachrichtenspeicheranbieter erstellen, der eine vorhandene Datenbank verwendet.
  
Dienstanbieter werden in der Regel von Softwareentwicklern, die über spezielle Kenntnisse oder Erfahrung mit einem bestimmten System verfügen, für bestimmte Messagingsysteme geschrieben. Beispielsweise verwenden die Microsoft Outlook 2013 und Microsoft Outlook 2010 Mobile Services einen Adressbuchanbieter, um ein mobiles Adressbuch in einem Outlook. 
  
MAPI stellt Clientanwendungen eine einheitliche Ansicht von Adressbuch- und Transportanbieterinformationen zur Verfügung. Dieser integrierte Ansatz verhindert, dass die Clientanwendung Dem entsprechenden Anbieter Daten zuordnungen muss. Außerdem wird verhindert, dass der Benutzer zwischen mehreren Adressbuch- und Transportanbieter-Adressierungsschemas verhandeln muss. Informationen des Nachrichtenspeicheranbieters sind jedoch nicht vereinheitlicht, und Clients, die mehrere Nachrichtenspeicheranbieter verwenden, sind für die individuelle Behandlung verantwortlich.
  
Die Dienstanbieter arbeiten mit MAPI zusammen, um Nachrichten auf folgende Weise zu erstellen und zu senden: Nachrichten werden mithilfe eines Formulars erstellt, das für den spezifischen Typ oder die Klasse der Nachricht geeignet ist. Viele Nachrichten werden mit dem Standardnotizformular erstellt, das im MAPI-Subsystem enthalten ist, entweder vom Benutzer einer Clientanwendung oder programmgesteuert ohne Benutzerinteraktion. Die abgeschlossene Nachricht wird an einen oder mehrere Empfänger adressiert, d. h. an einen Benutzer oder eine Gruppe von Benutzern, die für den Empfang der Nachricht bestimmt sind. Ein Empfänger hat möglicherweise einen Eintrag in einem Verzeichnis, das einem der installierten Adressbuchanbieter gehört. Empfänger, die keinem installierten Adressbuchanbieter zugeordnet sind, werden als benutzerdefinierte Empfänger oder sonderangerufene Adressen bezeichnet. Eine einmaladresse kann temporär sein und nur so lange dauern, bis die Nachricht übermittelt wird. 
  
Wenn die Clientanwendung die Nachricht sendet, überprüft der Nachrichtenspeicheranbieter, ob jeder Empfänger über eine eindeutige und gültige Adresse verfügt und dass die Nachricht über alle für die Übertragung erforderlichen Informationen verfügt. Wenn es eine Frage zu einem Empfänger gibt (z. B. wenn es mehrere Empfänger mit demselben Namen gibt), übernimmt ein Adressbuchanbieter die Lösung der Mehrdeutigkeit. Die Nachricht wird dann in der ausgehenden Warteschlange platziert. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Features und -Architektur](mapi-features-and-architecture.md)

