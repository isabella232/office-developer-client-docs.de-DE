---
title: Richtlinien für die ordnungsgemäße Anzeige von Aktivitäten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Die Outlook Social Connector-Anbieter (OSC) können die getactivitys-und dynamicActivitiesLookupEx-Elemente so festlegen, dass der OSC Aktivitäts Elemente im Arbeitsspeicher speichert.
ms.openlocfilehash: b2fcaa125ac8bf7924726f4f09ff507769c3a3f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286181"
---
# <a name="guidelines-for-properly-displaying-activities"></a>Richtlinien für die ordnungsgemäße Anzeige von Aktivitäten

Die Outlook Social Connector-Anbieter (OSC) können **** die getactivitys-und **dynamicActivitiesLookupEx** -Elemente so festlegen, dass der osc Aktivitäts Elemente im Arbeitsspeicher speichert. In diesem Thema werden die APIs für OSC-Anbieter Erweiterbarkeit beschrieben, die von OSC zum Abrufen oder Aktualisieren von Aktivitäten und Aktivitäten Besitzer Details aufgerufen werden, wenn der OSC-Anbieter die Synchronisierung von Aktivitätsfeeds aus dem sozialen Netzwerk unterstützt. Das Thema listet auch einige untergeordnete Elemente des **activityFeed** -Elements auf, die der osc-Anbieter für den osc festlegen muss, damit die Aktivitäten in der Office-Visitenkarte oder im Outlook-Personen Bereich angezeigt werden. 
  
- OSC Ruft die [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) -Methode auf, um Aktivitäten im Newsfeed-Ordner für den angemeldeten Benutzer abzurufen und zu speichern. Der OSC-Anbieter muss **GetActivitiesEx** implementieren, um eine XML- _Aktivitäts_ Zeichenfolge zurückzugeben, die der XML-Schema Definition des osc-Anbieters des **activityFeed** -Elements entspricht. 
    
- Der OSC-Anbieter muss das **Owner** -Element festlegen, das ein untergeordnetes Element des **activityDetails** -Elements ist. **Besitzer** -Kennung ist eine undurchsichtige Zeichenfolge, die den Besitzer der Aktivität im sozialen Netzwerk identifiziert. 
    
- Der OSC-Anbieter sollte die **nameHint** -und **Email** -Elemente im **publisherVariable** -Knoten des **templateVariables** -Elements festlegen. 
    
   Beachten Sie, dass das **NAMEHINT** -Element pro osc-Anbieter-XML-Schema ein optionales Element ist. Der OSC verwendet ihn, um den Anzeigenamen des in der Kontaktkarte oder im Personen Bereich ausgewählten Benutzers abzugleichen. Entsprechend ist das **Email** -Element ein optionales Element im XML-Schema. Der OSC verwendet ihn, um die SMTP-Adresse des Benutzers zu ermitteln, der im Bereich VisitenKarte oder Personen ausgewählt ist. 
    
   Wenn nur das **Owner** -Element angegeben ist, aber eine oder beide von **nameHint** und **** e/a nicht angegeben werden, ruft osc die [ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md) -Methode und dann die [ISocialPerson:: getDetails](isocialperson-getdetails.md) -Methode, um weitere Informationen zu der Person abzurufen, die von der **Besitzer**-Nr identifiziert wird. Wenn der OSC **ISocialPerson:: getDetails**aufruft, muss der Anbieter einen **Personen** -XML-Code zurückgeben, der die **FullName** -und **Email** -Elemente angibt. 
    
## <a name="see-also"></a>Siehe auch

- [XML für Aktivitäten](xml-for-activities.md)  
- [XML für Freunde](xml-for-friends.md)  
- [XML für Funktionen](xml-for-capabilities.md)

