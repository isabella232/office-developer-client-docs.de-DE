---
title: 'Kapitel 14: Grundlegendes zu ADO MD'
TOCTitle: 'Chapter 14: ADO MD Fundamentals'
ms:assetid: 129baa54-0bc1-985d-4bfd-25a1c1c3018e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248899(v=office.15)
ms:contentKeyID: 48543346
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8576d2a1d579de306b438f7b0fb04a1eb2d46cc
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863646"
---
# <a name="chapter-14-ado-md-fundamentals"></a><span data-ttu-id="af367-102">Kapitel 14: Grundlegendes zu ADO MD</span><span class="sxs-lookup"><span data-stu-id="af367-102">Chapter 14: ADO MD Fundamentals</span></span>


<span data-ttu-id="af367-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="af367-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="af367-p101">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) bietet einfachen Zugriff auf multidimensionale Daten in Sprachen wie Microsoft Visual Basic, Microsoft Visual C++ und Microsoft Visual J++. Mit ADO MD werden Microsoft ActiveX Data Objects (ADO) erweitert, um Objekte für multidimensionalspezifische Daten wie [CubeDef](cubedef-object-ado-md.md)- und [Cellset](cellset-object-ado-md.md)-Objekte einzuschließen. Mit ADO MD können Sie ein multidimensionales Schema durchsuchen, einen Cube abfragen und die Ergebnisse abrufen.</span><span class="sxs-lookup"><span data-stu-id="af367-p101">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++. ADO MD extends Microsoft ActiveX Data Objects (ADO) to include objects specific to multidimensional data, such as the [CubeDef](cubedef-object-ado-md.md) and [Cellset](cellset-object-ado-md.md) objects. With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="af367-p102">ADO MD verwendet wie ADO einen zugrunde liegenden OLE DB-Anbieter für den Zugriff auf Daten. Der Anbieter muss gemäß der OLE DB für OLAP-Spezifikation ein multidimensionaler Datenanbieter (Datenprovider, MDP) sein, um mit ADO MD arbeiten zu können. MDPs stellen Daten in multidimensionalen Ansichten dar. Tabellenorientierte Datenanbieter (Datenprovider, TDP) stellen Daten dagegen in Tabellenansichten dar. In der Dokumentation zu Ihrem OLE DB für OLAP-Anbieter finden Sie ausführlichere Information zur Syntax und zu den Funktionen, die von Ihrem Anbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="af367-p102">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data. To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification. MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views. Refer to the documentation for your OLAP OLE DB provider for more detailed information on the specific syntax and behaviors supported by your provider.</span></span>

<span data-ttu-id="af367-111">Dieses Dokument setzt Erfahrung in der Verwendung der Programmiersprache Visual Basic und grundlegende ADO- und OLAP-Kenntnisse voraus.</span><span class="sxs-lookup"><span data-stu-id="af367-111">This document assumes a working knowledge of the Visual Basic programming language and a general knowledge of ADO and OLAP.</span></span> <span data-ttu-id="af367-112">Weitere Informationen zu ADO finden Sie im [ADO-Programmierhandbuch](ado-programmer-s-guide.md) und der OLE DB für OLAP-Programmierreferenz.</span><span class="sxs-lookup"><span data-stu-id="af367-112">For more information, see the [ADO Programmer's Guide](ado-programmer-s-guide.md) and the OLE DB for OLAP Programmer's Reference.</span></span> 

<span data-ttu-id="af367-113">In diesem Kapitel werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="af367-113">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="af367-114">Übersicht über Multidimensionale Schemas und Daten</span><span class="sxs-lookup"><span data-stu-id="af367-114">Overview of Multidimensional Schemas and Data</span></span>](overview-of-multidimensional-schemas-and-data.md)

- [<span data-ttu-id="af367-115">Verwenden von multidimensionalen Daten </span><span class="sxs-lookup"><span data-stu-id="af367-115">Working with Multidimensional Data</span></span>](working-with-multidimensional-data.md)

- [<span data-ttu-id="af367-116">Verwenden von ADO mit ADO MD </span><span class="sxs-lookup"><span data-stu-id="af367-116">Using ADO with ADO MD</span></span>](using-ado-with-ado-md.md)

- [<span data-ttu-id="af367-117">Programmieren mit ADO MD </span><span class="sxs-lookup"><span data-stu-id="af367-117">Programming with ADO MD</span></span>](programming-with-ado-md.md)
