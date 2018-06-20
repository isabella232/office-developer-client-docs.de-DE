---
title: MAPI-Architektur (Übersicht)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00d2993c-d66a-4a00-9fb2-98696d29a007
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: db8ca0945c429e7b277ec95b419386d1ce175169
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792943"
---
# <a name="mapi-architecture-overview"></a>MAPI-Architektur (Übersicht)
 
**Betrifft**: Outlook 
  
MAPI definiert eine modulare Architektur, wie in der folgenden Abbildung dargestellt.  
  
![Outlook 2010-Architektur] (media/amapi_43.gif "Outlook 2010-Architektur")
  
Die MAPI-Anwendung wird als Clientanwendung bezeichnet, da es sich um einen Client des MAPI-Subsystems darstellt. Messaging-basierte Anwendungen als ein zentraler Bestandteil von deren Verarbeitung messaging einsetzen und bieten umfangreiche-Funktionen, wie etwa den Austausch von Informationen über verschiedene Arten in verschiedenen Formaten und die Möglichkeit zum Speichern und organisieren die Informationen lokal. E-Mail, Planung und Arbeit Flow Anwendungen sind Beispiele für die messaging-basierte Anwendungen.
  
MAPI-Subsystems eine einheitliche Benutzeroberfläche und die Programmierschnittstellen besteht. Einheitliche Benutzeroberfläche ist eine Gruppe von Dialogfeldern, die Clientanwendungen ein einheitliches Aussehen und Benutzer bietet ein konsistentes arbeiten.
  
MAPI hat Programmierschnittstellen, die von MAPI-Subsystems, Client-Software-Entwicklern und Service Provider Entwickler verwendet werden. Die MAPI-Programmierschnittstelle ist die Haupt-Objekt-basierten Programmierschnittstelle. Die MAPI-Programmierschnittstelle ähnelt der OLE Component Object Model und wird von der MAPI-Subsystems und messaging-basierte Clientanwendungen, die in C oder C++ geschrieben. 
  
Als Client Softwareentwickler stellen Sie MAPI-Aufrufe direkt über die MAPI-Programmierschnittstelle. Sie können die messaging mit einer einzigen Benutzeroberfläche der MAPI-Client oder eine Kombination von Schnittstellen implementieren. In einer einzigen Anwendung kann Methoden oder Funktionen, die zu einer Schnittstelle gehören anrufen.
  
## <a name="see-also"></a>Siehe auch

-[MAPI-Features und die Architektur](mapi-features-and-architecture.md)

