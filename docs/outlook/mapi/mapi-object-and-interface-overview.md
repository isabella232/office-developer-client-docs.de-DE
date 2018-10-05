---
title: MAPI-Objekt und Übersicht über die Benutzeroberfläche
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fcd85bf518f4e6466bf15a09e417767bc34df78d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390989"
---
# <a name="mapi-object-and-interface-overview"></a>MAPI-Objekt und Übersicht über die Benutzeroberfläche

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein MAPI-Objekt ist eine C++-Objektklassen oder C-Datenstruktur, die von einer oder mehreren MAPI-Schnittstellen oder Sammlungen verwandter Funktionen geerbt wird. Diese Sammlungen verwandter Funktionen werden als reinen virtuellen Funktionen für C++-Entwickler bezeichnet. Bei einer reinen virtuellen Funktion liefert MAPI nur Funktionsprototyp keine Implementierung. Es wird erwartet, dass eine Clientanwendung, einem Dienstanbieter oder MAPI dieser Implementierung leistet durch Erstellen einer Objektklassen, die von der Schnittstelle erbt und die Funktion Beschreibungen der Messaging-API entspricht. Eine MAPI-Schnittstelle kann nur über eine geerbte Klasse instanziiert werden.
  
Es gibt viele verschiedene MAPI-Objekte, jedes Objekt erben von eine Schnittstelle, die letztlich vom die [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) -Schnittstelle geerbt wird. **IUnknown** ist die Basis OLE Component Object Model (COM)-Schnittstelle. Softwareentwicklern MAPI-Objekte mit einem standard Mechanismus für die Kommunikation und Steuerelement. COM bestimmt Behandlung Objekt Implementierer Probleme wie Arbeitsspeicher Parameter Management, Verwaltung und multithreading. Durch dieses Modell angleichen, wird ein Objekt Implementierer einen Vertrag gemäß von den Schnittstellen im Objekt eingeschlossen. 
  
Viele MAPI-Schnittstellen geerbt werden direkt von **IUnknown**, während andere indirekt über eine der beiden anderen Basiskalender Schnittstellen vererbt werden: [IMAPIProp: IUnknown](imapipropiunknown.md) für die Eigenschaft Verwaltung und [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) für Ordner und Address Book Zugriff. Base-Schnittstellen werden nie als separate, eigenständige Objekte implementiert. Sie werden immer als Teil des anderen Objekten implementiert, abgeleitete Objekte, mit denen implementiert Schnittstellen. 
  
MAPI definiert viele andere Arten von Objekten, die jeweils durch eine oder mehrere MAPI-Komponenten implementiert. Objekte, die von Clients implementiert werden von MAPI, Dienstanbieter und benutzerdefinierte Formularkomponenten verwendet. Objekte, die vom Dienstanbieter implementiert werden in der Regel durch MAPI- und -Clients verwendet. Objekte von Formular Bibliothek Anbietern implementiert und Formular Servern werden von anderen Formularkomponenten und -Clients verwendet. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MAPI-Konzepte](mapi-concepts.md)

