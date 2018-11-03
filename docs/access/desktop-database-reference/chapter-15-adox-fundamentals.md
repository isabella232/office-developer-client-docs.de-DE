---
title: 'Kapitel 15: Grundlegendes zu ADOX'
TOCTitle: 'Chapter 15: ADOX fundamentals'
ms:assetid: 973d7579-4f34-3b31-a761-a951ab29e850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249673(v=office.15)
ms:contentKeyID: 48546464
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6b410fcaa81aa847732e530bd18bc18200f04ebc
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936868"
---
# <a name="chapter-15-adox-fundamentals"></a><span data-ttu-id="d7127-102">Kapitel 15: Grundlegendes zu ADOX</span><span class="sxs-lookup"><span data-stu-id="d7127-102">Chapter 15: ADOX fundamentals</span></span>

<span data-ttu-id="d7127-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7127-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d7127-p101">Microsoft ActiveX Data Objects Extensions für Datendefinitionssprache und Sicherheit (ADOX) ist eine Erweiterung der ADO-Objekte und des Programmiermodells. ADOX enthält Objekte zum Erstellen und Ändern von Schemas sowie zur Sicherheit. Da es sich um einen objektbasierten Ansatz zur Schemabearbeitung handelt, können Sie Code erstellen, der für verschiedene Datenquellen verwendet werden kann, ungeachtet der Unterschiede in der jeweiligen Syntax.</span><span class="sxs-lookup"><span data-stu-id="d7127-p101">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model. ADOX includes objects for schema creation and modification, as well as security. Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="d7127-p102">ADOX ist eine Begleitbibliothek zu den ADO-Hauptobjekten. ADOX stellt zusätzliche Objekte zum Erstellen, Bearbeiten und Löschen von Schemaobjekten wie Tabellen und Prozeduren bereit. Es schließt außerdem Sicherheitsobjekte zum Verwalten von Benutzern und Gruppen und zum Erteilen und Aufheben von Berechtigungen für Objekte ein.</span><span class="sxs-lookup"><span data-stu-id="d7127-p102">ADOX is a companion library to the core ADO objects. It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures. It also includes security objects to maintain users and groups and to grant and revoke permissions on objects.</span></span>

<span data-ttu-id="d7127-p103">Zur Verwendung von ADOX mit einem Entwicklungstool sollten Sie einen Verweis zur ADOX-Typbibliothek einrichten. Die Beschreibung der ADOX-Bibliothek finden Sie unter "Microsoft ADO Ext. for DDL and Security." Der Dateiname der ADOX-Bibliothek ist Msadox.dll. Die Programm-ID (ProgID) lautet "ADOX". Weitere Informationen zum Erstellen von Verweisen zu Bibliotheken finden Sie in der Dokumentation Ihres Entwicklungstools.</span><span class="sxs-lookup"><span data-stu-id="d7127-p103">To use ADOX with your development tool, you should establish a reference to the ADOX type library. The description of the ADOX library is "Microsoft ADO Ext. for DDL and Security." The ADOX library file name is Msadox.dll, and the program ID (ProgID) is "ADOX". For more information about establishing references to libraries, see the documentation of your development tool.</span></span>

<span data-ttu-id="d7127-p104">Der Microsoft OLE DB-Anbieter für das Microsoft Jet-Datenbankmodul unterstützt ADOX vollständig. Abhängig vom jeweiligen Datenprovider werden bestimmte Features von ADOX möglicherweise nicht unterstützt. Weitere Informationen zu unterstützten Features mit dem Microsoft OLE DB-Anbieter für ODBC, dem Microsoft OLE DB-Anbieter für Oracle oder dem Microsoft SQL Server OLE DB-Anbieter finden Sie in der MDAC-Infodatei.</span><span class="sxs-lookup"><span data-stu-id="d7127-p104">The Microsoft OLE DB Provider for the Microsoft Jet Database Engine fully supports ADOX. Certain features of ADOX may not be supported, depending on your data provider. For more information about supported features with the Microsoft OLE DB Provider for ODBC, the Microsoft OLE DB Provider for Oracle, or the Microsoft SQL Server OLE DB Provider, see the MDAC readme file.</span></span>

<span data-ttu-id="d7127-117">In diesem Dokument wird davon ausgegangen Kenntnisse in der Programmiersprache Microsoft Visual Basic sowie allgemeine Kenntnisse von ADO.</span><span class="sxs-lookup"><span data-stu-id="d7127-117">This document assumes a working knowledge of the Microsoft Visual Basic programming language and a general knowledge of ADO.</span></span> <span data-ttu-id="d7127-118">Weitere Informationen zu ADO finden Sie in der [ADO-Programmierhandbuch](ado-programmer-s-guide.md).</span><span class="sxs-lookup"><span data-stu-id="d7127-118">For more information about ADO, see the [ADO programmer's guide](ado-programmer-s-guide.md).</span></span>

<span data-ttu-id="d7127-119">In diesem Kapitel werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="d7127-119">This chapter covers the following topic:</span></span>

- [<span data-ttu-id="d7127-120">Anbieterunterstützung für ADOX</span><span class="sxs-lookup"><span data-stu-id="d7127-120">Provider support for ADOX</span></span>](provider-support-for-adox.md)

<span data-ttu-id="d7127-121">Weitere grundlegende Informationen zu ADOX finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="d7127-121">For more overview information about ADOX, see the following topics:</span></span>

- [<span data-ttu-id="d7127-122">ADOX-Objekte</span><span class="sxs-lookup"><span data-stu-id="d7127-122">ADOX objects</span></span>](adox-objects.md)
- [<span data-ttu-id="d7127-123">ADOX-Auflistungen</span><span class="sxs-lookup"><span data-stu-id="d7127-123">ADOX collections</span></span>](adox-collections.md)
- [<span data-ttu-id="d7127-124">ADOX-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d7127-124">ADOX properties</span></span>](adox-properties.md)
- [<span data-ttu-id="d7127-125">ADOX-Methoden</span><span class="sxs-lookup"><span data-stu-id="d7127-125">ADOX methods</span></span>](adox-methods.md)
- [<span data-ttu-id="d7127-126">ADOX-Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7127-126">ADOX examples</span></span>](adox-code-examples.md)

