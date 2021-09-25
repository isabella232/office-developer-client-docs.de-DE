---
title: Technische Anforderungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: In diesem Thema werden die unterstützten Programmiersprachen, COM-Sichtbarkeit und Methodenrückgabetypanforderungen sowie Details zur OSC-Anbietererweiterungs-DLL (Outlook Connector für soziale Netzwerke) beschrieben.
ms.openlocfilehash: 5d5ca78c7ff1e328257b7e645731e76a2e6e5633
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604060"
---
# <a name="technical-requirements"></a>Technische Anforderungen

In diesem Thema werden die unterstützten Programmiersprachen, COM-Sichtbarkeit und Methodenrückgabetypanforderungen sowie Details zur OSC-Anbietererweiterungs-DLL (Outlook Connector für soziale Netzwerke) beschrieben. 
  
## <a name="programming-language-and-com-requirements"></a>Programmiersprache und COM-Anforderungen

Sie können einen OSC-Anbieter erstellen, indem Sie verwaltete Sprachen wie Visual C# oder Visual Basic oder nicht verwaltete Sprachen wie Visual C++ verwenden. Sie können ein beliebiges Tool verwenden, das eine COM-sichtbare DLL-Komponente erstellen kann, um einen OSC-Anbieter zu entwickeln. Bei der Entscheidung, eine verwaltete oder nicht verwaltete Sprache zum Entwickeln eines Anbieters zu verwenden, sollten die Downloadgröße und Abhängigkeiten des Anbieterinstallationspakets berücksichtigt werden.
  
Ein OSC-Anbieter muss COM-sichtbar sein, wie durch Folgendes definiert:
  
- Nach der Installation muss ein OSC-Anbieter mithilfe der COM-Selbstregistrierung oder mithilfe von regsvr32 registriert werden.
    
- Die COM-Registrierung einer OSC-Anbieter-DLL registriert den Anbieter unter HKCU oder HKLM. 
    
- Die ProgID eines Anbieters wird unter  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` registriert.
    
- Ein OSC-Anbieter, der in einer verwalteten Sprache entwickelt wurde, ist COM-sichtbar.
    
- Ein OSC-Anbieter sollte der Windows Registrierung Werte hinzufügen, die angeben, dass die Anbieter-DLL sowohl Singlethread-Apartment (STA) als auch Multithread-Apartment-Threadingmodelle (MTA) unterstützt. Weitere Informationen zu COM-Threadingmodellen finden Sie unter [Descriptions and Workings of OLE Threading Models](https://support.microsoft.com/kb/150777).
    
Methoden in OSC-Anbietererweiterung müssen Grundtypen wie **Zeichenfolge** oder **Bool** zurückgeben. Bestimmte  Zeichenfolgenrückgabewerte müssen der Schemadefinition für die OSC-Anbietererweiterung entsprechen. Nur XML wird als Rückgabewert unterstützt. 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a>Details zur OSC-Anbietererweiterungs-DLL

Die Komponente, die die OSC-Anbietererweiterung unterstützt, ist die OSC-Anbietererweiterungs-DLL. Drittanbieterentwickler können OSC-Anbieter-DLLs mithilfe dieser Erweiterungsschnittstellen erstellen. Die folgende Liste enthält die Details der OSC-Anbietererweiterungs-DLL:
  
- Erweiterungs-DLL-Dateiname: socialprovider.dll
    
- Anzeigename der Erweiterbarkeits-DLL: Microsoft Outlook Erweiterbarkeit des Anbieters für soziale Netzwerke
    
- Erweiterungs-DLL-Hauptversion: 15.0
    
- Erweiterbare DLL TypeLib-Version: 1.1
    
## <a name="miscellaneous-technical-information"></a>Sonstige technische Informationen

JavaScript Object Notation (JSON) wird im OSC-Anbietererweiterungsmodell nicht unterstützt.
  
Es gibt keine Abhängigkeiten von einem XML-Parser. Der OSC-Anbieter kann einen XML-Parser verwenden, der in Office enthalten ist, z. B. Microsoft XML Core Services (MSXML), die in microsoft .NET Framework integrierten XML-Analysefunktionen oder einen XML-Parser eines Drittanbieters verwenden. 
  
## <a name="see-also"></a>Siehe auch

- [Bewährte Methoden für die Entwicklung eines Anbieters](best-practices-for-developing-a-provider.md)  
- [Schnelle Schritte für Learning zum Entwickeln eines Anbieters](quick-steps-for-learning-to-develop-a-provider.md)
- [Bereitstellen eines Providers](deploying-a-provider.md)  
- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)

