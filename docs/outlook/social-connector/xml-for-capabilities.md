---
title: XML für „capabilities“
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'Das Capabilities-Element im (OSC)-Anbieter-XML-Schema ermöglicht es einem OSC-Anbieter, seine Funktionalität anzugeben. Diese Funktionalität umfasst Folgendes:'
ms.openlocfilehash: ff6abbd4d99eb542a11e3d64a2015fc0585fca79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435005"
---
# <a name="xml-for-capabilities"></a>XML für „capabilities“

Das **Capabilities-Element** im (OSC)-Anbieter-XML-Schema ermöglicht es einem OSC-Anbieter, seine Funktionalität anzugeben. Diese Funktionalität umfasst Folgendes: 
  
- Ob der Anbieter das Abrufen, Zwischenspeichern oder dynamische Suchen von Freunden und Aktivitäten aus dem sozialen Netzwerk unterstützt.
    
- Wie das OSC bestimmte Anmeldebenutzerschnittstellen anzeigen soll.
    
- Gibt an, ob das OSC die formularbasierte Authentifizierung verwenden oder das soziale Netzwerk automatisch konfigurieren und sich beim Benutzer im sozialen Netzwerk anmeldet.
    
Das XML-Schema für **Funktionen** ist von entscheidender Bedeutung, da es für das OSC die vom Anbieter unterstützte Funktionalität identifiziert. Ein OSC-Anbieter muss die [ISocialProvider::GetCapabilities-Methode](isocialprovider-getcapabilities.md) implementieren, die eine _Ergebniszeichenfolge zurückgibt._ Das OSC ruft **ISocialProvider::GetCapabilities** auf, um Informationen zu  den Funktionen des OSC-Anbieters in der Ergebniszeichenfolge zu erhalten, die der XML-Schemadefinition für das **Capabilities-Element** entspricht. Mit diesen Informationen können nachfolgende Aufrufe des Betriebssystems an den OSC-Anbieter ordnungsgemäß ausgeführt werden. 
  
Um Funktionen eines OSC-Anbieters als Ausgabeparameter der **ISocialProvider::GetCapabilities-Methode** anzugeben, müssen Sie das XML-Schema für die Erweiterbarkeit des OSC-Anbieters erfüllen. Die folgende Abbildung zeigt die **XML-Struktur der Funktionen.** 
  
**Abbildung 1. \<funktionen \> XML-Struktur**

![Funktionen für XML-Struktur](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
Ausführliche Beschreibungen untergeordneter Elemente des **Capabilities-Elements** finden Sie unter [Capabilities XML Elements](capabilities-xml-elements.md). Ein Beispiel für **xml-Funktionen** finden Sie unter [Capabilities XML Example](capabilities-xml-example.md). Eine vollständige Definition des XML-Schemas des OSC-Anbieters, einschließlich der erforderlichen oder optionalen Elemente, finden Sie unter [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).
  
## <a name="see-also"></a>Siehe auch

- [Capabilities XML(Beispiel)](capabilities-xml-example.md)  
- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md)  
- [XML für Freunde](xml-for-friends.md)  
- [XML für Aktivitäten](xml-for-activities.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

