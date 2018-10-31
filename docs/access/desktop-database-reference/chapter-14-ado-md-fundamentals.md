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
# <a name="chapter-14-ado-md-fundamentals"></a>Kapitel 14: Grundlegendes zu ADO MD


**Betrifft**: Access 2013 | Office 2013

Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) bietet einfachen Zugriff auf multidimensionale Daten in Sprachen wie Microsoft Visual Basic, Microsoft Visual C++ und Microsoft Visual J++. Mit ADO MD werden Microsoft ActiveX Data Objects (ADO) erweitert, um Objekte für multidimensionalspezifische Daten wie [CubeDef](cubedef-object-ado-md.md)- und [Cellset](cellset-object-ado-md.md)-Objekte einzuschließen. Mit ADO MD können Sie ein multidimensionales Schema durchsuchen, einen Cube abfragen und die Ergebnisse abrufen.

ADO MD verwendet wie ADO einen zugrunde liegenden OLE DB-Anbieter für den Zugriff auf Daten. Der Anbieter muss gemäß der OLE DB für OLAP-Spezifikation ein multidimensionaler Datenanbieter (Datenprovider, MDP) sein, um mit ADO MD arbeiten zu können. MDPs stellen Daten in multidimensionalen Ansichten dar. Tabellenorientierte Datenanbieter (Datenprovider, TDP) stellen Daten dagegen in Tabellenansichten dar. In der Dokumentation zu Ihrem OLE DB für OLAP-Anbieter finden Sie ausführlichere Information zur Syntax und zu den Funktionen, die von Ihrem Anbieter unterstützt werden.

Dieses Dokument setzt Erfahrung in der Verwendung der Programmiersprache Visual Basic und grundlegende ADO- und OLAP-Kenntnisse voraus. Weitere Informationen zu ADO finden Sie im [ADO-Programmierhandbuch](ado-programmer-s-guide.md) und der OLE DB für OLAP-Programmierreferenz. 

In diesem Kapitel werden die folgenden Themen behandelt:

- [Übersicht über Multidimensionale Schemas und Daten](overview-of-multidimensional-schemas-and-data.md)

- [Verwenden von multidimensionalen Daten ](working-with-multidimensional-data.md)

- [Verwenden von ADO mit ADO MD ](using-ado-with-ado-md.md)

- [Programmieren mit ADO MD ](programming-with-ado-md.md)
