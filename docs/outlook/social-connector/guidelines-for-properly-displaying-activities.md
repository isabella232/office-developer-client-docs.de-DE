---
title: Richtlinien für die ordnungsgemäße Anzeige von Aktivitäten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Outlook Anbieter für sozialen Connector (Social Connector, OSC) können die Elemente getActivities und dynamicActivitiesLookupEx so festlegen, dass die OSC Aktivitätselemente im Speicher speichern.
ms.openlocfilehash: b2fcaa125ac8bf7924726f4f09ff507769c3a3f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422915"
---
# <a name="guidelines-for-properly-displaying-activities"></a>Richtlinien für die ordnungsgemäße Anzeige von Aktivitäten

Outlook Anbieter für sozialen Connector (Social Connector, OSC) können die **Elemente getActivities** und **dynamicActivitiesLookupEx** so festlegen, dass die OSC Aktivitätselemente im Speicher speichern. In diesem Thema werden die OSC-Anbieter-Erweiterbarkeits-APIs beschrieben, die das OSC aufruft, um Details zu Aktivitäten und Aktivitätsbesitzern zu erhalten oder zu aktualisieren, wenn der OSC-Anbieter die Synchronisierung von Aktivitätsfeeds aus dem sozialen Netzwerk unterstützt. Im Thema werden auch einige untergeordnete Elemente des **activityFeed-Elements** aufgeführt, das der OSC-Anbieter festlegen sollte, damit die Aktivitäten im Bereich Office Visitenkarte oder Outlook angezeigt werden. 
  
- Das OSC ruft die [ISocialSession2::GetActivitiesEx-Methode](isocialsession2-getactivitiesex.md) auf, um Aktivitäten im Ordner Newsfeed für den angemeldeten Benutzer zu erhalten und zu speichern. Der OSC-Anbieter muss **GetActivitiesEx** implementieren, um eine Aktivitäts-XML-Zeichenfolge zurücksenden zu können, die der XML-Schemadefinition des OSC-Anbieters des **activityFeed-Elements** entspricht.  
    
- Der #A0 muss das **ownerID-Element** festlegen, das ein untergeordnetes Element des **activityDetails-Elements** ist. **ownerID** ist eine undurchsichtige Zeichenfolge, die den Besitzer der Aktivität im sozialen Netzwerk identifiziert. 
    
- Der OSC-Anbieter sollte die **Elemente nameHint** und **emailAddress** im **Knoten publisherVariable** des **templateVariables-Elements** festlegen. 
    
   Beachten Sie, dass das **nameHint-Element** nach dem XML-Schema des OSC-Anbieters ein optionales Element ist. Das OSC verwendet es, um dem Anzeigenamen des im Bereich Visitenkarte oder Personen ausgewählten Benutzers zu entsprechen. Entsprechend ist das **emailAddress-Element** ein optionales Element im XML-Schema. Das OSC verwendet es, um die SMTP-Adresse des Benutzers zu entsprechen, der im Bereich Visitenkarte oder Personen ausgewählt ist. 
    
   Wenn nur das **ownerID-Element** angegeben ist, aber eine oder beide **nameHint-** und **emailAddress-Elemente** nicht angegeben sind, ruft das OSC die [ISocialSession2::GetPeopleDetails-Methode](isocialsession2-getpeopledetails.md) und dann die [ISocialPerson::GetDetails-Methode](isocialperson-getdetails.md) auf, um weitere Informationen über die durch die ownerID identifizierte Person **zu erhalten.** Wenn das OSC **ISocialPerson::GetDetails aufruft,** muss der Anbieter eine Person-XML  zurückgeben, die die Elemente **fullName** und **emailAddress** angibt. 
    
## <a name="see-also"></a>Siehe auch

- [XML für Aktivitäten](xml-for-activities.md)  
- [XML für Freunde](xml-for-friends.md)  
- [XML für Funktionen](xml-for-capabilities.md)

