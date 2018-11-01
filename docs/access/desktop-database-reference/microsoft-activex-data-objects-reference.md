---
title: Referenz zu Microsoft ActiveX Data Objects
TOCTitle: Microsoft ActiveX Data Objects Reference
ms:assetid: 235fc575-8a2e-913c-fa3d-bb86256733f9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249010(v=office.15)
ms:contentKeyID: 48543728
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 54d605beb0f6653695dafcd4a9ffffeb2f097d5b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871430"
---
# <a name="microsoft-activex-data-objects-reference"></a><span data-ttu-id="342e1-102">Referenz zu Microsoft ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="342e1-102">Microsoft ActiveX Data Objects reference</span></span>

<span data-ttu-id="342e1-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="342e1-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="purpose"></a><span data-ttu-id="342e1-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="342e1-104">Purpose</span></span>

<span data-ttu-id="342e1-p101">Mit Microsoft ActiveX Data Objects (ADO) können Clientanwendungen über einen OLE DB-Anbieter auf Daten auf einem Datenbankserver zugreifen und diese bearbeiten. Die wichtigsten Vorteile sind einfache Handhabung, hohe Geschwindigkeit sowie geringer Arbeitsspeicher- und Speicherplatzbedarf. ADO unterstützt Schlüsselfeatures für das Erstellen von Client-/Server- und webbasierten Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="342e1-p101">Microsoft ActiveX Data Objects (ADO) enable your client applications to access and manipulate data from a database server through an OLE DB provider. Its primary benefits are ease of use, high speed, low memory overhead, and a small disk footprint. ADO supports key features for building client/server and Web-based applications.</span></span>

## <a name="rds"></a><span data-ttu-id="342e1-108">RDS</span><span class="sxs-lookup"><span data-stu-id="342e1-108">RDS</span></span>

<span data-ttu-id="342e1-109">ADO bietet außerdem Remote Data Service (RDS), mit dem Sie Daten von einem Server zu einer Clientanwendung oder eine Webseite, die Daten auf dem Client manipulieren und Updates auf dem Server in einer einzelnen Roundtrip wieder verschieben können.</span><span class="sxs-lookup"><span data-stu-id="342e1-109">ADO also features Remote Data Service (RDS), by which you can move data from a server to a client application or webpage, manipulate the data on the client, and return updates to the server in a single round trip.</span></span>

## <a name="ado-md"></a><span data-ttu-id="342e1-110">ADO MD</span><span class="sxs-lookup"><span data-stu-id="342e1-110">ADO MD</span></span>

<span data-ttu-id="342e1-p102">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) ermöglicht den einfachen Zugriff auf multidimensionale Daten in Sprachen wie z. B. Microsoft Visual Basic, Microsoft Visual C++ und Microsoft Visual J++. ADO MD erweitert Microsoft ActiveX Data Objects (ADO) um Objekte speziell für multidimensionale Daten, wie z. B. die CubeDef- und Cellset-Objekte. Mit ADO MD können Sie ein multidimensionales Schema durchsuchen, einen Cube abfragen und die Ergebnisse abrufen.</span><span class="sxs-lookup"><span data-stu-id="342e1-p102">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++. ADO MD extends Microsoft ActiveX Data Objects (ADO) to include objects specific to multidimensional data, such as the CubeDef and Cellset objects. With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="342e1-p103">ADO MD verwendet wie ADO einen zugrunde liegenden OLE DB-Anbieter für den Zugriff auf Daten. Der Anbieter muss gemäß der OLE DB für OLAP-Spezifikation ein multidimensionaler Datenprovider (MDP) sein, um mit ADO MD arbeiten zu können. MDPs stellen Daten in multidimensionalen Ansichten dar. Tabulare Datenprovider (TDP) stellen Daten dagegen in tabularen Ansichten dar. In der Dokumentation zu Ihrem OLE DB für OLAP-Anbieter finden Sie ausführlichere Information zur Syntax und zu den Funktionen, die von Ihrem Anbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="342e1-p103">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data. To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification. MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views. Refer to the documentation for your OLAP OLE DB provider for more detailed information on the specific syntax and behaviors supported by your provider.</span></span>

## <a name="adox"></a><span data-ttu-id="342e1-118">ADOX</span><span class="sxs-lookup"><span data-stu-id="342e1-118">ADOX</span></span>

<span data-ttu-id="342e1-p104">Microsoft ActiveX Data Objects Extensions für Datendefinitionssprache und Sicherheit (ADOX) ist eine Erweiterung der ADO-Objekte und des Programmiermodells. ADOX enthält Objekte zum Erstellen und Ändern von Schemas sowie zur Sicherheit. Da es sich um einen objektbasierten Ansatz zur Schemabearbeitung handelt, können Sie Code erstellen, der für verschiedene Datenquellen verwendet werden kann, ungeachtet der Unterschiede in der jeweiligen Syntax.</span><span class="sxs-lookup"><span data-stu-id="342e1-p104">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model. ADOX includes objects for schema creation and modification, as well as security. Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="342e1-p105">ADOX ist eine Begleitbibliothek zu ADO-Kernobjekten. Hiermit werden zusätzliche Objekte für das Erstellen, Ändern und Löschen von Schemaobjekten wie Tabellen und Prozeduren verfügbar gemacht. Außerdem enthält dieses Element Sicherheitsobjekte, um Benutzer und Gruppen zu warten und um Berechtigungen für Objekte zu erteilen und aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="342e1-p105">ADOX is a companion library to the core ADO objects. It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures. It also includes security objects to maintain users and groups and to grant and revoke permissions on objects.</span></span>

## <a name="ado-25-main-components"></a><span data-ttu-id="342e1-125">ADO 2.5 Hauptkomponenten</span><span class="sxs-lookup"><span data-stu-id="342e1-125">ADO 2.5 main components</span></span>

- <span data-ttu-id="342e1-126">[Programmierhandbuch](ado-programmer-s-guide.md): eine Einführung in die Verwendung von ADO, RDS, ADO MD und ADOX.</span><span class="sxs-lookup"><span data-stu-id="342e1-126">[Programmer's guide](ado-programmer-s-guide.md): An introduction to using ADO, RDS, ADO MD, and ADOX.</span></span>

- <span data-ttu-id="342e1-127">[Programmer's Reference](ado-programmer-s-reference-topics.md): in diesem Abschnitt der ADO-Dokumentation enthält Themen jede Auflistung von ADO, RDS, ADO MD und ADOX-Objekt, -Eigenschaft, dynamische Eigenschaft, -Methode, -Ereignis, und -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="342e1-127">[Programmer's reference](ado-programmer-s-reference-topics.md): This section of the ADO documentation contains topics for each ADO, RDS, ADO MD, and ADOX object, collection, property, dynamic property, method, event, and enumeration.</span></span>

## <a name="feedback"></a><span data-ttu-id="342e1-128">Feedback</span><span class="sxs-lookup"><span data-stu-id="342e1-128">Feedback</span></span>

<span data-ttu-id="342e1-129">Feedback zu ADO-Dokumentation oder Beispielen können Sie direkt an das ADO-Dokumentationsteam senden.</span><span class="sxs-lookup"><span data-stu-id="342e1-129">You can send feedback about ADO documentation or samples directly to the ADO documentation team.</span></span>

