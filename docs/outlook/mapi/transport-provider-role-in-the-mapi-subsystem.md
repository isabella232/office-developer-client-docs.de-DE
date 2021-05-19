---
title: Transportanbieterrolle im MAPI-Subsystem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7659369a-0952-4f5a-a86b-91958c4c1a3f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7cadb57706e3feec7ed98dd5e4e8d75967036fef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424056"
---
# <a name="transport-provider-role-in-the-mapi-subsystem"></a>Transportanbieterrolle im MAPI-Subsystem
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
DlLs (Dynamic Link Libraries) des Transportanbieters stellen die Schnittstelle zwischen dem MAPI-Spooler und dem Teil eines Messagingsystems bereit, das für das Senden und Empfangen von Nachrichten zuständig ist. Der MAPI-Spooler und der Transportanbieter arbeiten zusammen, um die Verantwortlichkeiten des Sendens einer Nachricht oder des Empfangens einer Nachricht zu übernehmen. Der MAPI-Spooler lädt die Transportanbieter-DLL, wenn sie zum ersten Mal verwendet wird, und gibt sie frei, wenn sie nicht mehr benötigt wird. Mehrere Transportanbieter können auf demselben System installiert werden, aber MAPI stellt den erforderlichen Spooler zur.
  
Clientanwendungen kommunizieren in der Regel nicht direkt mit dem Transportanbieter. Stattdessen senden Clients Nachrichten über einen Speicheranbieter, und der MAPI-Spooler sendet ausgehende Nachrichten an den entsprechenden Transportanbieter und übermittelt eingehende Nachrichten an den entsprechenden Nachrichtenspeicher. Der MAPI-Spooler führt seine Arbeit aus und ruft Transportanbieter auf, wenn sich Vordergrundanwendungen im Leerlauf befinden. Nach der optionalen Anzeige von Dialogfeldern bei der ersten Anmeldung des Transportanbieters werden transportprovider im Hintergrund ausgeführt, es sei denn, der Client wird zum Leeren von Sende- und Empfangswarteschlangen aufgerufen. 
  
Transportanbieter haben in einem MAPI-Messagingsystem die folgenden Zuständigkeiten:
  
- Registrieren Sie die Adresstypen, die sie mit dem MAPI-Spooler akzeptieren können, damit der MAPI-Spooler Nachrichten abhängig von der Zieladresse der Nachrichten an den entsprechenden Transportanbieter übermitteln kann. Ein Transportanbieter kann mehrere Adresstypen registrieren. Transportanbieter können auch die Adressen bestimmter Empfänger mit dem MAPI-Spooler registrieren. Nachrichten, die an eine dieser Adressen adressiert sind, werden an den Transportanbieter übermittelt, der die Adresse beim MAPI-Spooler registriert hat. Weitere Informationen finden Sie [unter Transport Provider and MAPI Spooler Operational Model](transport-provider-and-mapi-spooler-operational-model.md).
    
- Senden eingehender Nachrichten an den MAPI-Spooler. Je nach Art des Messagingsystems kann ein Transportanbieter den MAPI-Spooler entweder direkt benachrichtigen, wenn eine neue Nachricht eintrifft, oder er kann anfordern, dass der MAPI-Spooler den Transportanbieter regelmäßig abruft, um nach neuen Nachrichten zu suchen.
    
- Konvertieren von MAPI-Nachrichteneigenschaften in und von Nachrichteneigenschaften, die für das Messagingsystem nativ sind. Der Transportanbieter muss beispielsweise die Adressen des Absenders und empfängers in einer ausgehenden Nachricht in ein Formular konvertieren, das für das Messagingsystem akzeptabel ist. Einige Messagingsysteme unterstützen nicht alle MAPI-Nachrichteneigenschaften. Weitere Informationen zum Beibehalten von MAPI-Nachrichteneigenschaften beim Senden von Nachrichten an ein Messagingsystem finden Sie unter [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).
    
- Registrieren Von Nachrichten- und Empfängeroptionen, die für den Transportanbieter spezifisch sind.
    
- Führen Sie eine Überprüfung der anmeldeinformationen durch, die vom Messagingsystem erforderlich sind.
    
- Greifen Sie auf ausgehende Nachrichten zu, indem Sie das message-Objekt verwenden, das vom MAPI-Spooler an sie übergeben wird.
    
- Übersetzen Sie das Nachrichtenformat, wie es vom zugrunde liegenden Messagingsystem erforderlich ist.
    
- Benachrichtigen Sie den #A0 darüber, welche Empfänger einer ausgehenden Nachricht der Transportanbieter für die Verarbeitung verantwortlich ist, indem Sie die **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) -Eigenschaft für diese Empfänger festlegen.
    
- Informieren Sie den MAPI-Spooler, wenn eine eingehende Nachricht verarbeitet werden muss.
    
- Übergeben Sie eingehende Nachrichtendaten mithilfe von Nachrichtenobjekten an den MAPI-Spooler.
    
- Zuweisen von Werten zu allen erforderlichen MAPI-Nachrichteneigenschaften für eingehende Nachrichten.
    
- Löschen Sie die Nachricht nach der Zustellung nach Bedarf aus dem zugrunde liegenden Messagingsystem.
    
- Bereitstellen von Statusinformationen für die MAPI-Spooler- und Clientanwendungen.
    
Die folgende Abbildung zeigt die Rolle eines Transportanbieters im Hinblick auf die anderen Komponenten der MAPI-Architektur.
  
**Transportanbieterrolle in einem Messaging-System**
  
![Rolle des Transportanbieters in einem Messagingsystem](media/xp01.gif "Transport provider role in a messaging system")
  

