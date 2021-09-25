---
title: Richtlinien für die ordnungsgemäße Anzeige von Aktivitäten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Outlook OSC-Anbieter (Social Connector) können die Elemente "getActivities" und "dynamicActivitiesLookupEx" so festlegen, dass die OSC-Aktivitätselemente im Arbeitsspeicher gespeichert werden.
ms.openlocfilehash: 77763ca1ec1f95ec0220c1cf59f3bdd61aa53bff
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560396"
---
# <a name="guidelines-for-properly-displaying-activities"></a>Richtlinien für die ordnungsgemäße Anzeige von Aktivitäten

Outlook OSC-Anbieter (Social Connector) können die **Elemente "getActivities"** und **"dynamicActivitiesLookupEx"** so festlegen, dass die OSC-Aktivitätselemente im Arbeitsspeicher gespeichert werden. In diesem Thema werden die OSC-Anbietererweiterungs-APIs beschrieben, die der OSC aufruft, um Aktivitäten und Aktivitätsbesitzerdetails abzurufen oder zu aktualisieren, wenn der OSC-Anbieter die Synchronisierung von Aktivitätsfeeds aus dem sozialen Netzwerk unterstützt. In diesem Thema werden auch einige untergeordnete Elemente des **ActivityFeed-Elements** aufgeführt, die der OSC-Anbieter festlegen sollte, damit aktivitäten ordnungsgemäß im Office Visitenkarte oder im Outlook Personenbereich angezeigt werden. 
  
- Der OSC ruft die [ISocialSession2::GetActivitiesEx-Methode](isocialsession2-getactivitiesex.md) auf, um Aktivitäten im Newsfeedordner für den angemeldeten Benutzer abzurufen und zu speichern. Der OSC-Anbieter muss **GetActivitiesEx** implementieren, um eine _XML-Zeichenfolge_ für Aktivitäten zurückzugeben, die der XML-Schemadefinition des OSC-Anbieters des **activityFeed-Elements entspricht.** 
    
- Der OSC-Anbieter muss das **ownerID-Element** festlegen, bei dem es sich um ein untergeordnetes Element des **activityDetails-Elements** handelt. **ownerID** ist eine undurchsichtige Zeichenfolge, die den Besitzer der Aktivität im sozialen Netzwerk identifiziert. 
    
- Der OSC-Anbieter sollte die **Elemente nameHint** und **emailAddress** im **publisherVariable-Knoten** des **templateVariables-Elements** festlegen. 
    
   Beachten Sie, dass gemäß dem OSC-Anbieter-XML-Schema das **nameHint-Element** ein optionales Element ist. Der OSC verwendet sie, um dem Anzeigenamen des Benutzers zu entsprechen, der in der Visitenkarte oder im Personenbereich ausgewählt wurde. Ebenso ist das **emailAddress-Element** ein optionales Element im XML-Schema. Das OSC verwendet es, um die SMTP-Adresse des Benutzers zuzuordnen, der im Visitenkarten- oder Personenbereich ausgewählt wurde. 
    
   Wenn nur das **ownerID-Element** angegeben ist, aber eines oder beides von **nameHint** und **emailAddress** nicht angegeben sind, ruft osc die [ISocialSession2::GetPeopleDetails-Methode](isocialsession2-getpeopledetails.md) und dann die [ISocialPerson::GetDetails-Methode](isocialperson-getdetails.md) auf, um weitere Informationen über die von der **ownerID** identifizierte Person abzurufen. Wenn der OSC **ISocialPerson::GetDetails** aufruft, muss der Anbieter **Personen-XML** zurückgeben, die die **Elemente "fullName"** und **"emailAddress"** angibt. 
    
## <a name="see-also"></a>Siehe auch

- [XML für Aktivitäten](xml-for-activities.md)  
- [XML für Freunde](xml-for-friends.md)  
- [XML für Funktionen](xml-for-capabilities.md)

