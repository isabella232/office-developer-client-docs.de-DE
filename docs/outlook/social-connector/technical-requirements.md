---
title: Technische Anforderungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: In diesem Thema werden die unterstützten Programmiersprachen, COM-Sichtbarkeits-und Methodenrückgabe Typen und Details zur Erweiterbarkeits-DLL für Outlook Social Connector (OSC) beschrieben.
ms.openlocfilehash: 14dfcf52d714177775c5610b5da91d174f81a132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329155"
---
# <a name="technical-requirements"></a>Technische Anforderungen

In diesem Thema werden die unterstützten Programmiersprachen, COM-Sichtbarkeits-und Methodenrückgabe Typen und Details zur Erweiterbarkeits-DLL für Outlook Social Connector (OSC) beschrieben. 
  
## <a name="programming-language-and-com-requirements"></a>Programmiersprachen-und COM-Anforderungen

Sie können einen OSC-Anbieter erstellen, indem Sie verwaltete Sprachen wie Visual C# oder Visual Basic oder nicht verwaltete Sprachen wie Visual C++ verwenden. Sie können ein beliebiges Tool verwenden, mit dem eine COM-sichtbare DLL-Komponente erstellt werden kann, um einen OSC-Anbieter zu entwickeln. Die Entscheidung, eine verwaltete oder nicht verwaltete Sprache für die Entwicklung eines Anbieters zu verwenden, sollte die Downloadgröße und die Abhängigkeiten des Anbieter Installationspakets berücksichtigen.
  
Ein OSC-Anbieter muss gemäß der folgenden Definition COM-sichtbar sein:
  
- Nach der Installation muss ein OSC-Anbieter mithilfe von COM Self-Registration oder regsvr32 registriert werden.
    
- Die COM-Registrierung einer OSC-Anbieter-DLL registriert den Anbieter unter HKCU oder HKLM. 
    
- Die ProgID eines Anbieters ist unter `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`registriert.
    
- Ein OSC-Anbieter, der in einer verwalteten Sprache entwickelt wurde, ist COM-sichtbar.
    
- Ein OSC-Anbieter sollte der Windows-Registrierung Werte hinzufügen, die darauf hinweisen, dass die Anbieter-DLL sowohl ein STA-als auch ein Multithread-Apartment (MTA)-Threading-Modelle unterstützt. Weitere Informationen zu COM-Threadingmodellen finden Sie unter [Beschreibungen und Funktionsweise von OLE](https://support.microsoft.com/kb/150777)-threadIng-Modellen.
    
Methoden in der OSC-Anbieter Erweiterbarkeit müssen primitive Typen wie **String** oder **bool**zurückgeben. Bestimmte **Zeichenfolgen** Rückgabewerte müssen der Schema Definition für osc-Anbieter Erweiterbarkeit entsprechen. Nur XML wird als Rückgabewert unterstützt. 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a>Details zur OSC-Anbieter Erweiterbarkeits-DLL

Die Komponente, die OSC-Anbieter Erweiterbarkeit unterstützt, ist die OSC-Erweiterungs-DLL. Drittanbieter-Entwickler können OSC-Anbieter-DLLs mithilfe dieser Erweiterbarkeitsschnittstellen erstellen. In der folgenden Liste sind die Details der OSC-Anbieter Erweiterungs-DLL aufgeführt:
  
- Erweiterungs-DLL-Dateiname: socialprovider. dll
    
- Erweiterbarkeit der DLL-Datei: Microsoft Outlook-Erweiterbarkeit für soziale Netzwerke
    
- Erweiterungs-DLL-Hauptversion: 15,0
    
- Extensibiilty-DLL-Bibliotheksversion: 1,1
    
## <a name="miscellaneous-technical-information"></a>Sonstige technische Informationen

JSON (JavaScript Object Notation) wird im Erweiterbarkeitsmodell des OSC-Anbieters nicht unterstützt.
  
Es gibt keine Abhängigkeiten von einem XML-Parser. Der OSC-Anbieter kann einen in Office enthaltenen XML-Parser wie Microsoft XML Core Services (MSXML) verwenden, die in Microsoft .NET Framework integrierten XML-Analysefunktionen verwenden oder einen Drittanbieter-XML-Parser verwenden. 
  
## <a name="see-also"></a>Siehe auch

- [Bewährte Methoden für die Entwicklung eines Anbieters](best-practices-for-developing-a-provider.md)  
- [Schnelle Schritte für die Entwicklung eines Anbieters](quick-steps-for-learning-to-develop-a-provider.md)
- [Bereitstellen eines Providers](deploying-a-provider.md)  
- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)

