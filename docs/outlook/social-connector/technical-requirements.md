---
title: Technische Anforderungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: In diesem Thema werden die unterstützten Programmiersprachen, die Anforderungen für die COM-Sichtbarkeit und die Rückgabetypanforderungen der Methode sowie Details der Outlook Social Connector (OSC)-Anbieter-Erweiterbarkeits-DLL beschrieben.
ms.openlocfilehash: 14dfcf52d714177775c5610b5da91d174f81a132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329155"
---
# <a name="technical-requirements"></a>Technische Anforderungen

In diesem Thema werden die unterstützten Programmiersprachen, die Anforderungen für die COM-Sichtbarkeit und die Rückgabetypanforderungen der Methode sowie Details der Outlook Social Connector (OSC)-Anbieter-Erweiterbarkeits-DLL beschrieben. 
  
## <a name="programming-language-and-com-requirements"></a>Programmiersprachen- und COM-Anforderungen

Sie können einen #A0 mithilfe verwalteter Sprachen wie Visual C# oder Visual Basic oder nicht verwalteten Sprachen wie Visual C++ erstellen. Sie können jedes Tool verwenden, das eine COM-sichtbare DLL-Komponente erstellen kann, um einen OSC-Anbieter zu entwickeln. Die Entscheidung, eine verwaltete oder nicht verwaltete Sprache zum Entwickeln eines Anbieters zu verwenden, sollte die Downloadgröße und Abhängigkeiten des Anbieterinstallationspakets berücksichtigen.
  
Ein OSC-Anbieter muss com-visible sein, wie durch folgendes definiert:
  
- Nach der Installation muss ein OSC-Anbieter mithilfe der COM-Selbstregistrierung oder regsvr32 registriert werden.
    
- Die COM-Registrierung einer OSC-Anbieter-DLL registriert den Anbieter unter HKCU oder HKLM. 
    
- Die ProgID eines Anbieters ist unter  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` registriert.
    
- Ein in einer verwalteten Sprache entwickelter OSC-Anbieter ist COM-visible.
    
- Ein OSC-Anbieter sollte der Windows-Registrierung Werte hinzufügen, die angeben, dass die Anbieter-DLL sowohl Single-Threaded Apartment (STA) als auch Multithreaded Apartment (MTA)-Threadingmodelle unterstützt. Weitere Informationen zu COM-Threadingmodellen finden Sie unter [Descriptions and Workings of OLE Threading Models](https://support.microsoft.com/kb/150777).
    
Methoden in der Erweiterbarkeit des OSC-Anbieters müssen primitive Typen wie **zeichenfolge** oder **bool zurückgeben.** Bestimmte  Zeichenfolgenrücklaufwerte müssen der Schemadefinition für die Erweiterbarkeit des OSC-Anbieters entsprechen. Nur XML wird als Rückgabewert unterstützt. 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a>Details zur ERWEITERUNGS-DLL des OSC-Anbieters

Die Komponente, die die Erweiterbarkeit des OSC-Anbieters unterstützt, ist die ERWEITERUNGS-DLL des OSC-Anbieters. Drittanbieterentwickler können MITHILFE dieser Erweiterbarkeitsschnittstellen DLLs des OSC-Anbieters erstellen. In der folgenden Liste sind die Details der ERWEITERUNGs-DLL des OSC-Anbieters aufgeführt:
  
- Erweiterungs-DLL-Dateiname: socialprovider.dll
    
- Erweiterungs-DLL-Anzeigename: Microsoft Outlook Erweiterbarkeit für soziale Anbieter
    
- Erweiterungs-DLL-Hauptversion: 15.0
    
- Extensibiilty DLL TypeLib Version: 1.1
    
## <a name="miscellaneous-technical-information"></a>Verschiedene technische Informationen

JavaScript Object Notation (JSON) wird im Erweiterbarkeitsmodell des OSC-Anbieters nicht unterstützt.
  
Es gibt keine Abhängigkeiten von einem XML-Parser. Der OSC-Anbieter kann einen xml-Parser verwenden, der in Office enthalten ist, z. B. Microsoft XML Core Services (MSXML), die in Microsoft .NET Framework integrierten XML-Analysefunktionen oder einen DRITTANBIETER-XML-Parser verwenden. 
  
## <a name="see-also"></a>Siehe auch

- [Bewährte Methoden für die Entwicklung eines Anbieters](best-practices-for-developing-a-provider.md)  
- [Schnelle Schritte zum Entwickeln eines Anbieters](quick-steps-for-learning-to-develop-a-provider.md)
- [Bereitstellen eines Providers](deploying-a-provider.md)  
- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)

