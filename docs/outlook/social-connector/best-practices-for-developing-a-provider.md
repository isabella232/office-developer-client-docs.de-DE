---
title: Bewährte Methoden für das Entwickeln eines Providers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: 'Sie sollten die folgenden Methoden bei der Entwicklung eines Outlook Social Connector 2013 (OSC)-Anbieters erfüllen:'
ms.openlocfilehash: a6ee9d54f33bbc855d178aba844a8f65ec92f964
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795950"
---
# <a name="best-practices-for-developing-a-provider"></a>Bewährte Methoden für das Entwickeln eines Providers

Sie sollten die folgenden Methoden bei der Entwicklung eines Outlook Social Connector 2013 (OSC)-Anbieters erfüllen:
  
- Aus Sicherheitsgründen sollten Rollenanbieter, die Kommunikation über das Internet mit Servern das Protokoll HTTPS (Hypertext Transfer Protocol (HTTP) mit Secure Socket Layer (SSL)) verwenden. Anderenfalls besteht ein Risiko dar, ob e-Mail-Adressen, Aktivitäten für soziale Netzwerke und anderer Benutzer Daten abgefangen oder unterwegs verfügbar gemacht werden können.
    
- Wenn Sie einen OSC-Anbieter für ein Drittanbieter-soziales Netzwerk entwickeln, muss der Anbieter Vertragsbedingungen für das soziale Netzwerk entsprechen.
    
- Um die Größe des Downloadpakets Anbieter zu minimieren, erstellen Sie den Anbieter mit einem systemeigenen Compiler wie C++ oder ein anderes Programm, das eine COM-Komponente erstellen kann.
    
- Erstellen Sie in Ihren Anbieter einen eindeutigen Benutzer-Agent, der zum Nachverfolgen von Aufrufe durch den Anbieter für soziale Netzwerke in sozialen Netzwerken gesendet wird.
    
- Die Methode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) sollten nicht zum Aufrufen von sozialen Netzwerk über das Internet zum Abrufen der Funktionalität des Anbieters verlassen. Beispielsweise können Benutzer offline Starten von Outlook; Wenn die OSC- **GetCapabilities Anrufe** , und es keine Verbindung zum Netzwerk wird, wird der Anruf **GetCapabilities** keine gültige **Funktionen** XML zurück. Bewährt hat sich zum Speichern von **Funktionen** XML als Ressource in Ihrem Anbieter. 
    
- Ihre OSC-Anbieter kann Anrufe mit einem sozialen Netzwerk umfangreichem generieren. Erwägen Sie je nach der rechtlichen Hinweise für das soziale Netzwerk Zwischenspeichern Freunde zu einem Outlook-Ordner, um die Anzahl der Anrufe von der OSC an Ihren Anbieter und wiederum von Ihrem Anbieter in sozialen Netzwerken reduziert.
    
- Office 2013 ist in 32-Bit- und 64-Bit-Versionen verfügbar. Office prior to Office 2010-Versionen stehen nur in einer 32-Bit-Version zur Verfügung. Die Standardinstallation von Office 2013 64-Bit-Version von Windows ist 32-Bit. Wenn Sie beabsichtigen, die 64-Bit-Version von der OSC zu unterstützen, die mit Office 2013 64-Bit-Version installiert ist, müssen Sie auch eine 64-Bit-Version des Anbieters freigeben. 
    
## <a name="see-also"></a>Siehe auch

- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)  
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)  
- [Bereitstellen eines Providers](deploying-a-provider.md)  
- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)

