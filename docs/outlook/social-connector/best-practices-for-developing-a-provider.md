---
title: Bewährte Methoden für die Entwicklung eines Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: 'Beachten Sie beim Entwickeln eines Outlook Social Connector 2013 (OSC)-Anbieters die folgenden Methoden:'
ms.openlocfilehash: 6a48a56d8065fb9a176ca6527340c99551cdb52a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425918"
---
# <a name="best-practices-for-developing-a-provider"></a>Bewährte Methoden für die Entwicklung eines Anbieters

Beachten Sie beim Entwickeln eines Outlook Social Connector 2013 (OSC)-Anbieters die folgenden Methoden:
  
- Aus Sicherheitsgründen sollten Anbieter, die mit Servern über das Internet kommunizieren, das HTTPS (Hypertext Transfer Protocol (HTTP) mit Secure Socket Layer (SSL))-Protokoll verwenden. Andernfalls besteht das Risiko, dass e-Mail-Adressen, Aktivitäten für soziale Netzwerke und andere Benutzerdaten während der Übertragung abgefangen oder offen gelegt werden können.
    
- Wenn Sie einen OSC-Anbieter für ein soziales Netzwerk eines Drittanbieters entwickeln, muss Ihr Anbieter die Nutzungsbedingungen für das soziale Netzwerk einhalten.
    
- Um die Größe des Anbieter-Downloadpakets zu minimieren, erstellen Sie den Anbieter mit einem systemeigenen Compiler wie C++ oder einem anderen Tool, das eine COM-Komponente erstellen kann.
    
- Erstellen Sie in Ihrem Anbieter einen eindeutigen Benutzer-Agent, der an das soziale Netzwerk gesendet wird, um Anrufe des Anbieters an das soziale Netzwerk nachzuverfolgen.
    
- Die [ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md) -Methode sollte sich nicht darauf verlassen, das soziale Netzwerk über das Internet aufzurufen, um die Funktionen des Anbieters zu erhalten. Beispielsweise können Benutzer Outlook offline starten; Wenn der OSC **getCapabilities** aufruft und keine Netzwerkverbindung besteht, gibt der getCapabilities-Aufruf keine gültigen XML- **Funktionen** zurück. **** Die bewährte Methode besteht darin, XML- **Funktionen** als Ressource in Ihrem Anbieter zu speichern. 
    
- Ihr OSC-Anbieter kann eine beträchtliche Anzahl von Anrufen an ein soziales Netzwerk generieren. Ziehen Sie in Abhängigkeit von den Nutzungsbedingungen für Ihr soziales Netzwerk das Zwischenspeichern von Freunden in einen Outlook-Ordner in Betracht, um die Anzahl von Anrufen vom OSC zu Ihrem Anbieter zu verringern, und zwar von Ihrem Anbieter zum sozialen Netzwerk.
    
- Office 2013 ist sowohl in 32-Bit-als auch in 64-Bit-Versionen verfügbar. Versionen von Office vor Office 2010 sind nur in einer 32-Bit-Version verfügbar. Die Standardinstallation von Office 2013 auf 64-Bit-Windows ist 32-Bit. Wenn Sie die 64-Bit-Version des mit 64-Bit Office 2013 installierten OSC unterstützen möchten, müssen Sie auch eine 64-Bit-Version Ihres Anbieters freigeben. 
    
## <a name="see-also"></a>Siehe auch

- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)  
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)  
- [Bereitstellen eines Providers](deploying-a-provider.md)  
- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)

