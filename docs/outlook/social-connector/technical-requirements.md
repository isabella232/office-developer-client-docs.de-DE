---
title: Technische Anforderungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: In diesem Thema werden die unterstützten Programmiersprachen, Typ Anforderungen und Details zu den Outlook Social Connector (OSC)-Erweiterbarkeit des Providers DLL COM-Sichtbarkeit und -Methode zurück.
ms.openlocfilehash: 94b57e20957f3d8d779c4d3324ecbb8ccd37f60a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796083"
---
# <a name="technical-requirements"></a>Technische Anforderungen

In diesem Thema werden die unterstützten Programmiersprachen, Typ Anforderungen und Details zu den Outlook Social Connector (OSC)-Erweiterbarkeit des Providers DLL COM-Sichtbarkeit und -Methode zurück. 
  
## <a name="programming-language-and-com-requirements"></a>Programmiersprachen und COM-Anforderungen

Sie können einen OSC-Anbieter mit verwalteten Sprachen wie Visual c# oder Visual Basic oder nicht verwaltete Sprachen wie Visual C++ erstellen. Sie können eine beliebige Tool verwenden, die eine COM-sichtbare DLL-Komponente Informationen zum Entwickeln von eines OSC-Anbieters erstellen können. Die Entscheidung für eine verwaltete oder nicht verwaltete Sprache zum Entwickeln eines Providers sollte Konto die Download-Größe und Abhängigkeiten des Installationspakets Anbieter berücksichtigen.
  
Ein OSC-Anbieter muss COM-sichtbar sein, wie folgt definiert:
  
- Nach der Installation muss ein OSC-Anbieters mithilfe von COM-Self-Registrierung oder regsvr32 registriert werden.
    
- COM-Registrierung eines OSC-Anbieters DLL registriert den Anbieter unter HKCU oder HKLM. 
    
- ProgID des Providers registriert ist, klicken Sie unter `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.
    
- Ein in einer verwalteten Sprache entwickelt OSC-Anbieter ist COM-sichtbar.
    
- Ein OSC-Anbieter sollten Werte hinzufügen, der Windows-Registrierung, die angeben, dass der Provider-DLL des Apartmentthreading Single-Threading (Station) und multithreaded Apartmentthreading (MTA) Modelle unterstützt. Weitere Informationen zu COM Threadmodelle finden Sie unter [Beschreibung und Funktionsweise von OLE Threading-Modelle](http://support.microsoft.com/kb/150777).
    
Methoden bei der Erweiterbarkeit der OSC-Anbieter müssen Grundtypen wie **Zeichenfolge** oder **Bool**zurückgeben. Bestimmte **Zeichenfolge** zurück, dass die Werte der Schemadefinition für die Erweiterbarkeit des OSC-Providers einhalten müssen. Nur XML-Zeichenfolge wird als Rückgabewert unterstützt. 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a>Details der die OSC-anbietererweiterung DLL

Die Komponente, die Erweiterbarkeit des OSC-Providers unterstützt ist die OSC-anbietererweiterung DLL. Drittanbieter-Entwickler können mit dieser Erweiterungsschnittstellen OSC-Anbieter-DLLs erstellen. Die folgende Liste enthält die Details der OSC-anbietererweiterung DLL:
  
- Erweiterbarkeit der DLL-Dateiname: socialprovider.dll
    
- Erweiterbarkeit der DLL-Anzeigename: Microsoft Outlook für soziale Netzwerke Erweiterbarkeit des Providers
    
- Erweiterbarkeit der DLL-Hauptversion: 15.0
    
- Der Typbibliothek Extensibiilty-DLL-Version: 1.1
    
## <a name="miscellaneous-technical-information"></a>Sonstige technische Informationen

JavaScript Object Notation (JSON) wird im Modell Erweiterbarkeit OSC-Anbieter nicht unterstützt.
  
Es gibt keine Abhängigkeiten auf einen XML-Parser. OSC-Anbieter kann verwenden einen XML-Parser, der mit Office, wie beispielsweise Microsoft XML Core Services (MSXML) enthalten ist, verwenden Sie die XML-Parser Funktionen in Microsoft .NET Framework integriert, oder einen Drittanbieter-XML-Parser. 
  
## <a name="see-also"></a>Siehe auch

- [Bewährte Methoden für das Entwickeln eines Providers](best-practices-for-developing-a-provider.md)  
- [QuickSteps für Informationen zum Entwickeln eines Providers](quick-steps-for-learning-to-develop-a-provider.md)
- [Bereitstellen eines Providers](deploying-a-provider.md)  
- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)

