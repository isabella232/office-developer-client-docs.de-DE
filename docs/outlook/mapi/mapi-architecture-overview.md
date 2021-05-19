---
title: Übersicht über die MAPI-Architektur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00d2993c-d66a-4a00-9fb2-98696d29a007
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 98a723528a714918ad7e0f10534efb0d38ef139a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410077"
---
# <a name="mapi-architecture-overview"></a>Übersicht über die MAPI-Architektur
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI definiert eine modulare Architektur, wie in der folgenden Abbildung dargestellt.  
  
![Outlook 2010-Architektur](media/amapi_43.gif "Outlook 2010-Architektur")
  
Die MAPI-Anwendung wird als Clientanwendung bezeichnet, da sie ein Client des MAPI-Subsystems ist. Messaging-basierte Anwendungen verwenden Messaging als zentralen Teil ihrer Verarbeitung und bieten umfangreiche Messagingfeatures, z. B. den Austausch von Informationen verschiedener Typen in verschiedenen Formaten und die Möglichkeit, die Informationen lokal zu speichern und zu organisieren. E-Mail-, Planungs- und Arbeitsflussanwendungen sind Beispiele für messagingbasierte Anwendungen.
  
Das MAPI-Subsystem besteht aus einer gemeinsamen Benutzeroberfläche und den Programmierschnittstellen. Bei der allgemeinen Benutzeroberfläche handelt es sich um eine Reihe von Dialogfelder, die Clientanwendungen ein einheitliches Aussehen und Benutzern eine konsistente Arbeit ermöglichen.
  
MAPI verfügt über Programmierschnittstellen, die vom MAPI-Subsystem, von Clientsoftwareentwicklern und von Dienstanbieterentwicklern verwendet werden. Die MAPI-Programmierschnittstelle ist die wichtigste objektbasierte Programmierschnittstelle. Die MAPI-Programmierschnittstelle ähnelt dem OLE-Komponentenobjektmodell und wird vom #A0 und messagingbasierten Clientanwendungen verwendet, die in C oder C++ geschrieben wurden. 
  
Als Clientsoftwareentwickler nehmen Sie MAPI-Aufrufe direkt über die MAPI-Programmierschnittstelle vor. Sie können Messaging mit einer einzelnen MAPI-Clientschnittstelle oder einer Kombination von Schnittstellen implementieren. Eine einzelne Anwendung kann Methoden oder Funktionen aufrufen, die zu einer der Schnittstellen gehören.
  
## <a name="see-also"></a>Siehe auch

-[MAPI-Features und -Architektur](mapi-features-and-architecture.md)

