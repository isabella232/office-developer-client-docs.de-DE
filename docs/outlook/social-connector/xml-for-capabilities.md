---
title: XML-Code für Funktionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'Das Capabilities-Element im XML-Schema (OSC)-Anbieter ermöglicht einen OSC-Anbieter an seine Funktionalität. Eine solche Funktionalität umfasst Folgendes:'
ms.openlocfilehash: 8192c4d559ae656cfc3b12cd8f50f7d4acd5ed5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796084"
---
# <a name="xml-for-capabilities"></a>XML-Code für Funktionen

Das **Capabilities** -Element im XML-Schema (OSC)-Anbieter ermöglicht einen OSC-Anbieter an seine Funktionalität. Eine solche Funktionalität umfasst Folgendes: 
  
- Gibt an, ob der Anbieter abrufen, Zwischenspeichern oder dynamisch Nachschlagen Freunde und Aktivitäten aus dem sozialen Netzwerk unterstützt.
    
- Wie die OSC-Benutzeroberflächen für bestimmte Anmeldung angezeigt werden soll.
    
- Gibt an, ob die OSC formularbasierte Authentifizierung verwenden oder automatisch die für soziale Netzwerke und die Protokolle auf den Benutzer im sozialen Netzwerk konfigurieren.
    
XML-Schema für **Funktionen** ist wichtig, da er den vom Anbieter unterstützten Funktionen an die OSC angegeben. Ein OSC-Anbieter muss die [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) -Methode implementieren, die Zeichenfolge ein _Ergebnis_ zurückgibt. Die OSC ruft **ISocialProvider::GetCapabilities** zum Abrufen von Informationen zu den Funktionen des OSC-Anbieters in die _resultierende_ Zeichenfolge, die die XML-Schemadefinition für das **Capabilities** -Element entspricht. Diese Informationen kann für nachfolgende Anrufe über den OSC, OSC-Anbieter ordnungsgemäß funktioniert. 
  
Um Funktionen für einen OSC-Anbieter als Output-Parameter der Methode **ISocialProvider::GetCapabilities** angeben, müssen Sie das OSC-Anbieter Erweiterbarkeit XML-Schema entsprechen. Die folgende Abbildung zeigt die XML-Struktur von **Funktionen** . 
  
**Abbildung 1. \<Funktionen\> XML-Struktur**

![Funktionen für XML-Struktur](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
Eine ausführliche Beschreibung der untergeordneten Elemente des **Capabilities** -Element finden Sie unter [Funktionen XML-Elemente](capabilities-xml-elements.md). Ein Beispiel für XML- **Funktionen** finden Sie unter [Funktionen XML-Beispiel](capabilities-xml-example.md). Eine vollständige Definition des OSC-Anbieter XML-Schema, welche Elemente sind, erforderlich oder optional, einschließlich finden Sie unter [Outlook Social Connector Provider XML-Schema](outlook-social-connector-provider-xml-schema.md).
  
## <a name="see-also"></a>Siehe auch

- [Funktionen XML-Beispiel](capabilities-xml-example.md)  
- [Synchronisieren von Freunde und Aktivitäten](synchronizing-friends-and-activities.md)  
- [XML-Code für Freunde](xml-for-friends.md)  
- [XML-Code für Aktivitäten](xml-for-activities.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

