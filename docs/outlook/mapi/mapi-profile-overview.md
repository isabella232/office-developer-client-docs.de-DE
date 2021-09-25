---
title: Übersicht über MAPI-Profile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d6c57be6-2397-4ab1-a912-028454dffc44
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2353b8e5da09f57607e10d65efb032a0b6f530c0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610223"
---
# <a name="mapi-profile-overview"></a>Übersicht über MAPI-Profile

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Profil ist eine Sammlung von Informationen zu den Nachrichtendiensten und Dienstanbietern, die ein Benutzer einer Clientanwendung während einer bestimmten MAPI-Sitzung verfügbar sein möchte. Jeder Benutzer verfügt über mindestens ein Profil; viele Benutzer behalten mehrere. Beispielsweise kann ein Benutzer über ein Profil verfügen, um mit einem serverbasierten Nachrichtenspeicherdienst zu arbeiten, und ein anderes Profil, um mit einem Nachrichtenspeicherdienst auf dem lokalen Computer zu arbeiten. Ein Benutzer möchte möglicherweise auf eine Gruppe von Messagingsystemen zugreifen, indem er die entsprechenden Transportdienste für einen Teil des Tages und einen anderen Satz für den Rest des Tages verwendet. Profile bieten eine flexible Möglichkeit, Kombinationen von Messaging-Systemdiensten auszuwählen. 
  
Profile können Namen von bis zu 64 alphanumerischen Zeichen enthalten. Die Namen können Akzentzeichen, den Unterstrich und eingebettete Leerzeichen enthalten und dürfen keine führenden oder nachstehenden Leerzeichen enthalten. 
  
Profile sind hierarchisch organisiert und in Abschnitte unterteilt, mit einem Abschnitt für jeden Nachrichtendienst und einem Abschnitt für jeden Dienstanbieter in einem Dienst. Die zugehörigen Abschnitte sind verknüpft, wodurch die Navigation durch die Informationen erleichtert wird. Jeder Abschnitt enthält eine Reihe von Einträgen, die mapi oder eine Clientanwendung für die Konfiguration verwendet.
  
Die in einem Profil enthaltenen Einträge variieren von Nachrichtendienst zu Nachrichtendienst. Einige der allgemeinen Einträge umfassen Folgendes:
  
- Der Name der einzelnen Nachrichtendienste oder Dienstanbieter.
    
- Der Name der DLLs, die Dienstanbieter und Nachrichtendienste enthalten.
    
- Der Name der Einstiegspunktfunktion jedes Nachrichtendiensts.
    
- Eine Liste der Dienstanbieter, aus denen die einzelnen Nachrichtendienste bestehen.
    
Profile können bei der Installation, beim Laden der MAPI oder eines Nachrichtendiensts auf einen Computer oder zu einem späteren Zeitpunkt erstellt werden. MAPI stellt den Profil-Assistenten für die Profilverwaltung bereit. 
  
Der Profil-Assistent ist eine Anwendung, die neue Profile mit einem Minimum an Arbeit erstellt. Der Assistent verwendet nach Möglichkeit Standardwerte für Einstellungen, wodurch Den Benutzern Zeit und Aufwand gespart wird. Benutzer geben Werte nur ein, wenn dies unbedingt erforderlich ist. Weitere Informationen finden Sie unter [Erstellen eines Profils mithilfe des Profil-Assistenten.](creating-a-profile-by-using-the-profile-wizard.md) Sie können auch das Office Anpassungstool verwenden, um ein neues Profil zu erstellen. Weitere Informationen finden Sie unter [Office-Anpassungstool](https://go.microsoft.com/fwlink/?LinkId=123000).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Features und -Architektur](mapi-features-and-architecture.md)

