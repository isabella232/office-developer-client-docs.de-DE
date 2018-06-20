---
title: Übersicht über die MAPI-Profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d6c57be6-2397-4ab1-a912-028454dffc44
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 573709c4374786bb1bd3d763c8ba91de59f7fb1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793028"
---
# <a name="mapi-profile-overview"></a>Übersicht über die MAPI-Profil

  
  
**Betrifft**: Outlook 
  
Ein Profil ist eine Auflistung von Informationen zu den Message-Dienste und Dienstanbieter, die ein Benutzer von einer Clientanwendung möchte während einer bestimmten MAPI-Sitzung verfügbar sein soll. Jeder Benutzer verfügt über mindestens ein Profil; viele Benutzer behalten mehrere. Ein Benutzer möglicherweise beispielsweise ein Profil entwickelt eine serverbasierte Message Store Service und ein anderes Profil ein Informationsspeicher-Dienst auf dem lokalen Computer entwickelt. Ein Benutzer kann auf eine Gruppe von messaging-Systeme mithilfe der entsprechenden Transportdienste für einen Teil der Tag und eine andere für den Rest des Tages zugreifen möchten. Profile bieten eine flexible Möglichkeit zum Kombinationen von messaging-Systemdienste auswählen. 
  
Profile können Namen bis zu 64 alphanumerische Zeichen Länge aufweisen. Die Namen können Akzent Zeichen, Unterstriche und Leerzeichen enthalten und darf keine Leerzeichen beginnen oder enden. 
  
Profile sind hierarchisch organisiert und Abschnitte mit einem Abschnitt für jeden Nachrichtendienst und einen Abschnitt für jeden Anbieter in einem Dienst unterteilt. Verwandte Abschnitte sind verknüpft, die Informationen Navigieren zu erleichtern. Jeder Abschnitt enthält eine Reihe von Einträgen, die MAPI- oder einer anderen Clientanwendung für die Konfiguration verwendet.
  
Die Einträge in einem Profil enthalten unterscheiden sich von Messagingdiensts zu Messagingdiensts. Einige allgemeine Einträge umfassen Folgendes:
  
- Der Name jedes Messagingdiensts oder Dienstanbieter.
    
- Der Name der DLLs, die e-Mail-Dienste und enthalten-Dienstanbieter.
    
- Der Name der einzelnen Messagingdiensts Eintrag Point-Funktion.
    
- Eine Liste der Dienstanbieter, die jeder Messagingdiensts bilden.
    
Profile können bei der Installation, wenn MAPI oder einer Nachrichtendienst auf einem Computer geladen wird, oder zu einem späteren Zeitpunkt erstellt werden. MAPI bietet der Profil-Assistent für die Benutzerprofildienst-Verwaltung. 
  
Der Profil-Assistent ist eine Anwendung, die mit einem minimum an der Arbeit neue Profile erstellt. Der Assistent verwendet Standardwerte für Einstellungen möglichst Benutzer Zeit und Mühe speichern. Nur bei Bedarf Werte geben die Benutzer ein. Weitere Informationen finden Sie unter [Erstellen eines Profils mithilfe der Profil-Assistent](creating-a-profile-by-using-the-profile-wizard.md). Sie können auch Office-Anpassungstool verwenden, um ein neues Profil zu erstellen. Weitere Informationen finden Sie unter [Office Customization Tool](http://go.microsoft.com/fwlink/?LinkId=123000).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Features und die Architektur](mapi-features-and-architecture.md)

