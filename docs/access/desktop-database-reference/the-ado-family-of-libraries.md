---
title: ADO-bibliotheksfamilie
TOCTitle: The ADO family of libraries
ms:assetid: 9e794509-d0a8-2e5b-02a8-65e26f059c4e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249724(v=office.15)
ms:contentKeyID: 48546656
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 821de4312d3fa76468311305b18eaaa156e05318
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999043"
---
# <a name="the-ado-family-of-libraries"></a><span data-ttu-id="023cf-102">ADO-bibliotheksfamilie</span><span class="sxs-lookup"><span data-stu-id="023cf-102">The ADO family of libraries</span></span>

<span data-ttu-id="023cf-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="023cf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="023cf-104">Die ADO-Familie besteht aus drei Hauptbibliotheken: ADO (einschließlich RDS), ADO MD und ADOX.</span><span class="sxs-lookup"><span data-stu-id="023cf-104">Three major libraries make up the ADO family: ADO (including RDS), ADO MD, and ADOX.</span></span>

## <a name="ado"></a><span data-ttu-id="023cf-105">ADO</span><span class="sxs-lookup"><span data-stu-id="023cf-105">ADO</span></span>

<span data-ttu-id="023cf-106">Mit ADO können Clientanwendungen über einen OLE DB-Anbieter auf Daten auf einem Datenbankserver zugreifen und diese bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="023cf-106">ADO enables your client applications to access and manipulate data from a database server through an OLE DB provider.</span></span> <span data-ttu-id="023cf-107">Die wichtigsten Vorteile von ADO sind einfache Handhabung, hohe Geschwindigkeit sowie geringer Arbeitsspeicher- und Speicherplatzbedarf.</span><span class="sxs-lookup"><span data-stu-id="023cf-107">The primary benefits of ADO are ease of use, high speed, low memory overhead, and a small disk footprint.</span></span> <span data-ttu-id="023cf-108">ADO unterstützt wichtige Features für die Erstellung von Client-Server und webbasierten Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="023cf-108">ADO supports key features for building client/server and web-based applications.</span></span>

<span data-ttu-id="023cf-109">ADO bietet außerdem Remote Data Service (RDS), mit dem Sie Daten von einem Server zu einer Clientanwendung oder eine Webseite, die Daten auf dem Client manipulieren und Updates auf dem Server in einer einzelnen Roundtrip wieder verschieben können.</span><span class="sxs-lookup"><span data-stu-id="023cf-109">ADO also features Remote Data Service (RDS), by which you can move data from a server to a client application or webpage, manipulate the data on the client, and return updates to the server in a single round trip.</span></span>

## <a name="ado-md"></a><span data-ttu-id="023cf-110">ADO MD</span><span class="sxs-lookup"><span data-stu-id="023cf-110">ADO MD</span></span>

<span data-ttu-id="023cf-p102">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) ermöglicht den einfachen Zugriff auf multidimensionale Daten in Sprachen wie z. B. Microsoft Visual Basic, Microsoft Visual C++ und Microsoft Visual J++. ADO MD erweitert ADO um Objekte speziell für multidimensionale Daten, wie z. B. die Objekte **CubeDef** und **Cellset**. Mit ADO MD können Sie ein multidimensionales Schema durchsuchen, einen Cube abfragen und die Ergebnisse abrufen.</span><span class="sxs-lookup"><span data-stu-id="023cf-p102">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++. ADO MD extends ADO to include objects specific to multidimensional data, such as the **CubeDef** and **Cellset** objects. With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="023cf-p103">ADO MD verwendet wie ADO einen zugrunde liegenden OLE DB-Anbieter für den Zugriff auf Daten. Der Anbieter muss gemäß der OLE DB für OLAP-Spezifikation ein multidimensionaler Datenprovider (MDP) sein, um mit ADO MD arbeiten zu können. MDPs stellen Daten in multidimensionalen Ansichten dar. Tabulare Datenprovider (TDP) stellen Daten dagegen in tabularen Ansichten dar. In der Dokumentation zu Ihrem OLE DB für OLAP-Anbieter finden Sie ausführlichere Information zur Syntax und zu den Funktionen, die von Ihrem Anbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="023cf-p103">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data. To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification. MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views. Refer to the documentation for your OLE DB for OLAP provider for more detailed information about the specific syntax and behaviors supported by your provider.</span></span>

## <a name="adox"></a><span data-ttu-id="023cf-118">ADOX</span><span class="sxs-lookup"><span data-stu-id="023cf-118">ADOX</span></span>

<span data-ttu-id="023cf-p104">Microsoft ActiveX Data Objects Extensions für Datendefinitionssprache und Sicherheit (ADOX) ist eine Erweiterung der ADO-Objekte und des Programmiermodells. ADOX enthält Objekte zum Erstellen und Ändern von Schemas sowie zur Sicherheit. Da es sich um einen objektbasierten Ansatz zur Schemabearbeitung handelt, können Sie Code erstellen, der für verschiedene Datenquellen verwendet werden kann, ungeachtet der Unterschiede in der jeweiligen Syntax.</span><span class="sxs-lookup"><span data-stu-id="023cf-p104">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model. ADOX includes objects for schema creation and modification as well as security. Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="023cf-p105">ADOX ist eine Begleitbibliothek zu ADO-Kernobjekten. Hiermit werden zusätzliche Objekte für das Erstellen, Ändern und Löschen von Schemaobjekten wie Tabellen und Prozeduren verfügbar gemacht. Außerdem enthält dieses Element Sicherheitsobjekte, um Benutzer und Gruppen zu warten und um Berechtigungen für Objekte zu erteilen und aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="023cf-p105">ADOX is a companion library to the core ADO objects. It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures. It also includes security objects to maintain users and groups, and to grant and revoke permissions on objects.</span></span>

