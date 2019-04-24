---
title: XML für „activities“
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: acc4a555-a3bf-4a79-86dc-aba6477733b8
description: Dieses Thema enthält ein Beispielszenario, in dem die von einem OSC-Anbieter implementierten APIs für die Erweiterbarkeits-Erweiterbarkeit (Social Connector) und OSC zum Abrufen von Aktivitätsinformationen angezeigt werden. Informationen werden in XML-Zeichenfolgen ausgedrückt, die dem OSC-Anbieter-XML-Schema entsprechen.
ms.openlocfilehash: a4f1c6ce1f33b59811f6a6fecb737cd1f737946b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329120"
---
# <a name="xml-for-activities"></a>XML für „activities“

Dieses Thema enthält ein Beispielszenario, in dem die von einem OSC-Anbieter implementierten APIs für die Erweiterbarkeits-Erweiterbarkeit (Social Connector) und OSC zum Abrufen von Aktivitätsinformationen angezeigt werden. Informationen werden in XML-Zeichenfolgen ausgedrückt, die dem OSC-Anbieter-XML-Schema entsprechen.
  
Das XML-Schema des OSC-Anbieters ermöglicht es einem OSC-Anbieter, Aktivitäten zu definieren. Aktivitätsinformationen können das soziale Netzwerk einbeziehen, in dem die Aktivitätsfeed-Elemente stammen, Details zu den einzelnen Aktivitätsfeed-Elementen (wie Besitzer, Typ und Veröffentlichungsdatum der Aktivität) sowie die Vorlage zum Anzeigen der Aktivität. Zur Unterstützung der Anzeige von Aktivitäten im Personen Bereich oder der VisitenKarte muss der OSC-Anbieter eines sozialen Netzwerks die richtigen Aktivitäten XML implementieren und zurückgeben. Ein Beispiel für Aktivitäts-Feed-XML finden Sie unter [Activity Feed XML example](activity-feed-xml-example.md). Weitere Informationen zum Synchronisieren von Aktivitäten von Freunden finden Sie unter [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md). Eine vollständige Definition des XML-Schemas des OSC-Anbieters, einschließlich der erforderlichen oder optionalen Elemente, finden Sie unter [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md). 
  
Im folgenden Szenario synchronisiert OSC die Aktivitäten für eine im Personen Bereich ausgewählte Person dynamisch und ruft Details zu dieser Person ab:
  
1. Ein OSC-Anbieter, der die bedarfsgesteuerte Synchronisierung von Aktivitäten unterstützt, weist darauf hin, **** dass der osc mithilfe der Elemente GetActivities und **dynamicActivitiesLookupEx** . Der OSC-Anbieter legt auch das **hashFunction** -Element fest. Alle drei Elemente sind untergeordnete Elemente der **Funktionen**. 
    
2. Der OSC-Anbieter implementiert die Methoden **ISocialProvider:: getCapabilities** und [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) . 
    
3. OSC ruft **ISocialProvider:: getCapabilities** auf, um den Wert von **GetActivities** und **dynamicActivitiesLookupEx** zu überprüfen, um zu überprüfen, ob der osc-Anbieter die bedarfsgesteuerte Synchronisierung von Aktivitäten unterstützt. Der OSC stellt auch den Wert des vom OSC-Anbieter unterstützten **hashFunction** -Elements fest. 
    
4. Der OSC aktualisiert den Personen Bereich oder die VisitenKarte, damit der Benutzer die neuesten Aktivitäten der ausgewählten Person anzeigen kann. OSC verschlüsselt die SMTP-Adresse der Person mithilfe der im **hashFunction** -Element angegebenen Hashfunktion und bildet eine XML-Zeichenfolge, die der XML-Schema Definition für das **hashedAddresses** -Element entspricht. 
    
5. OSC ruft **ISocialSession2:: GetActivitiesEx**auf, wobei diese XML-Zeichenfolge der Hash Adresse als _hashedAddresses_ -Parameter bereitgestellt wird, um eine aktuelle Auflistung von Aktivitäten für diese Person im _Activities_ -Parameter abzurufen. Die _Aktivitäts_ Parameterzeichenfolge entspricht der XML-Schema Definition des **activityFeed** -Elements. 
    
6. Basierend auf der XML-Schema Definition für **activityFeed**analysiert der osc die Aktivitäts Zeichenfolge __ weiter, um den Typ, das Veröffentlichungsdatum und weitere Informationen zu den einzelnen Aktivitäten zu ermitteln und die Aktivität anzuzeigen. 
    
7. Um Details zur ausgewählten Person abzurufen, ruft OSC [ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md)auf und stellt die gleiche XML-Zeichenfolge von Hash-Adressen als Argument für den _personsAddresses_ -Parameter bereit. Die Details zur Person werden im Parameter personencollection __ zurückgegeben. Diese Details können **FirstName**, **LastName**und **Email**-e/a sein. Der __ Parameter personencollection entspricht der XML-Schema Definition für das **Person** -Element. 
    
Weitere Informationen zum Angeben von XML für Aktivitäten finden Sie in den folgenden Themen dieses Abschnitts:
  
- [Übersicht über XML für ein Aktivitäts Feed-Element](overview-of-xml-for-an-activity-feed-item.md)
    
- [activityDetails-Element](activitydetails-element.md)
    
- [activityTemplateContainer-Element](activitytemplatecontainer-element.md)
    
- [Vorlagenvariablen](template-variables.md)
    
- [Richtlinien für die OrdnungsGemäße Anzeige von Aktivitäten](guidelines-for-properly-displaying-activities.md)
    
## <a name="see-also"></a>Siehe auch

- [XML-Beispiel für Aktivitätsfeeds](activity-feed-xml-example.md)  
- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md) 
- [XML für Funktionen](xml-for-capabilities.md)  
- [XML für Freunde](xml-for-friends.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

