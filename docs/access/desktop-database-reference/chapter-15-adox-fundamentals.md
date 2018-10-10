---
title: 'Kapitel 15: Grundlegendes zu ADOX'
TOCTitle: 'Chapter 15: ADOX Fundamentals'
ms:assetid: 973d7579-4f34-3b31-a761-a951ab29e850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249673(v=office.15)
ms:contentKeyID: 48546464
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3869f23b93df78fd207812a85f91dd3272bd255f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475706"
---
# <a name="chapter-15-adox-fundamentals"></a><span data-ttu-id="391c5-102">Kapitel 15: Grundlegendes zu ADOX</span><span class="sxs-lookup"><span data-stu-id="391c5-102">Chapter 15: ADOX Fundamentals</span></span>


<span data-ttu-id="391c5-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="391c5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="391c5-p101">Microsoft® ActiveX® Data Objects Extensions for Data Definition Language and Security (ADOX) ist eine Erweiterung des ADO-Objekt- und Programmiermodells. ADOX umfasst Objekte für die Schemaerstellung und -bearbeitung sowie Sicherheitsobjekte. Da es sich um einen objektbasierten Ansatz für die Schemamanipulation handelt, können Sie Code schreiben, der für verschiedene Datenquellen verwendbar ist, unabhängig von Unterschieden der jeweiligen systemeigenen Syntax.</span><span class="sxs-lookup"><span data-stu-id="391c5-p101">Microsoft® ActiveX® Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model. ADOX includes objects for schema creation and modification, as well as security. Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="391c5-p102">ADOX ist eine Begleitbibliothek zu den ADO-Hauptobjekten. ADOX stellt zusätzliche Objekte zum Erstellen, Bearbeiten und Löschen von Schemaobjekten wie Tabellen und Prozeduren bereit. Es schließt außerdem Sicherheitsobjekte zum Verwalten von Benutzern und Gruppen und zum Erteilen und Aufheben von Berechtigungen für Objekte ein.</span><span class="sxs-lookup"><span data-stu-id="391c5-p102">ADOX is a companion library to the core ADO objects. It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures. It also includes security objects to maintain users and groups and to grant and revoke permissions on objects.</span></span>

<span data-ttu-id="391c5-p103">Zur Verwendung von ADOX mit einem Entwicklungstool sollten Sie einen Verweis zur ADOX-Typbibliothek einrichten. Die Beschreibung der ADOX-Bibliothek finden Sie unter "Microsoft ADO Ext. for DDL and Security." Der Dateiname der ADOX-Bibliothek ist Msadox.dll. Die Programm-ID (ProgID) lautet "ADOX". Weitere Informationen zum Erstellen von Verweisen zu Bibliotheken finden Sie in der Dokumentation Ihres Entwicklungstools.</span><span class="sxs-lookup"><span data-stu-id="391c5-p103">To use ADOX with your development tool, you should establish a reference to the ADOX type library. The description of the ADOX library is "Microsoft ADO Ext. for DDL and Security." The ADOX library file name is Msadox.dll, and the program ID (ProgID) is "ADOX". For more information about establishing references to libraries, see the documentation of your development tool.</span></span>

<span data-ttu-id="391c5-p104">Der Microsoft OLE DB-Anbieter für das Microsoft Jet-Datenbankmodul unterstützt ADOX vollständig. Abhängig vom jeweiligen Datenprovider werden bestimmte Features von ADOX möglicherweise nicht unterstützt. Weitere Informationen zu unterstützten Features mit dem Microsoft OLE DB-Anbieter für ODBC, dem Microsoft OLE DB-Anbieter für Oracle oder dem Microsoft SQL Server OLE DB-Anbieter finden Sie in der MDAC-Infodatei.</span><span class="sxs-lookup"><span data-stu-id="391c5-p104">The Microsoft OLE DB Provider for the Microsoft Jet Database Engine fully supports ADOX. Certain features of ADOX may not be supported, depending on your data provider. For more information about supported features with the Microsoft OLE DB Provider for ODBC, the Microsoft OLE DB Provider for Oracle, or the Microsoft SQL Server OLE DB Provider, see the MDAC readme file.</span></span>

<span data-ttu-id="391c5-p105">Dieses Dokument setzt Erfahrung in der Verwendung der Programmiersprache Microsoft® Visual Basic® und grundlegende ADO-Kenntnisse voraus. Weitere Informationen zu ADO finden Sie im [ADO-Programmierhandbuch](ado-programmer-s-guide.md). Weitere grundlegende Informationen zu ADOX finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="391c5-p105">This document assumes a working knowledge of the Microsoft® Visual Basic® programming language and a general knowledge of ADO. For more information about ADO, see the [ADO Programmer's Guide](ado-programmer-s-guide.md). For more overview information about ADOX, see the following topics:</span></span>

  - [<span data-ttu-id="391c5-120">ADOX-Objekte </span><span class="sxs-lookup"><span data-stu-id="391c5-120">ADOX Objects</span></span>](adox-objects.md)

  - [<span data-ttu-id="391c5-121">ADOX-Auflistungen</span><span class="sxs-lookup"><span data-stu-id="391c5-121">ADOX Collections</span></span>](adox-collections.md)

  - [<span data-ttu-id="391c5-122">ADOX-Eigenschaften </span><span class="sxs-lookup"><span data-stu-id="391c5-122">ADOX Properties</span></span>](adox-properties.md)

  - [<span data-ttu-id="391c5-123">ADOX-Methoden </span><span class="sxs-lookup"><span data-stu-id="391c5-123">ADOX Methods</span></span>](adox-methods.md)

  - [<span data-ttu-id="391c5-124">ADOX-Beispiele </span><span class="sxs-lookup"><span data-stu-id="391c5-124">ADOX Examples</span></span>](adox-code-examples.md)

