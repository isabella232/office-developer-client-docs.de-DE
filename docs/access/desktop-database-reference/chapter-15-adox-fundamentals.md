---
title: 'Kapitel 15: Grundlegendes zu ADOX'
TOCTitle: 'Chapter 15: ADOX fundamentals'
ms:assetid: 973d7579-4f34-3b31-a761-a951ab29e850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249673(v=office.15)
ms:contentKeyID: 48546464
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0e46920ba47dba018944768ff61c970781e37a02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296451"
---
# <a name="chapter-15-adox-fundamentals"></a><span data-ttu-id="775b7-102">Kapitel 15: Grundlegendes zu ADOX</span><span class="sxs-lookup"><span data-stu-id="775b7-102">Chapter 15: ADOX fundamentals</span></span>

<span data-ttu-id="775b7-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="775b7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="775b7-p101">Microsoft ActiveX Data Objects Extensions für Datendefinitionssprache und Sicherheit (ADOX) ist eine Erweiterung der ADO-Objekte und des Programmiermodells. ADOX enthält Objekte zum Erstellen und Ändern von Schemas sowie zur Sicherheit. Da es sich um einen objektbasierten Ansatz zur Schemabearbeitung handelt, können Sie Code erstellen, der für verschiedene Datenquellen verwendet werden kann, ungeachtet der Unterschiede in der jeweiligen Syntax.</span><span class="sxs-lookup"><span data-stu-id="775b7-p101">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model. ADOX includes objects for schema creation and modification, as well as security. Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="775b7-p102">ADOX ist eine Begleitbibliothek zu ADO-Kernobjekten. Hiermit werden zusätzliche Objekte für das Erstellen, Ändern und Löschen von Schemaobjekten wie Tabellen und Prozeduren verfügbar gemacht. Außerdem enthält dieses Element Sicherheitsobjekte, um Benutzer und Gruppen zu warten und um Berechtigungen für Objekte zu erteilen und aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="775b7-p102">ADOX is a companion library to the core ADO objects. It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures. It also includes security objects to maintain users and groups and to grant and revoke permissions on objects.</span></span>

<span data-ttu-id="775b7-p103">To use ADOX with your development tool, you should establish a reference to the ADOX type library. The description of the ADOX library is "Microsoft ADO Ext. for DDL and Security." The ADOX library file name is Msadox.dll, and the program ID (ProgID) is "ADOX". For more information about establishing references to libraries, see the documentation of your development tool.</span><span class="sxs-lookup"><span data-stu-id="775b7-p103">To use ADOX with your development tool, you should establish a reference to the ADOX type library. The description of the ADOX library is "Microsoft ADO Ext. for DDL and Security." The ADOX library file name is Msadox.dll, and the program ID (ProgID) is "ADOX". For more information about establishing references to libraries, see the documentation of your development tool.</span></span>

<span data-ttu-id="775b7-p104">Der Microsoft OLE DB-Anbieter für das Microsoft Jet-Datenbankmodul unterstützt ADOX vollständig. Abhängig vom jeweiligen Datenprovider werden bestimmte Features von ADOX möglicherweise nicht unterstützt. Weitere Informationen zu unterstützten Features mit dem Microsoft OLE DB-Anbieter für ODBC, dem Microsoft OLE DB-Anbieter für Oracle oder dem Microsoft SQL Server OLE DB-Anbieter finden Sie in der MDAC-Infodatei.</span><span class="sxs-lookup"><span data-stu-id="775b7-p104">The Microsoft OLE DB Provider for the Microsoft Jet Database Engine fully supports ADOX. Certain features of ADOX may not be supported, depending on your data provider. For more information about supported features with the Microsoft OLE DB Provider for ODBC, the Microsoft OLE DB Provider for Oracle, or the Microsoft SQL Server OLE DB Provider, see the MDAC readme file.</span></span>

<span data-ttu-id="775b7-117">In diesem Dokument werden Kenntnisse der Microsoft Visual Basic-Programmiersprache und allgemeine ADO-Kenntnisse vorausgesetzt.</span><span class="sxs-lookup"><span data-stu-id="775b7-117">This document assumes a working knowledge of the Microsoft Visual Basic programming language and a general knowledge of ADO.</span></span> <span data-ttu-id="775b7-118">Weitere Informationen zu ADO finden Sie im [ADO-Programmierhandbuch](ado-programmer-s-guide.md).</span><span class="sxs-lookup"><span data-stu-id="775b7-118">For more information about ADO, see the [ADO programmer's guide](ado-programmer-s-guide.md).</span></span>

<span data-ttu-id="775b7-119">In diesem Kapitel wird Folgendes Thema behandelt:</span><span class="sxs-lookup"><span data-stu-id="775b7-119">This chapter covers the following topic:</span></span>

- [<span data-ttu-id="775b7-120">Anbieterunterstützung für ADOX</span><span class="sxs-lookup"><span data-stu-id="775b7-120">Provider support for ADOX</span></span>](provider-support-for-adox.md)

<span data-ttu-id="775b7-121">Weitere grundlegende Informationen zu ADOX finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="775b7-121">For more overview information about ADOX, see the following topics:</span></span>

- [<span data-ttu-id="775b7-122">ADOX-Objekte</span><span class="sxs-lookup"><span data-stu-id="775b7-122">ADOX objects</span></span>](adox-objects.md)
- [<span data-ttu-id="775b7-123">ADOX-Auflistungen</span><span class="sxs-lookup"><span data-stu-id="775b7-123">ADOX collections</span></span>](adox-collections.md)
- [<span data-ttu-id="775b7-124">ADOX-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="775b7-124">ADOX properties</span></span>](adox-properties.md)
- [<span data-ttu-id="775b7-125">ADOX-Methoden</span><span class="sxs-lookup"><span data-stu-id="775b7-125">ADOX methods</span></span>](adox-methods.md)
- [<span data-ttu-id="775b7-126">ADOX-Beispiele</span><span class="sxs-lookup"><span data-stu-id="775b7-126">ADOX examples</span></span>](adox-code-examples.md)

