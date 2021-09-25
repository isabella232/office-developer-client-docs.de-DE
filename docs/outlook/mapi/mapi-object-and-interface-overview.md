---
title: Übersicht über MAPI-Objekt und -Schnittstelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d60f1bc4863986adf3d539c35f924a39e18beda9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595805"
---
# <a name="mapi-object-and-interface-overview"></a>Übersicht über MAPI-Objekt und -Schnittstelle

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein MAPI-Objekt ist eine C++-Objektklasse oder eine C-Datenstruktur, die von einer oder mehreren MAPI-Schnittstellen oder Auflistungen verwandter Funktionen geerbt wird. Diese Sammlungen verwandter Funktionen werden C++-Entwicklern als reine virtuelle Funktionen bezeichnet. Bei einer reinen virtuellen Funktion stellt MAPI nur den Funktionsprototyp und keine Implementierung bereit. Es wird erwartet, dass eine Clientanwendung, ein Dienstanbieter oder eine MAPI diese Implementierung bereitstellt, indem eine Objektklasse erstellt wird, die von der Schnittstelle erbt und den Funktionsbeschreibungen der Messaging-API entspricht. Eine MAPI-Schnittstelle kann nur über eine geerbte Klasse instanziiert werden.
  
Es gibt viele verschiedene MAPI-Objekte, wobei jedes Objekt von einer Schnittstelle erbt, die letztendlich von der [IUnknown-Schnittstelle](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) geerbt wird. **IUnknown** ist die COM-Basisschnittstelle (OLE Component Object Model). Es stellt MAPI-Objekten einen Standardmechanismus für Kommunikation und Steuerung bereit. COM bestimmt, wie Objekt implementierer Probleme wie Speicherverwaltung, Parameterverwaltung und Multithreading behandeln. Durch die Konformität mit diesem Modell hält ein Objekt implementierer einen Vertrag gemäß den Schnittstellen im Objekt ein. 
  
Viele MAPI-Schnittstellen werden direkt von **IUnknown** geerbt, während andere indirekt über eine von zwei anderen Basisschnittstellen geerbt werden: [IMAPIProp : IUnknown](imapipropiunknown.md) für die Eigenschaftenverwaltung und [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) für Ordner- und Adressbuchzugriff. Basisschnittstellen werden nie als separate eigenständige Objekte implementiert. sie werden immer als Teil anderer Objekte implementiert, d. h. Objekte, die abgeleitete Schnittstellen implementieren. 
  
MAPI definiert viele Objekttypen, die jeweils von einer oder mehreren MAPI-Komponenten implementiert werden. Von Clients implementierte Objekte werden von mapi, von Dienstanbietern und von benutzerdefinierten Formularkomponenten verwendet. Objekte, die von Dienstanbietern implementiert werden, werden in der Regel von der MAPI und von Clients verwendet. Objekte, die von Formularbibliotheksanbietern und Formularservern implementiert werden, werden von anderen Formularkomponenten und von Clients verwendet. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MAPI-Konzepte (engl.)](mapi-concepts.md)

