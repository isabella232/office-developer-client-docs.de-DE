---
title: XML für „capabilities“
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'Das Capabilities-Element im XML-Schema des (OSC)-Anbieters ermöglicht es einem OSC-Anbieter, seine Funktionalität anzugeben. Diese Funktionalität umfasst Folgendes:'
ms.openlocfilehash: ff6abbd4d99eb542a11e3d64a2015fc0585fca79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356445"
---
# <a name="xml-for-capabilities"></a>XML für „capabilities“

Das **Capabilities** -Element im XML-Schema des (OSC)-Anbieters ermöglicht es einem osc-Anbieter, seine Funktionalität anzugeben. Diese Funktionalität umfasst Folgendes: 
  
- Ob der Anbieter das Abrufen, Zwischenspeichern oder dynamische Suchen von Freunden und Aktivitäten aus dem sozialen Netzwerk unterstützt.
    
- Wie der OSC bestimmte Anmeldebenutzer Oberflächen anzeigen soll.
    
- Gibt an, ob OSC die formularbasierte Authentifizierung verwenden oder das soziale Netzwerk automatisch konfigurieren und den Benutzer im sozialen Netzwerk anmelden soll.
    
Das XML-Schema für **Funktionen** ist von entscheidender Bedeutung, da es die vom Anbieter unterstützten Funktionen für osc identifiziert. Ein OSC-Anbieter muss die [ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md) -Methode implementieren, die eine _Ergebnis_ Zeichenfolge zurückgibt. OSC ruft **ISocialProvider:: getCapabilities** auf, um Informationen zu den Funktionen des osc-Anbieters in der _Ergebnis_ Zeichenfolge abzurufen, die der XML-Schema Definition für das **Capabilities** -Element entspricht. Anhand dieser Informationen können nachfolgende Aufrufe vom OSC an den OSC-Anbieter ordnungsgemäß ausgeführt werden. 
  
Um die Funktionen eines OSC-Anbieters als Ausgabeparameter der **ISocialProvider:: getCapabilities** -Methode anzugeben, müssen Sie dem XML-Schema osc-Anbieter Erweiterbarkeit entsprechen. Die folgende Abbildung zeigt die XML-Struktur der **Funktionen** . 
  
**Abbildung 1. \<XML\> -Struktur der Funktionen**

![Funktionen für XML-Struktur](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
Ausführliche Beschreibungen der untergeordneten Elemente des **Capabilities** -Elements finden Sie unter [Capabilities XML Elements](capabilities-xml-elements.md). Ein Beispiel für XML- **Funktionen** finden Sie unter [Capabilities XML example](capabilities-xml-example.md). Eine vollständige Definition des XML-Schemas des OSC-Anbieters, einschließlich der erforderlichen oder optionalen Elemente, finden Sie unter [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).
  
## <a name="see-also"></a>Siehe auch

- [XML-Beispiel für Funktionen](capabilities-xml-example.md)  
- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md)  
- [XML für Freunde](xml-for-friends.md)  
- [XML für Aktivitäten](xml-for-activities.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

