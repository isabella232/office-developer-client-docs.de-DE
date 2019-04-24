---
title: Übersicht über MAPI-Profile
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
# <a name="mapi-profile-overview"></a>Übersicht über MAPI-Profile

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bei einem Profil handelt es sich um eine Sammlung von Informationen zu den Nachrichtendiensten und Dienstanbietern, die ein Benutzer einer Clientanwendung während einer bestimmten MAPI-Sitzung verfügbar sein möchte. Jeder Benutzer verfügt über mindestens ein Profil; viele Benutzer halten mehrere. Ein Benutzer kann beispielsweise über ein Profil mit einem Server basierten Nachrichtenspeicher Dienst und einem anderen Profil verfügen, um mit einem Nachrichtenspeicher Dienst auf dem lokalen Computer zu arbeiten. Ein Benutzer möchte möglicherweise auf einen Satz von Messagingsystemen zugreifen, indem er die entsprechenden Transportdienste für einen Teil des Tages und einen anderen Satz für den Rest des Tages verwendet. Profile bieten eine flexible Möglichkeit, Kombinationen von Messagingsystem Diensten auszuwählen. 
  
Profile können bis zu 64 alphanumerische Zeichen enthalten. Die Namen können Akzentzeichen, den Unterstrich und eingebettete Leerzeichen enthalten und dürfen keine führenden oder nachstehenden Leerzeichen enthalten. 
  
Profile werden hierarchisch strukturiert und in Abschnitte unterteilt, mit einem Abschnitt für jeden Nachrichtendienst und einem Abschnitt für jeden Dienstanbieter in einem Dienst. Die zugehörigen Abschnitte sind verknüpft, sodass die Navigation durch die Informationen vereinfacht wird. Jeder Abschnitt enthält eine Reihe von Einträgen, die von MAPI oder einer Clientanwendung zur Konfiguration verwendet werden.
  
Die Einträge in einem Profil variieren vom Nachrichtendienst zum Nachrichtendienst. Zu den häufig verwendeten Einträgen gehört Folgendes:
  
- Der Name der einzelnen Nachrichtendienste oder Dienstanbieter.
    
- Der Name der DLLs, die Dienstanbieter und Nachrichtendienste enthalten.
    
- Der Name der Einstiegspunktfunktion der einzelnen Nachrichtendienste.
    
- Eine Liste der Dienstanbieter, aus denen sich die einzelnen Nachrichtendienste zusammensetzen.
    
Profile können zur Installationszeit erstellt werden, wenn MAPI oder ein Nachrichtendienst auf einen Computer oder zu einem späteren Zeitpunkt geladen wird. MAPI stellt den Profil-Assistenten für die Profilverwaltung bereit. 
  
Der Profil-Assistent ist eine Anwendung, die neue Profile mit einem minimalen Arbeitsaufwand erstellt. Der Assistent verwendet Standardwerte für Einstellungen, wo immer möglich, und spart Benutzern Zeit und Aufwand. Benutzer geben Werte nur bei Bedarf ein. Weitere Informationen finden Sie unter [Erstellen eines Profils mithilfe des Profil-Assistenten](creating-a-profile-by-using-the-profile-wizard.md). Sie können auch das Office-Anpassungs Tool verwenden, um ein neues Profil zu erstellen. Weitere Informationen finden Sie unter [Office-Anpassungstool](https://go.microsoft.com/fwlink/?LinkId=123000).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Features und -Architektur](mapi-features-and-architecture.md)

