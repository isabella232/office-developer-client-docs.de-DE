---
title: Übersicht über MAPI-Dienstanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e7cbc79f-3d60-4f21-a378-7b0088ee8ad3
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: be2ad66f88b4e357d618286403ebefcb73942103
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595798"
---
# <a name="mapi-service-provider-overview"></a>Übersicht über MAPI-Dienstanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zwischen dem MAPI-Subsystem und den Messagingsystemen befinden sich die verschiedenen Dienstanbieter. Dienstanbieter ähneln Treibern, die MAPI-Clientanwendungen mit einem zugrunde liegenden Messagingsystem verbinden. Es gibt drei Arten von Anbietern: Nachrichtenspeicheranbieter, Adressbuch- oder Verzeichnisanbieter und Nachrichtentransportanbieter. Die MAPI unterstützt jeden Diensttyp unabhängig, sodass ein Anbieter einen oder mehrere benutzerdefinierte Dienstanbieter anbieten kann. Beispielsweise kann ein Anbieter einen Adressbuchanbieter erstellen, der ein Unternehmenstelefonbuchverzeichnis von Mitarbeitern verwendet, oder einen Nachrichtenspeicheranbieter erstellen, der eine vorhandene Datenbank verwendet.
  
Dienstanbieter werden in der Regel für bestimmte Messagingsysteme von Softwareentwicklern geschrieben, die über spezielle Kenntnisse oder Erfahrungen mit einem bestimmten System verfügen. Beispielsweise verwenden die Microsoft Outlook 2013 und Microsoft Outlook 2010 Mobile Services einen Adressbuchanbieter, um ein mobiles Adressbuch in Outlook verfügbar zu machen. 
  
Die MAPI stellt Clientanwendungen eine einheitliche Ansicht der Adressbuch- und Transportanbieterinformationen bereit. Dieser integrierte Ansatz verhindert, dass die Clientanwendung Daten dem entsprechenden Anbieter zuordnen muss. Außerdem wird verhindert, dass der Benutzer zwischen mehreren Adressbuch- und Transportanbieter-Adressierungsschemas aushandeln muss. Nachrichtenspeicheranbieterinformationen sind jedoch nicht vereinheitlicht, und Clients, die mehrere Nachrichtenspeicheranbieter verwenden, sind für die individuelle Verarbeitung verantwortlich.
  
Die Dienstanbieter arbeiten mit MAPI zusammen, um Nachrichten wie folgt zu erstellen und zu senden: Nachrichten werden mithilfe eines Formulars erstellt, das für den jeweiligen Nachrichtentyp oder die jeweilige Klasse der Nachricht geeignet ist. Viele Nachrichten werden mit dem Standardnotizformular erstellt, das im MAPI-Subsystem enthalten ist, entweder vom Benutzer einer Clientanwendung oder programmgesteuert ohne Benutzerinteraktion. Die abgeschlossene Nachricht wird an einen oder mehrere Empfänger adressiert – einen Benutzer oder eine Gruppe von Benutzern, die für den Empfang der Nachricht bestimmt sind. Ein Empfänger verfügt möglicherweise oder nicht über einen Eintrag in einem Verzeichnis, das einer der installierten Adressbuchanbieter besitzt. Empfänger, die keinem installierten Adressbuchanbieter zugeordnet sind, werden als benutzerdefinierte Empfänger oder einmalige Adressen bezeichnet. Eine einmalige Adresse kann temporär sein und nur so lange erhalten bleiben, bis die Nachricht gesendet wird. 
  
Wenn die Clientanwendung die Nachricht sendet, überprüft der Nachrichtenspeicheranbieter, ob jeder Empfänger über eine eindeutige und gültige Adresse verfügt und ob die Nachricht über alle für die Übertragung erforderlichen Informationen verfügt. Wenn es eine Frage zu einem Empfänger gibt (z. B. wenn mehrere Empfänger mit demselben Namen vorhanden sind), kümmert sich ein Adressbuchanbieter um die Auflösung der Zweideutigkeit. Die Nachricht wird dann in der ausgehenden Warteschlange platziert. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Features und -Architektur](mapi-features-and-architecture.md)

