---
title: 'Kapitel 14: Grundlegendes zu ADO MD'
TOCTitle: 'Chapter 14: ADO MD fundamentals'
ms:assetid: 129baa54-0bc1-985d-4bfd-25a1c1c3018e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248899(v=office.15)
ms:contentKeyID: 48543346
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1a3b816c44b6b3b5e50a8ed492e1ca6240c920b4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627100"
---
# <a name="chapter-14-ado-md-fundamentals"></a>Kapitel 14: Grundlegendes zu ADO MD

**Gilt für**: Access 2013, Office 2013

Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) bietet einfachen Zugriff auf multidimensionale Daten in Sprachen wie Microsoft Visual Basic, Microsoft Visual C++ und Microsoft Visual J++. Mit ADO MD werden Microsoft ActiveX Data Objects (ADO) erweitert, um Objekte für multidimensionalspezifische Daten wie [CubeDef](cubedef-object-ado-md.md)- und [Cellset](cellset-object-ado-md.md)-Objekte einzuschließen. Mit ADO MD können Sie ein multidimensionales Schema durchsuchen, einen Cube abfragen und die Ergebnisse abrufen.

ADO MD verwendet wie ADO einen zugrunde liegenden OLE DB-Anbieter für den Zugriff auf Daten. Der Anbieter muss gemäß der OLE DB für OLAP-Spezifikation ein multidimensionaler Datenprovider (MDP) sein, um mit ADO MD arbeiten zu können. MDPs stellen Daten in multidimensionalen Ansichten dar. Tabulare Datenprovider (TDP) stellen Daten dagegen in tabularen Ansichten dar. In der Dokumentation zu Ihrem OLE DB für OLAP-Anbieter finden Sie ausführlichere Information zur Syntax und zu den Funktionen, die von Ihrem Anbieter unterstützt werden.

Dieses Dokument setzt Erfahrung in der Verwendung der Programmiersprache Visual Basic und grundlegende ADO- und OLAP-Kenntnisse voraus. Weitere Informationen finden Sie im [ADO-Programmierhandbuch](ado-programmer-s-guide.md) und in der OLE DB für OLAP-Programmierreferenz. 

In diesem Kapitel werden die folgenden Themen behandelt:

- [Übersicht über multidimensionale Schemas und Daten](overview-of-multidimensional-schemas-and-data.md)
- [Arbeiten mit mehrdimensionalen Daten](working-with-multidimensional-data.md)
- [Verwenden von ADO mit ADO MD ](using-ado-with-ado-md.md)
- [Programmieren mit ADO MD ](programming-with-ado-md.md)
