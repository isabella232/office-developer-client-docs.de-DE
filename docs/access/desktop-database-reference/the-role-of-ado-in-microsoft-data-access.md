---
title: Rolle von ADO in Microsoft Data Access
TOCTitle: The Role of ADO in Microsoft Data Access
ms:assetid: e9087ec8-850b-ebbe-369a-a5987a528de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250180(v=office.15)
ms:contentKeyID: 48548433
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 91f591513e0a35a70d157b0a640c87efc961fe22
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314035"
---
# <a name="role-of-ado-in-microsoft-data-access"></a><span data-ttu-id="3c8c2-102">Rolle von ADO in Microsoft Data Access</span><span class="sxs-lookup"><span data-stu-id="3c8c2-102">Role of ADO in Microsoft Data Access</span></span>

<span data-ttu-id="3c8c2-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c8c2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3c8c2-p101">Microsoft Data Access Components (MDAC) ermöglicht den Datenzugriff unabhängig von Datenspeichern, Tools und Sprachen. MDAC stellt eine einfach zu handhabende Schnittstelle auf hoher Ebene sowie eine leistungsfähige Schnittstelle auf niedriger Ebene für praktisch jeden verfügbaren Datenspeicher bereit. Dank dieser Flexibilität können Sie verschiedene Datenspeicher integrieren und die gewünschten Tools, Anwendungen und Plattformdienste integrieren, um die passenden Lösungen für Ihre Anforderungen zu erstellen. Diese Technologien liefern die Basis für den allgemeinen Datenzugriff in Microsoft Windows-Betriebssystemen.</span><span class="sxs-lookup"><span data-stu-id="3c8c2-p101">The Microsoft Data Access Components (MDAC) provide data access that is independent of data stores, tools, and languages. It provides a high-level, easy-to-use interface, and a low-level, high-performance interface to practically any data store available. You can use this flexibility to integrate diverse data stores and use your choice of tools, applications, and platform services to create the right solutions for your needs. These technologies provide the basic framework for general-purpose data access in Microsoft Windows operating systems.</span></span>

<span data-ttu-id="3c8c2-p102">In MDAC gibt es drei wichtige Technologien. ActiveX Data Objects (ADO) ist eine einfach zu handhabende Schnittstelle auf hoher Ebene zu OLE DB. OLE DB ist eine leistungsfähige Schnittstelle auf niedriger Ebene zu einer Reihe von Datenspeichern. ADO und OLE DB können beide relationale (tabular) und nicht relationale (hierarchisch oder Datenstrom) Daten verwenden. Open Database Connectivity (ODBC) ist schließlich eine weitere leistungsfähige Schnittstelle auf niedriger Ebene speziell für relationale Datenspeicher.</span><span class="sxs-lookup"><span data-stu-id="3c8c2-p102">There are three primary technologies in MDAC. ActiveX Data Objects (ADO) is a high-level, easy-to-use interface to OLE DB. OLE DB is a low-level, high-performance interface to a variety of data stores. ADO and OLE DB both can work with relational (tabular) and nonrelational (hierarchical or stream) data. Finally, Open Database Connectivity (ODBC) is another low-level, high-performance interface that is designed specifically for relational data stores.</span></span>

<span data-ttu-id="3c8c2-p103">ADO stellt eine Abstraktionsschicht zwischen dem Client oder der Anwendung auf mittlerer Ebene und den OLE DB-Schnittstellen auf niedriger Ebene bereit. ADO verwendet wenige Automatisierungsobjekte, um eine einfache und effiziente Schnittstelle zu OLE DB bereitzustellen. Aufgrund dieser Schnittstelle ist ADO die optimale Wahl für Entwickler, die höher entwickelte Programmiersprachen wie Visual Basic und sogar VBScript verwenden und auf Daten zugreifen möchten, ohne sich mit den Feinheiten von COM und OLE DB vertraut machen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="3c8c2-p103">ADO provides a layer of abstraction between your client or middle-tier application and the low-level OLE DB interfaces. ADO uses a small set of Automation objects to provide a simple and efficient interface to OLE DB. This interface makes ADO the perfect choice for developers in higher level languages, such as Visual Basic and even VBScript, who want to access data without having to learn the intricacies of COM and OLE DB.</span></span>

