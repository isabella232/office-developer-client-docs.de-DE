---
title: Übersicht über die MAPI-Architektur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 00d2993c-d66a-4a00-9fb2-98696d29a007
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8fbb340371a2f7ff5ef6b28fa63af2f4ecc438d5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571479"
---
# <a name="mapi-architecture-overview"></a>Übersicht über die MAPI-Architektur
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI definiert eine modular aufgebaute Architektur, wie in der folgenden Abbildung dargestellt.  
  
![Architektur von Outlook 2010](media/amapi_43.gif "Architektur von Outlook 2010")
  
Die MAPI-Anwendung wird als Clientanwendung bezeichnet, da sie ein Client des MAPI-Subsystems ist. Messaging-basierte Anwendungen verwenden Messaging als zentralen Teil ihrer Verarbeitung und bieten umfangreiche Messaging-Funktionen, z. B. den Austausch von Informationen verschiedener Typen in verschiedenen Formaten und die Möglichkeit, die Informationen lokal zu speichern und zu organisieren. E-Mail-, Planungs- und Arbeitsflussanwendungen sind Beispiele für messagingbasierte Anwendungen.
  
Das MAPI-Subsystem besteht aus einer gemeinsamen Benutzeroberfläche und den Programmierschnittstellen. Bei der allgemeinen Benutzeroberfläche handelt es sich um eine Reihe von Dialogfeldern, die Clientanwendungen ein einheitliches Erscheinungsbild und benutzern eine konsistente Arbeitsweise bieten.
  
DIE MAPI verfügt über Programmierschnittstellen, die vom MAPI-Subsystem, von Clientsoftwareentwicklern und von Dienstanbieterentwicklern verwendet werden. Die MAPI-Programmierschnittstelle ist die wichtigste objektbasierte Programmierschnittstelle. Die MAPI-Programmierschnittstelle ähnelt dem OLE-Komponentenobjektmodell und wird vom MAPI-Subsystem und messagingbasierten Clientanwendungen verwendet, die in C oder C++ geschrieben wurden. 
  
Als Clientsoftwareentwickler führen Sie MAPI-Aufrufe direkt über die MAPI-Programmierschnittstelle durch. Sie können Messaging mit einer einzelnen MAPI-Clientschnittstelle oder einer Kombination von Schnittstellen implementieren. Eine einzelne Anwendung kann Aufrufe von Methoden oder Funktionen ausführen, die zu einer beliebigen Schnittstelle gehören.
  
## <a name="see-also"></a>Siehe auch

-[MAPI-Features und -Architektur](mapi-features-and-architecture.md)

