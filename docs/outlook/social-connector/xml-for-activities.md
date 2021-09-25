---
title: XML für „activities“
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: acc4a555-a3bf-4a79-86dc-aba6477733b8
description: Dieses Thema enthält ein Beispielszenario, das die Outlook OSC-Anbietererweiterungs-API (Social Connector) aufruft, die ein OSC-Anbieter implementiert und vom OSC zum Abrufen von Aktivitätsinformationen durchführt. Informationen werden in XML-Zeichenfolgen ausgedrückt, die dem OSC-Anbieter-XML-Schema entsprechen.
ms.openlocfilehash: e3b82ca77ecb3e5fa93a86aac840a8a791380b46
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629046"
---
# <a name="xml-for-activities"></a>XML für „activities“

Dieses Thema enthält ein Beispielszenario, das die Outlook OSC-Anbietererweiterungs-API (Social Connector) aufruft, die ein OSC-Anbieter implementiert und vom OSC zum Abrufen von Aktivitätsinformationen durchführt. Informationen werden in XML-Zeichenfolgen ausgedrückt, die dem OSC-Anbieter-XML-Schema entsprechen.
  
Das OSC-Anbieter-XML-Schema ermöglicht es einem OSC-Anbieter, Aktivitäten zu definieren. Zu den Aktivitätsinformationen gehören das soziale Netzwerk, in dem die Aktivitätsfeedelemente stammen, Details zu jedem Aktivitätsfeedelement (z. B. Besitzer, Typ und Veröffentlichungsdatum der Aktivität) und die Vorlage zum Anzeigen der Aktivität. Um das Anzeigen von Aktivitäten im Personenbereich oder auf der Visitenkarte zu unterstützen, muss der OSC-Anbieter eines sozialen Netzwerks den richtigen XML-Code für Aktivitäten implementieren und zurückgeben. Ein Beispiel für aktivitätsfeed-XML finden Sie unter [Activity Feed XML Example](activity-feed-xml-example.md). Weitere Informationen zum Synchronisieren von Aktivitäten von Freunden finden Sie unter ["Synchronisieren von Freunden und Aktivitäten".](synchronizing-friends-and-activities.md) Eine vollständige Definition des OSC-Anbieter-XML-Schemas, einschließlich der erforderlichen oder optionalen Elemente, finden Sie unter [Outlook XML-Schema](outlook-social-connector-provider-xml-schema.md)des Connector für soziale Netzwerke. 
  
Im folgenden Szenario synchronisiert osc aktivitäten für eine im Personenbereich ausgewählte Person dynamisch und ruft Details zu dieser Person ab:
  
1. Ein OSC-Anbieter, der die On-Demand-Synchronisierung von Aktivitäten unterstützt, gibt an, dass für osc mithilfe der **elemente getActivities** und **dynamicActivitiesLookupEx.** Der OSC-Anbieter legt auch das **hashFunction-Element** fest. Alle drei Elemente sind untergeordnete Elemente von **Funktionen.** 
    
2. Der OSC-Anbieter implementiert die Methoden **ISocialProvider::GetCapabilities** und [ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md) 
    
3. Der OSC ruft **ISocialProvider::GetCapabilities** auf, um den Wert von **"getActivities"** und **"dynamicActivitiesLookupEx"** zu überprüfen, um zu überprüfen, ob der OSC-Anbieter die On-Demand-Synchronisierung von Aktivitäten unterstützt. Der OSC notiert auch den Wert des **hashFunction-Elements,** das vom OSC-Anbieter unterstützt wird. 
    
4. Der OSC aktualisiert den Personenbereich oder die Visitenkarte, damit der Benutzer die neuesten Aktivitäten der ausgewählten Person sehen kann. Der OSC verschlüsselt die SMTP-Adresse der Person mithilfe der im **hashFunction-Element** angegebenen Hashfunktion und bildet eine XML-Zeichenfolge, die der XML-Schemadefinition für das **hashedAddresses-Element** entspricht. 
    
5. Der OSC ruft **ISocialSession2::GetActivitiesEx** auf und stellt diese XML-Zeichenfolge der Hashadresse als  _hashedAddresses-Parameter_ bereit, um eine aktuelle Sammlung von Aktivitäten für diese Person im  _Aktivitätsparameter_ abzurufen. Die _Zeichenfolge_ des Aktivitätsparameters entspricht der XML-Schemadefinition des **activityFeed-Elements.** 
    
6. Basierend auf der XML-Schemadefinition für **activityFeed** analysiert osc die  _Aktivitätszeichenfolge_ weiter, um den Typ, das Veröffentlichungsdatum und andere Informationen zu den einzelnen Aktivitäten zu ermitteln und wie die Aktivität angezeigt wird. 
    
7. Um Details über die ausgewählte Person abzurufen, ruft der OSC [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)auf und stellt die gleiche XML-Zeichenfolge mit Hashadressen wie das Argument für den  _parameter personsAddresses_ bereit. Die Details zu der Person werden im Parameter  _"personsCollection"_ zurückgegeben. Diese Details können **FirstName**, **LastName** und **emailAddress** enthalten. Der _Parameter "personsCollection"_ entspricht der XML-Schemadefinition für das **Personenelement.** 
    
Weitere Informationen zum Angeben von XML für Aktivitäten finden Sie in den folgenden Themen dieses Abschnitts:
  
- [Übersicht über XML für ein Aktivitätsfeedelement](overview-of-xml-for-an-activity-feed-item.md)
    
- [activityDetails-Element](activitydetails-element.md)
    
- [activityTemplateContainer-Element](activitytemplatecontainer-element.md)
    
- [Vorlagenvariablen](template-variables.md)
    
- [Richtlinien für die ordnungsgemäße Anzeige von Aktivitäten](guidelines-for-properly-displaying-activities.md)
    
## <a name="see-also"></a>Siehe auch

- [Beispiel für Aktivitätsfeed-XML](activity-feed-xml-example.md)  
- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md) 
- [XML für Funktionen](xml-for-capabilities.md)  
- [XML für Freunde](xml-for-friends.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

