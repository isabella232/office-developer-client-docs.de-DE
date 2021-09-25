---
title: XML für „capabilities“
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'Das Funktionselement im XML-Schema des (OSC)-Anbieters ermöglicht es einem OSC-Anbieter, seine Funktionalität anzugeben. Diese Funktionalität umfasst Folgendes:'
ms.openlocfilehash: 6b46567853a2f8a37ff5f9479c9eb8e4f4da7ccf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582981"
---
# <a name="xml-for-capabilities"></a>XML für „capabilities“

Das **Funktionselement** im XML-Schema des (OSC)-Anbieters ermöglicht es einem OSC-Anbieter, seine Funktionalität anzugeben. Diese Funktionalität umfasst Folgendes: 
  
- Gibt an, ob der Anbieter das Abrufen, Zwischenspeichern oder dynamische Nachschlagen von Freunden und Aktivitäten aus dem sozialen Netzwerk unterstützt.
    
- Anzeigen bestimmter Benutzeroberflächen für die Anmeldung durch osc.
    
- Gibt an, ob der OSC die formularbasierte Authentifizierung verwenden oder das soziale Netzwerk automatisch konfigurieren und sich beim Benutzer im sozialen Netzwerk anmelden soll.
    
Das XML-Schema für **Funktionen** ist wichtig, da es dem OSC die vom Anbieter unterstützte Funktionalität identifiziert. Ein OSC-Anbieter muss die [ISocialProvider::GetCapabilities-Methode](isocialprovider-getcapabilities.md) implementieren, die eine  _Ergebniszeichenfolge_ zurückgibt. Der OSC ruft **ISocialProvider::GetCapabilities** auf, um Informationen zu den Funktionen des OSC-Anbieters in der  _Ergebniszeichenfolge_ abzurufen, die der XML-Schemadefinition für das **Capabilities-Element** entspricht. Anhand dieser Informationen können nachfolgende Aufrufe von OSC an den OSC-Anbieter ordnungsgemäß ausgeführt werden. 
  
Um die Funktionen eines OSC-Anbieters als Ausgabeparameter der **ISocialProvider::GetCapabilities-Methode** anzugeben, müssen Sie dem OSC-Anbietererweiterungs-XML-Schema entsprechen. Die folgende Abbildung zeigt die XML-Struktur der **Funktionen.** 
  
**Abbildung 1. \<capabilities\> XML-Struktur**

![Funktionen für XML-Struktur](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
Ausführliche Beschreibungen der untergeordneten Elemente des **Capabilities-Elements** finden Sie unter [Capabilities XML-Elemente.](capabilities-xml-elements.md) Ein Beispiel für **funktions-XML** finden Sie unter [Capabilities XML Example](capabilities-xml-example.md). Eine vollständige Definition des OSC-Anbieter-XML-Schemas, einschließlich der erforderlichen oder optionalen Elemente, finden Sie unter [Outlook XML-Schema](outlook-social-connector-provider-xml-schema.md)des Connector für soziale Netzwerke.
  
## <a name="see-also"></a>Siehe auch

- [Xml-Beispiel für Funktionen](capabilities-xml-example.md)  
- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md)  
- [XML für Freunde](xml-for-friends.md)  
- [XML für Aktivitäten](xml-for-activities.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

