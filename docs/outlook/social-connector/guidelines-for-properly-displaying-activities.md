---
title: Richtlinien für die ordnungsgemäße Anzeige von Aktivitäten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Outlook Social Connector (OSC)-Anbieter lassen sich die GetActivities und DynamicActivitiesLookupEx Elemente, die die OSC-Aktivitätselemente im Arbeitsspeicher gespeichert haben.
ms.openlocfilehash: f8cb5850c8920f09f784343db18372bb75ca17a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795954"
---
# <a name="guidelines-for-properly-displaying-activities"></a>Richtlinien für die ordnungsgemäße Anzeige von Aktivitäten

Outlook Social Connector (OSC)-Anbieter können die **GetActivities** und **DynamicActivitiesLookupEx** Elemente haben die OSC Aktivitätselemente im Arbeitsspeicher gespeichert. In diesem Thema werden die OSC-anbietererweiterung, die aus dem sozialen Netzwerk-APIs, die die OSC zum Abrufen oder Aktualisieren von Aktivitäten und Aktivität Besitzer Details, aufruft Wenn der OSC-Anbieter synchronisieren Aktivität unterstützt feeds. Das Thema enthält auch ein paar untergeordnete Elemente des **ActivityFeed** -Elements, dass der OSC-Anbieter für das osc bilden zum Anzeigen von Aktivitäten ordnungsgemäß in der Office-Visitenkarte oder Outlook Personenbereich festgelegt werden soll. 
  
- Die OSC Ruft die [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) -Methode zum Abrufen und Speichern von Aktivitäten im Newsfeed Ordner des angemeldeten Benutzers. Der OSC-Anbieter muss **GetActivitiesEx** um _Aktivitäten_ XML-Zeichenfolge zurückzugeben, die mit dem OSC-Anbieter XML-Schemadefinition des **ActivityFeed** -Elements entspricht implementieren. 
    
- Der OSC-Anbieter muss das **OwnerID** -Element ein untergeordnetes Element des Elements **ActivityDetails ist** festlegen. **OwnerID** ist eine opake Zeichenfolge, die den Besitzer der Aktivität im sozialen Netzwerk identifiziert. 
    
- Der OSC-Anbieter sollte die **NameHint** und **EmailAddress** -Elemente im Knoten **PublisherVariable** des **TemplateVariables** -Elements festgelegt. 
    
   Beachten Sie, dass pro das OSC-Anbieter-XML-Schema, das **NameHint** -Element ein optionales Element ist. Die OSC wird verwendet, um den Anzeigenamen des Benutzers in der Visitenkarte oder Personenbereich ausgewählt übereinstimmen. In ähnlicher Weise ist das **EmailAddress** -Element ein optionales Element im XML-Schema. Die OSC wird verwendet, um die SMTP-Adresse des Benutzers in der Visitenkarte oder Personenbereich ausgewählt übereinstimmen. 
    
   Wenn nur das **OwnerID** -Element angegeben ist, aber eine oder beide der **NameHint** und **EmailAddress** nicht angegeben werden, ruft das osc bilden die [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) -Methode, und klicken Sie dann die [ISocialPerson::GetDetails](isocialperson-getdetails.md) Methode, um weitere Informationen über die Person, die vom **OwnerID**abzurufen. Wenn die OSC **ISocialPerson::GetDetails**aufruft, muss der Anbieter **Person** XML zurück, der die **FullName** und **EmailAddress** -Elemente angibt. 
    
## <a name="see-also"></a>Siehe auch

- [XML-Code für Aktivitäten](xml-for-activities.md)  
- [XML-Code für Freunde](xml-for-friends.md)  
- [XML-Code für Funktionen](xml-for-capabilities.md)

