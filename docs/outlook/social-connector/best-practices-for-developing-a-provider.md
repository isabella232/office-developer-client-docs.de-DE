---
title: Bewährte Methoden für die Entwicklung eines Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: 'Sie sollten die folgenden Methoden einhalten, wenn Sie einen anbieter für Outlook Connector für soziale Netzwerke 2013 (OSC) entwickeln:'
ms.openlocfilehash: 97405b70b225e7e5c961e07f31bdd5eeb3247bb2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608963"
---
# <a name="best-practices-for-developing-a-provider"></a>Bewährte Methoden für die Entwicklung eines Anbieters

Sie sollten die folgenden Methoden einhalten, wenn Sie einen anbieter für Outlook Connector für soziale Netzwerke 2013 (OSC) entwickeln:
  
- Aus Sicherheitsgründen sollten Anbieter, die über das Internet mit Servern kommunizieren, das HTTPS-Protokoll (Hypertext Transfer Protocol, HTTP) mit SSL (Secure Socket Layer) verwenden. Andernfalls besteht das Risiko, dass E-Mail-Adressen, Aktivitäten in sozialen Netzwerken und andere Benutzerdaten während der Übertragung abgefangen oder offengelegt werden können.
    
- Wenn Sie einen OSC-Anbieter für ein soziales Netzwerk eines Drittanbieters entwickeln, muss Ihr Anbieter die Nutzungsbedingungen des sozialen Netzwerks einhalten.
    
- Um die Größe des Anbieterdownloadpakets zu minimieren, erstellen Sie den Anbieter mithilfe eines systemeigenen Compilers wie C++ oder eines anderen Tools, das eine COM-Komponente erstellen kann.
    
- Erstellen Sie in Ihrem Anbieter einen eindeutigen Benutzer-Agent, der an das soziale Netzwerk gesendet wird, um Anrufe des Anbieters an das soziale Netzwerk nachzuverfolgen.
    
- Die [ISocialProvider::GetCapabilities-Methode](isocialprovider-getcapabilities.md) sollte sich nicht darauf verlassen, das soziale Netzwerk über das Internet aufzurufen, um die Funktionen des Anbieters abzurufen. Beispielsweise können Benutzer Outlook offline starten. Wenn der OSC **GetCapabilities** aufruft und keine Netzwerkverbindung besteht, gibt der **GetCapabilities-Aufruf** keine gültige **FUNKTIONS-XML** zurück. Die bewährte Methode besteht darin, **xml-Funktionen** als Ressource in Ihrem Anbieter zu speichern. 
    
- Ihr OSC-Anbieter kann ein erhebliches Volumen von Anrufen an ein soziales Netzwerk generieren. Je nach den Nutzungsbedingungen für Ihr soziales Netzwerk sollten Sie in Betracht ziehen, Freunde in einem Outlook Ordner zwischenzuspeichern, um die Anzahl der Anrufe vom OSC an Ihren Anbieter und wiederum von Ihrem Anbieter an das soziale Netzwerk zu reduzieren.
    
- Office 2013 ist sowohl in 32-Bit- als auch in 64-Bit-Versionen verfügbar. Versionen von Office vor Office 2010 sind nur in einer 32-Bit-Version verfügbar. Die Standardinstallation von Office 2013 auf 64-Bit-Windows ist 32-Bit. Wenn Sie die 64-Bit-Version des OSC unterstützen möchten, die mit 64-Bit-Office 2013 installiert ist, müssen Sie auch eine 64-Bit-Version Ihres Anbieters freigeben. 
    
## <a name="see-also"></a>Siehe auch

- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)  
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)  
- [Bereitstellen eines Providers](deploying-a-provider.md)  
- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)

