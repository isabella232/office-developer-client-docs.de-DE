---
title: XML für „activities“
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: acc4a555-a3bf-4a79-86dc-aba6477733b8
description: Dieses Thema enthält ein Beispielszenario, das die Outlook Social Connector (OSC)-Anbieter-Erweiterungs-API-Aufrufe zeigt, die von einem OSC-Anbieter implementiert werden, und das OSC zum Abrufen von Aktivitäteninformationen. Informationen werden in XML-Zeichenfolgen ausgedrückt, die dem XML-Schema des OSC-Anbieters entsprechen.
ms.openlocfilehash: a4f1c6ce1f33b59811f6a6fecb737cd1f737946b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409629"
---
# <a name="xml-for-activities"></a>XML für „activities“

Dieses Thema enthält ein Beispielszenario, das die Outlook Social Connector (OSC)-Anbieter-Erweiterungs-API-Aufrufe zeigt, die von einem OSC-Anbieter implementiert werden, und das OSC zum Abrufen von Aktivitäteninformationen. Informationen werden in XML-Zeichenfolgen ausgedrückt, die dem XML-Schema des OSC-Anbieters entsprechen.
  
Das XML-Schema des OSC-Anbieters ermöglicht es einem OSC-Anbieter, Aktivitäten zu definieren. Aktivitätsinformationen können das soziale Netzwerk, in dem die Aktivitätsfeedelemente stammen, Details der einzelnen Aktivitätsfeedelemente (z. B. Besitzer, Typ und Veröffentlichungsdatum der Aktivität) und die Vorlage zum Anzeigen der Aktivität enthalten. Um das Anzeigen von Aktivitäten im Personenbereich oder auf der Visitenkarte zu unterstützen, muss der OsC-Anbieter eines sozialen Netzwerks den richtigen XML-Code für Aktivitäten implementieren und zurückgeben. Ein Beispiel für aktivitätsfeed-XML finden Sie unter [Activity Feed XML Example](activity-feed-xml-example.md). Weitere Informationen zum Synchronisieren der Aktivitäten von Freunden finden Sie [unter Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md). Eine vollständige Definition des XML-Schemas des OSC-Anbieters, einschließlich der erforderlichen oder optionalen Elemente, finden Sie unter [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md). 
  
Im folgenden Szenario synchronisiert das OSC die Aktivitäten für eine im Personenbereich ausgewählte Person dynamisch und ruft Details zu dieser Person ab:
  
1. Ein OSC-Anbieter, der die On-Demand-Synchronisierung von Aktivitäten unterstützt, gibt dies mithilfe der **Elemente getActivities** und **dynamicActivitiesLookupEx** an. Der #A0 legt auch das **hashFunction-Element** fest. Alle drei Elemente sind untergeordnete Elemente von **Funktionen.** 
    
2. Der OSC-Anbieter implementiert die **ISocialProvider::GetCapabilities-** und [ISocialSession2::GetActivitiesEx-Methoden.](isocialsession2-getactivitiesex.md) 
    
3. Das OSC ruft **ISocialProvider::GetCapabilities** auf, um den Wert von **getActivities** und **dynamicActivitiesLookupEx** zu überprüfen, um zu überprüfen, ob der OSC-Anbieter die On-Demand-Synchronisierung von Aktivitäten unterstützt. Das OSC notiert auch den Wert des **hashFunction-Elements,** das vom #A0 unterstützt wird. 
    
4. Das OSC aktualisiert den Personenbereich oder die Visitenkarte, damit der Benutzer die neuesten Aktivitäten der ausgewählten Person sehen kann. Das OSC verschlüsselt die #A0 der Person mithilfe der im **hashFunction-Element** angegebenen Hashfunktion und bildet eine XML-Zeichenfolge, die der #A1 für das **HashedAddresses-Element** entspricht. 
    
5. Das OSC ruft **ISocialSession2::GetActivitiesEx** auf und stellt diese #A0 der Hashadresse als  _HashedAddresses-Parameter_ zur Verfügung, um eine aktuelle Auflistung von Aktivitäten für diese Person im Parameter  _activities_ zu erhalten. Die _Zeichenfolge des Activities-Parameters_ entspricht der XML-Schemadefinition des **activityFeed-Elements.** 
    
6. Basierend auf der XML-Schemadefinition für **activityFeed** analysiert  das OSC die Aktivitätszeichenfolge weiter, um den Typ, das Veröffentlichungsdatum und weitere Informationen zu den einzelnen Aktivitäten zu finden und wie die Aktivität angezeigt wird. 
    
7. Um Details zur ausgewählten Person zu erhalten, ruft das OSC [ISocialSession2::GetPeopleDetails auf](isocialsession2-getpeopledetails.md)und stellt dieselbe #A0 mit Hashadressen wie das Argument für den  _parameter personsAddresses_ zur Verfügung. Die Details zur Person werden im  _Parameter personsCollection_ zurückgegeben. Diese Details können **firstName,** **lastName** und **emailAddress enthalten.** Der _parameter personsCollection_ entspricht der XML-Schemadefinition für das **Person-Element.** 
    
Weitere Informationen zum Angeben von XML für Aktivitäten finden Sie in den folgenden Themen dieses Abschnitts:
  
- [Übersicht über XML für ein Aktivitätsfeedelement](overview-of-xml-for-an-activity-feed-item.md)
    
- [activityDetails-Element](activitydetails-element.md)
    
- [activityTemplateContainer-Element](activitytemplatecontainer-element.md)
    
- [Vorlagenvariablen](template-variables.md)
    
- [Richtlinien für die ordnungsgemäßen Anzeige von Aktivitäten](guidelines-for-properly-displaying-activities.md)
    
## <a name="see-also"></a>Siehe auch

- [Beispiel für Aktivitätsfeed-XML](activity-feed-xml-example.md)  
- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md) 
- [XML für Funktionen](xml-for-capabilities.md)  
- [XML für Freunde](xml-for-friends.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

