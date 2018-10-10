---
title: 'Kapitel 9: Datenstrukturierung'
TOCTitle: 'Chapter 9: Data Shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8217be1004ea8304501e7d32908b8af269873b7a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475168"
---
# <a name="chapter-9-data-shaping"></a>Kapitel 9: Datenstrukturierung


**Betrifft**: Access 2013 | Office 2013

*Data shaping* bietet eine Möglichkeit zum Abfragen einer Datenquelle und Zurückgeben einer [Recordset-Objekt](recordset-object-ado.md) , das eine hierarchische Beziehung zwischen zwei oder mehr logische Entitäten (einer Hierarchie) darstellt. Ein klassisches Beispiel für eine hierarchische Beziehung sind Kunden und Aufträge. Für jeden Kunden in einer Datenbank können null oder mehr Aufträge vorhanden sein. Mit regulären SQL-Befehlen könnten die Daten mithilfe der JOIN-Syntax abgerufen werden, was jedoch ineffizient und unhandlich sein kann, da in jedem für eine bestimmte Übergeordnet-Untergeordnet-Beziehung zurückgegebenen Datensatz redundante Daten zum übergeordneten Element wiederholt werden. Durch Datenstrukturierung kann ein einzelner übergeordneter Datensatz im übergeordneten **Recordset** in Beziehung zu mehreren untergeordneten Datensätzen im **Recordset** gesetzt werden, wodurch die Redundanz von JOIN vermieden wird. Die meisten Personen finden das Programmiermodell mit Übergeordnet-Untergeordnet-Beziehungen und mehreren **Recordsets** natürlicher und meinen, dass sie mit ihm einfacher arbeiten als mit dem JOIN-Modell und einem einzelnen **Recordset**.

Die Datenstrukturierungssyntax stellt außerdem weitere Funktionen bereit. Entwickler können neue **Recordset** -Objekte ohne zugrunde liegende Datenquelle erstellen, indem sie das NEW-Schlüsselwort verwenden, um die Felder der über- und untergeordneten **Recordsets** zu beschreiben. Das neue **Recordset** -Objekt kann mit Daten aufgefüllt und permanent gespeichert werden. Entwickler können außerdem verschiedene Berechnungen oder Aggregationen (z. B. SUM, AVG und MAX) für untergeordnete Felder ausführen. Mit Datenstrukturierung kann auch ein übergeordnetes **Recordset** aus einem untergeordneten **Recordset** erstellt werden, indem Datensätze im untergeordneten Element gruppiert werden und im übergeordneten Element für jede Gruppe im untergeordneten Element eine Zeile platziert wird.

Weitere Informationen zur Datenstrukturierung finden Sie unter den folgenden Themen:

  - [Datenstrukturierung (Zusammenfassung)](data-shaping-summary.md)

  - [Erforderliche Anbieter für die Datenstrukturierung](required-providers-for-data-shaping.md)

  - [Shape-Befehle im Allgemeinen](shape-commands-in-general.md)

  - [APPEND-Klausel für Formen](shape-append-clause.md)

  - [COMPUTE-Klausel für Formen](shape-compute-clause.md)

  - [Erstellen hierarchischer Recordsets](fabricating-hierarchical-recordsets.md)

  - [Zugreifen auf Zeilen in einem hierarchischen Recordset](accessing-rows-in-a-hierarchical-recordset.md)

  - [Formale Grammatik für Formen](formal-shape-grammar.md)

  - [Visual Basic für Applikationen (Funktionen)](visual-basic-for-applications-functions.md)

