---
title: Bewährte Methoden für die Entwicklung eines Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: 'Beachten Sie die folgenden Methoden, wenn Sie einen Outlook Social Connector 2013 (OSC) entwickeln:'
ms.openlocfilehash: 6a48a56d8065fb9a176ca6527340c99551cdb52a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425918"
---
# <a name="best-practices-for-developing-a-provider"></a>Bewährte Methoden für die Entwicklung eines Anbieters

Beachten Sie die folgenden Methoden, wenn Sie einen Outlook Social Connector 2013 (OSC) entwickeln:
  
- Aus Sicherheitsgründen sollten Anbieter, die mit Servern über das Internet kommunizieren, das HTTPS -Protokoll (Hypertext Transfer Protocol, HTTP) mit SSL (Secure Socket Layer) verwenden. Andernfalls besteht das Risiko, dass E-Mail-Adressen, Aktivitäten in sozialen Netzwerken und andere Benutzerdaten während der Übertragung abgefangen oder verfügbar gemacht werden.
    
- Wenn Sie einen OSC-Anbieter für ein soziales Netzwerk eines Drittanbieters entwickeln, muss ihr Anbieter die Nutzungsbedingungen des sozialen Netzwerks einhalten.
    
- Um die Größe des Anbieterdownloadpakets zu minimieren, erstellen Sie den Anbieter mithilfe eines systemeigenen Compilers wie C++ oder eines anderen Tools, das eine #A0 erstellen kann.
    
- Erstellen Sie in Ihrem Anbieter einen eindeutigen Benutzer-Agent, der an das soziale Netzwerk gesendet wird, um Anrufe des Anbieters an das soziale Netzwerk zu verfolgen.
    
- Die [ISocialProvider::GetCapabilities-Methode](isocialprovider-getcapabilities.md) sollte nicht auf das Aufrufen des sozialen Netzwerks über das Internet angewiesen sein, um die Funktionen des Anbieters zu nutzen. Benutzer können z. B. offline Outlook starten. Wenn das OSC **GetCapabilities** aufruft und keine Netzwerkverbindung besteht, gibt **der GetCapabilities-Aufruf** keinen gültigen **Funktionen-XML-Code** zurück. Die bewährte Methode besteht in der Speicherung von **Funktionen von** XML als Ressource in Ihrem Anbieter. 
    
- Ihr OSC-Anbieter kann eine große Anzahl von Anrufen an ein soziales Netzwerk generieren. In Abhängigkeit von den Nutzungsbedingungen für Ihr soziales Netzwerk sollten Sie die Zwischenspeicherung von Freunden in einem Outlook-Ordner in Betracht ziehen, um die Anzahl der Anrufe vom OSC an Ihren Anbieter und wiederum von Ihrem Anbieter an das soziale Netzwerk zu reduzieren.
    
- Office 2013 ist sowohl in 32-Bit- als auch in 64-Bit-Versionen verfügbar. Versionen von Office vor Office 2010 sind nur in einer 32-Bit-Version verfügbar. Die Standardinstallation von Office 2013 auf 64-Bit-Windows ist 32-Bit. Wenn Sie die 64-Bit-Version des Betriebssystems unterstützen möchten, die mit 64-Bit Office 2013 installiert ist, müssen Sie auch eine 64-Bit-Version Ihres Anbieters veröffentlichen. 
    
## <a name="see-also"></a>Siehe auch

- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)  
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)  
- [Bereitstellen eines Providers](deploying-a-provider.md)  
- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)

