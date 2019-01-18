---
title: 'Kapitel 14: Grundlegendes zu ADO MD'
TOCTitle: 'Chapter 14: ADO MD fundamentals'
ms:assetid: 129baa54-0bc1-985d-4bfd-25a1c1c3018e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248899(v=office.15)
ms:contentKeyID: 48543346
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 44a4e666fb615f7d3870acfbd986e93971606d5b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701137"
---
# <a name="chapter-14-ado-md-fundamentals"></a><span data-ttu-id="2092f-102">Kapitel 14: Grundlegendes zu ADO MD</span><span class="sxs-lookup"><span data-stu-id="2092f-102">Chapter 14: ADO MD fundamentals</span></span>

<span data-ttu-id="2092f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2092f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2092f-p101">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) bietet einfachen Zugriff auf multidimensionale Daten in Sprachen wie Microsoft Visual Basic, Microsoft Visual C++ und Microsoft Visual J++. Mit ADO MD werden Microsoft ActiveX Data Objects (ADO) erweitert, um Objekte für multidimensionalspezifische Daten wie [CubeDef](cubedef-object-ado-md.md)- und [Cellset](cellset-object-ado-md.md)-Objekte einzuschließen. Mit ADO MD können Sie ein multidimensionales Schema durchsuchen, einen Cube abfragen und die Ergebnisse abrufen.</span><span class="sxs-lookup"><span data-stu-id="2092f-p101">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++. ADO MD extends Microsoft ActiveX Data Objects (ADO) to include objects specific to multidimensional data, such as the [CubeDef](cubedef-object-ado-md.md) and [Cellset](cellset-object-ado-md.md) objects. With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="2092f-p102">ADO MD verwendet wie ADO einen zugrunde liegenden OLE DB-Anbieter für den Zugriff auf Daten. Der Anbieter muss gemäß der OLE DB für OLAP-Spezifikation ein multidimensionaler Datenanbieter (Datenprovider, MDP) sein, um mit ADO MD arbeiten zu können. MDPs stellen Daten in multidimensionalen Ansichten dar. Tabellenorientierte Datenanbieter (Datenprovider, TDP) stellen Daten dagegen in Tabellenansichten dar. In der Dokumentation zu Ihrem OLE DB für OLAP-Anbieter finden Sie ausführlichere Information zur Syntax und zu den Funktionen, die von Ihrem Anbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2092f-p102">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data. To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification. MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views. Refer to the documentation for your OLAP OLE DB provider for more detailed information on the specific syntax and behaviors supported by your provider.</span></span>

<span data-ttu-id="2092f-111">Dieses Dokument setzt Erfahrung in der Verwendung der Programmiersprache Visual Basic und grundlegende ADO- und OLAP-Kenntnisse voraus.</span><span class="sxs-lookup"><span data-stu-id="2092f-111">This document assumes a working knowledge of the Visual Basic programming language and a general knowledge of ADO and OLAP.</span></span> <span data-ttu-id="2092f-112">Weitere Informationen finden Sie unter der [ADO-Programmierhandbuch](ado-programmer-s-guide.md) und der OLE DB für OLAP-Programmierreferenz.</span><span class="sxs-lookup"><span data-stu-id="2092f-112">For more information, see the [ADO programmer's guide](ado-programmer-s-guide.md) and the OLE DB for OLAP Programmer's Reference.</span></span> 

<span data-ttu-id="2092f-113">In diesem Kapitel werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="2092f-113">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="2092f-114">Übersicht über multidimensionale Schemas und Daten</span><span class="sxs-lookup"><span data-stu-id="2092f-114">Overview of multidimensional schemas and data</span></span>](overview-of-multidimensional-schemas-and-data.md)
- [<span data-ttu-id="2092f-115">Verwenden von multidimensionalen Daten</span><span class="sxs-lookup"><span data-stu-id="2092f-115">Working with multidimensional data</span></span>](working-with-multidimensional-data.md)
- [<span data-ttu-id="2092f-116">Verwenden von ADO mit ADO MD </span><span class="sxs-lookup"><span data-stu-id="2092f-116">Using ADO with ADO MD</span></span>](using-ado-with-ado-md.md)
- [<span data-ttu-id="2092f-117">Programmieren mit ADO MD </span><span class="sxs-lookup"><span data-stu-id="2092f-117">Programming with ADO MD</span></span>](programming-with-ado-md.md)
