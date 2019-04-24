---
title: Übersicht über MAPI-Objekte und-Schnittstellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fcd85bf518f4e6466bf15a09e417767bc34df78d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345787"
---
# <a name="mapi-object-and-interface-overview"></a>Übersicht über MAPI-Objekte und-Schnittstellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bei einem MAPI-Objekt handelt es sich um eine C++-Objektklasse oder eine C-Datenstruktur, die von einer oder mehreren MAPI-Schnittstellen geerbt wurde, oder Auflistungen verwandter Funktionen. Diese Auflistungen verwandter Funktionen sind C++-Entwicklern als reine virtuelle Funktionen bekannt. Für eine reine virtuelle Funktion liefert MAPI nur den Funktionsprototyp, keine Implementierung. Es wird erwartet, dass eine Clientanwendung, ein Dienstanbieter oder eine MAPI diese Implementierung bereitstellt, indem eine Objektklasse erstellt wird, die von der Schnittstelle erbt und den Funktionsbeschreibungen der Messaging-API entspricht. Eine MAPI-Schnittstelle kann nur über eine geerbte Klasse instanziiert werden.
  
Es gibt viele verschiedene MAPI-Objekte, jedes Objekt erbt von einer Schnittstelle, die letztlich von der [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) -Schnittstelle geerbt wird. **IUnknown** ist die OLE Component Object Model (com)-Basisschnittstelle. MAPI-Objekte werden mit einem Standardmechanismus für die Kommunikation und Steuerung bereitgestellt. COM bestimmt, wie Objekt Implementierer Probleme wie Speicherverwaltung, Parameterverwaltung und Multithreading behandeln. Durch die Übereinstimmung mit diesem Modell wird ein objektimplementierer an einen Vertrag gemäß den Schnittstellen des Objekts gebunden. 
  
Viele MAPI-Schnittstellen werden direkt von **IUnknown**geerbt, während andere indirekt über eine der beiden anderen Basisschnittstellen vererbt werden: [IMAPIProp: IUnknown](imapipropiunknown.md) für Property Management und [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) für Folder und Zugriff auf das Adressbuch. Basisschnittstellen werden nie als separate, eigenständige Objekte implementiert; Sie werden immer als Teil anderer Objekte implementiert, die abgeleitete Schnittstellen implementieren. 
  
MAPI definiert viele Objekttypen, die jeweils von einer oder mehreren MAPI-Komponenten implementiert werden. Von Clients implementierte Objekte werden von MAPI, von Dienstanbietern und von benutzerdefinierten Formularkomponenten verwendet. Von Dienstanbietern implementierte Objekte werden in der Regel von MAPI und von Clients verwendet. Von Formular Bibliotheks Anbietern und Formular Servern implementierte Objekte werden von anderen Formularkomponenten und von Clients verwendet. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MAPI-Konzepte (engl.)](mapi-concepts.md)

