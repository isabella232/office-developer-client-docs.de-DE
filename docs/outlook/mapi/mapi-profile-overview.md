---
title: Übersicht über das MAPI-Profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d6c57be6-2397-4ab1-a912-028454dffc44
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e196800b717ce2528da4b9871bad7425f3a2c326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328164"
---
# <a name="mapi-profile-overview"></a>Übersicht über das MAPI-Profil

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Profil ist eine Sammlung von Informationen zu den Nachrichtendiensten und Dienstanbietern, die ein Benutzer einer Clientanwendung während einer bestimmten MAPI-Sitzung verfügbar sein möchte. Jeder Benutzer verfügt über mindestens ein Profil. Viele Benutzer behalten mehrere. Ein Benutzer kann beispielsweise ein Profil für die Arbeit mit einem serverbasierten Nachrichtenspeicherdienst und ein anderes Profil für die Arbeit mit einem Nachrichtenspeicherdienst auf dem lokalen Computer haben. Ein Benutzer möchte möglicherweise auf eine Gruppe von Messagingsystemen zugreifen, indem er die entsprechenden Transportdienste für einen Teil des Tages und einen anderen Satz für den Rest des Tages verwendet. Profile bieten eine flexible Möglichkeit, Kombinationen von Messagingsystemdiensten auszuwählen. 
  
Profile können Namen von bis zu 64 alphanumerischen Zeichen haben. Die Namen können Akzentzeichen, den Unterstrich und eingebettete Leerzeichen enthalten und dürfen keine vor- oder nachgestellten Leerzeichen enthalten. 
  
Profile sind hierarchisch organisiert und in Abschnitte unterteilt, mit einem Abschnitt für jeden Nachrichtendienst und einem Abschnitt für jeden Dienstanbieter in einem Dienst. Die zugehörigen Abschnitte sind verknüpft, wodurch die Navigation durch die Informationen erleichtert wird. Jeder Abschnitt enthält eine Reihe von Einträgen, die MAPI oder eine Clientanwendung für die Konfiguration verwendet.
  
Die Einträge in einem Profil variieren vom Nachrichtendienst zum Nachrichtendienst. Zu den gängigen Einträgen gehören die folgenden:
  
- Der Name der einzelnen Nachrichtendienste oder Dienstanbieter.
    
- Der Name der DLLs, die Dienstanbieter und Nachrichtendienste enthalten.
    
- Der Name der Einstiegspunktfunktion jedes Nachrichtendiensts.
    
- Eine Liste der Dienstanbieter, aus den einzelnen Nachrichtendiensten.
    
Profile können bei der Installation, beim Laden von MAPI oder einem Nachrichtendienst auf einen Computer oder zu einem späteren Zeitpunkt erstellt werden. MAPI bietet den Profil-Assistenten für die Profilverwaltung. 
  
Der Profil-Assistent ist eine Anwendung, die neue Profile mit minimalem Arbeitsvolumen erstellt. Der Assistent verwendet Standardwerte für Einstellungen, wo immer möglich, was benutzern Zeit und Aufwand spart. Benutzer geben Werte nur ein, wenn dies unbedingt erforderlich ist. Weitere Informationen finden Sie unter [Erstellen eines Profils mithilfe des Profil-Assistenten](creating-a-profile-by-using-the-profile-wizard.md). Sie können auch das Office-Anpassungstool verwenden, um ein neues Profil zu erstellen. Weitere Informationen finden Sie unter [Office-Anpassungstool](https://go.microsoft.com/fwlink/?LinkId=123000).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Features und -Architektur](mapi-features-and-architecture.md)

