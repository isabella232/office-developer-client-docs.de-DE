---
title: Rolle von ADO in Microsoft Data Access
TOCTitle: The Role of ADO in Microsoft Data Access
ms:assetid: e9087ec8-850b-ebbe-369a-a5987a528de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250180(v=office.15)
ms:contentKeyID: 48548433
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b0812e87c961110f6ee7afc8e0909c85b6197df3
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944949"
---
# <a name="role-of-ado-in-microsoft-data-access"></a>Rolle von ADO in Microsoft Data Access

**Betrifft**: Access 2013, Office 2013

Microsoft Data Access Components (MDAC) ermöglicht den Datenzugriff unabhängig von Datenspeichern, Tools und Sprachen. MDAC stellt eine einfach zu handhabende Schnittstelle auf hoher Ebene sowie eine leistungsfähige Schnittstelle auf niedriger Ebene für praktisch jeden verfügbaren Datenspeicher bereit. Dank dieser Flexibilität können Sie verschiedene Datenspeicher integrieren und die gewünschten Tools, Anwendungen und Plattformdienste integrieren, um die passenden Lösungen für Ihre Anforderungen zu erstellen. Diese Technologien liefern die Basis für den allgemeinen Datenzugriff in Microsoft Windows-Betriebssystemen.

In MDAC gibt es drei wichtige Technologien. ActiveX Data Objects (ADO) ist eine einfach zu handhabende Schnittstelle auf hoher Ebene zu OLE DB. OLE DB ist eine leistungsfähige Schnittstelle auf niedriger Ebene zu einer Reihe von Datenspeichern. ADO und OLE DB können beide relationale (tabular) und nicht relationale (hierarchisch oder Datenstrom) Daten verwenden. Open Database Connectivity (ODBC) ist schließlich eine weitere leistungsfähige Schnittstelle auf niedriger Ebene speziell für relationale Datenspeicher.

ADO stellt eine Abstraktionsschicht zwischen dem Client oder der Anwendung auf mittlerer Ebene und den OLE DB-Schnittstellen auf niedriger Ebene bereit. ADO verwendet wenige Automatisierungsobjekte, um eine einfache und effiziente Schnittstelle zu OLE DB bereitzustellen. Aufgrund dieser Schnittstelle ist ADO die optimale Wahl für Entwickler, die höher entwickelte Programmiersprachen wie Visual Basic und sogar VBScript verwenden und auf Daten zugreifen möchten, ohne sich mit den Feinheiten von COM und OLE DB vertraut machen zu müssen.

