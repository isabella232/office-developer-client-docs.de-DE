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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339970"
---
# <a name="mapi-service-provider-overview"></a>Übersicht über den MAPI-Dienstanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zwischen dem MAPI-Subsystem und den Messagingsystemen sind die verschiedenen Dienstanbieter. Dienstanbieter sind wie Treiber, die MAPI-Clientanwendungen mit einem zugrunde liegenden Messagingsystem verbinden. Es gibt drei Arten von Anbietern: Nachrichtenspeicher Anbieter, Adressbuch-oder Verzeichnis Anbieter und Nachrichtentransport Anbieter. MAPI unterstützt die einzelnen Diensttypen unabhängig und ermöglicht es einem Anbieter, einen oder mehrere benutzerdefinierte Dienstanbieter anzubieten. Ein Kreditor kann beispielsweise einen Adressbuchanbieter erstellen, der ein Unternehmens Telefonbuch-Verzeichnis von Mitarbeitern verwendet oder einen Nachrichtenspeicher Anbieter erstellt, der eine vorhandene Datenbank verwendet.
  
Dienstanbieter werden in der Regel für bestimmte Messagingsysteme von Softwareentwicklern geschrieben, die über spezielle Kenntnisse oder Erfahrungen mit einem bestimmten System verfügen. Beispielsweise verwenden die mobilen Dienste von Microsoft Outlook 2013 und Microsoft Outlook 2010 einen Adressbuchanbieter, um ein mobiles Adressbuch in Outlook verfügbar zu machen. 
  
MAPI präsentiert Clientanwendungen mit einer einheitlichen Ansicht von Adressbuch-und Transportanbieter Informationen. Dieser integrierte Ansatz verhindert, dass die Clientanwendung Daten dem entsprechenden Anbieter zuordnen muss. Außerdem wird verhindert, dass der Benutzer unter mehreren Adressierungsschemas für Adressbücher und Transportanbieter verhandeln muss. Informationen zum Nachrichtenspeicher Anbieter sind jedoch nicht einheitlich, und Clients, die mehrere Nachrichtenspeicher Anbieter verwenden, sind für die individuelle Verarbeitung verantwortlich.
  
Die Dienstanbieter arbeiten mit MAPI, um Nachrichten auf folgende Weise zu erstellen und zu senden: Nachrichten werden mithilfe eines Formulars erstellt, das für den jeweiligen Typ oder die Klasse der Nachricht geeignet ist. Viele Nachrichten werden mit dem standardmäßigen Note-Formular erstellt, das mit dem MAPI-Subsystem geliefert wird, entweder vom Benutzer einer Clientanwendung oder programmgesteuert ohne Benutzerinteraktion. Die abgeschlossene Nachricht wird an einen oder mehrere Empfänger adressiert – einen Benutzer oder eine Gruppe von Benutzern, die für den Empfang der Nachricht bestimmt sind. Ein Empfänger hat möglicherweise einen Eintrag in einem Verzeichnis, der einer der installierten Adressbuchanbieter besitzt. Empfänger, die keinem installierten Adressbuchanbieter zugeordnet sind, werden als benutzerdefinierte Empfänger oder als einmalige Adressen bezeichnet. Eine einmalige Adresse kann nur vorübergehend sein und dauert nur bis zur Übermittlung der Nachricht. 
  
Wenn die Clientanwendung die Nachricht sendet, überprüft der Nachrichtenspeicher Anbieter, ob jeder Empfänger eine eindeutige und gültige Adresse hat und ob die Nachricht alle für die Übertragung erforderlichen Informationen enthält. Wenn es eine Frage zu einem Empfänger gibt (beispielsweise bei mehreren Empfängern mit demselben Namen), sorgt ein Adressbuchanbieter für die Auflösung der Mehrdeutigkeit. Die Nachricht wird dann in der ausgehenden Warteschlange platziert. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Features und -Architektur](mapi-features-and-architecture.md)

