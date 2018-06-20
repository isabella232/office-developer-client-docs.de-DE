---
title: XML-Code für Aktivitäten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: acc4a555-a3bf-4a79-86dc-aba6477733b8
description: Dieses Thema enthält ein Beispielszenario, das den Outlook Social Connector (OSC)-Anbieter zeigt Erweiterbarkeits-API-Aufrufe, die ein OSC-Anbieter implementiert und die OSC zum Abrufen von Aktivitätsinformationen macht. Informationen wird in XML-Zeichenfolgen ausgedrückt, die das OSC-Anbieter-XML-Schema entsprechen.
ms.openlocfilehash: 44f74d9e72eec3ff6da7f9967315fc9d75191584
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796098"
---
# <a name="xml-for-activities"></a>XML-Code für Aktivitäten

Dieses Thema enthält ein Beispielszenario, das den Outlook Social Connector (OSC)-Anbieter zeigt Erweiterbarkeits-API-Aufrufe, die ein OSC-Anbieter implementiert und die OSC zum Abrufen von Aktivitätsinformationen macht. Informationen wird in XML-Zeichenfolgen ausgedrückt, die das OSC-Anbieter-XML-Schema entsprechen.
  
OSC-Anbieter-XML-Schema ermöglicht einen OSC-Anbieter Aktivitäten zu definieren. Aktivitätsinformationen kann das soziale Netzwerk, in dem die Aktivitäts--Elemente stammt Feed, Details der einzelnen Elemente Aktivitätsfeed enthalten (z. B. Besitzer, eingeben und Veröffentlichungsdatum der Aktivität), und die Vorlage aus, um die Aktivität anzuzeigen. Zur Unterstützung der mit Aktivitäten auf dem Bereich Personen oder Visitenkarte muss ein social Network OSC-Anbieter implementieren und die richtigen Aktivitäten XML zurückgegeben. Ein Beispiel der Aktivität XML-feed, finden Sie unter [Aktivität Feed XML-Beispiel](activity-feed-xml-example.md). Weitere Informationen zum Synchronisieren von Freunden Aktivitäten finden Sie unter [Synchronisieren Freunde und Aktivitäten](synchronizing-friends-and-activities.md). Eine vollständige Definition des OSC-Anbieter XML-Schema, welche Elemente sind, erforderlich oder optional, einschließlich finden Sie unter [Outlook Social Connector Provider XML-Schema](outlook-social-connector-provider-xml-schema.md). 
  
Im folgenden Szenario wird die OSC dynamisch synchronisiert Aktivitäten für eine Person im Bereich Personen ausgewählt und ruft Informationen zu dieser Person:
  
1. Ein OSC-Anbieter, der bedarfsgesteuerten Synchronisierung von Aktivitäten unterstützt angibt, der die OSC, mithilfe der **GetActivities** und **DynamicActivitiesLookupEx** Elemente. Der OSC-Anbieter wird auch das **HashFunction** -Element. Alle drei Elemente sind untergeordnete Elemente des **Funktionen**. 
    
2. Der OSC-Anbieter implementiert die Methoden **ISocialProvider::GetCapabilities** und [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) . 
    
3. Die OSC-Aufrufe **ISocialProvider::GetCapabilities** an den Wert der **GetActivities** und **DynamicActivitiesLookupEx** überprüfen, um sicherzustellen, dass den OSC-Anbieter unterstützt bedarfsgesteuerten Synchronisierung von Aktivitäten. Die OSC Notizen auch den Wert des **HashFunction** -Elements durch den OSC-Anbieter unterstützt. 
    
4. Die OSC wird der Bereich Personen oder Visitenkarte, um die neuesten Aktivitäten der ausgewählten Person finden Sie unter Benutzer können aktualisiert. Die OSC verschlüsselt die SMTP-Adresse der Person mithilfe der Hashfunktion im Element **HashFunction** bilden eine XML-Zeichenfolge, die die XML-Schemadefinition für das **HashedAddresses** -Element entspricht. 
    
5. Die OSC ruft **ISocialSession2::GetActivitiesEx**, bietet diese XML-Zeichenfolge der Hash-Adresse als _HashedAddresses_ -Parameter, um aktuelle Zusammenstellung von Aktivitäten für diese Person im Parameter _Aktivitäten_ zu erhalten. Die Zeichenfolge für den _Aktivitäten_ Parameter erfüllt die XML-Schemadefinition des **ActivityFeed** -Elements. 
    
6. Basierend auf den XML-Schemadefinition für **ActivityFeed**, analysiert der OSC weiter die _Aktivitäten_ Zeichenfolge suchen, die-Typ, veröffentlichen, Datum, und andere Informationen über jede Aktivität und wie Sie die Aktivität anzeigen. 
    
7. Um Informationen zu der ausgewählten Person erhalten möchten, ruft der OSC [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md), die gleiche XML-Zeichenfolge als Argument für den Parameter _PersonsAddresses_ Hash-Adressen bereitstellt. Die Details über die Person werden im Parameter _PersonsCollection_ zurückgegeben. Diese Einzelheiten können **FirstName**, **LastName**und **EmailAddress**hinzufügen. Der Parameter _PersonsCollection_ entspricht der XML-Schemadefinition für das Element **Person** . 
    
Sie finden weitere Informationen zum Angeben von XML für Aktivitäten in den folgenden Themen dieses Abschnitts:
  
- [Übersicht über XML-Code für eine Aktivität Element-Feed](overview-of-xml-for-an-activity-feed-item.md)
    
- [ActivityDetails Element](activitydetails-element.md)
    
- [ActivityTemplateContainer Element](activitytemplatecontainer-element.md)
    
- [Vorlagenvariablen](template-variables.md)
    
- [Richtlinien für das Aktivitäten ordnungsgemäß anzeigen](guidelines-for-properly-displaying-activities.md)
    
## <a name="see-also"></a>Siehe auch

- [Beispiel für eine Aktivität Feed XML](activity-feed-xml-example.md)  
- [Synchronisieren von Freunde und Aktivitäten](synchronizing-friends-and-activities.md) 
- [XML-Code für Funktionen](xml-for-capabilities.md)  
- [XML-Code für Freunde](xml-for-friends.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

