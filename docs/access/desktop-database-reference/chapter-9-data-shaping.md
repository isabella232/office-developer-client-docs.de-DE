---
title: 'Kapitel 9: Daten modellieren'
TOCTitle: 'Chapter 9: Data shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43ad9d5e989bc1c6f4a54fb4882cfe3c3e357fd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296423"
---
# <a name="chapter-9-data-shaping"></a>Kapitel 9: Daten modellieren

**Gilt für**: Access 2013, Office 2013

Die *Datenstrukturierung* stellt eine Möglichkeit zum Abfragen einer Datenquelle und Zurückgeben eines [Recordsets](recordset-object-ado.md) bereit, das eine Übergeordnet-Untergeordnet-Beziehung zwischen zwei oder mehr logischen Entitäten (eine Hierarchie) darstellt. 

Ein klassisches Beispiel für eine hierarchische Beziehung sind Kunden und Aufträge. Für jeden Kunden in einer Datenbank können null oder mehr Aufträge vorhanden sein. Mit regulären SQL-Befehlen könnten die Daten mithilfe der JOIN-Syntax abgerufen werden, was jedoch ineffizient und unhandlich sein kann, da in jedem für eine bestimmte Übergeordnet-Untergeordnet-Beziehung zurückgegebenen Datensatz redundante Daten zum übergeordneten Element wiederholt werden. Durch Datenstrukturierung kann ein einzelner übergeordneter Datensatz im übergeordneten **Recordset** in Beziehung zu mehreren untergeordneten Datensätzen im **Recordset** gesetzt werden, wodurch die Redundanz von JOIN vermieden wird. Die meisten Personen finden das Programmiermodell mit Übergeordnet-Untergeordnet-Beziehungen und mehreren **Recordsets** natürlicher und meinen, dass sie mit ihm einfacher arbeiten als mit dem JOIN-Modell und einem einzelnen **Recordset**.

Die Datenstrukturierungssyntax stellt außerdem weitere Funktionen bereit. Entwickler können neue **Recordset** -Objekte ohne zugrunde liegende Datenquelle erstellen, indem sie das NEW-Schlüsselwort verwenden, um die Felder der über- und untergeordneten **Recordsets** zu beschreiben. Das neue **Recordset** -Objekt kann mit Daten aufgefüllt und permanent gespeichert werden. Entwickler können außerdem verschiedene Berechnungen oder Aggregationen (z. B. SUM, AVG und MAX) für untergeordnete Felder ausführen. Mit Datenstrukturierung kann auch ein übergeordnetes **Recordset** aus einem untergeordneten **Recordset** erstellt werden, indem Datensätze im untergeordneten Element gruppiert werden und im übergeordneten Element für jede Gruppe im untergeordneten Element eine Zeile platziert wird.

Weitere Informationen zur Datenstrukturierung finden Sie unter den folgenden Themen:

- [Erforderliche Anbieter für Datenmodellierung](required-providers-for-data-shaping.md)
- [Shape Compute-Klausel](shape-compute-clause.md)
- [Fabrizieren hierarchischer Recordsets](fabricating-hierarchical-recordsets.md)
- [Zugreifen auf Zeilen in einem hierarchischen Recordset](accessing-rows-in-a-hierarchical-recordset.md)
- [Formal Shape Grammar](formal-shape-grammar.md)
- [Funktionen (Visual Basic for Applications)](visual-basic-for-applications-functions.md)
- [Shape APPEND-Klausel (ADO)](shape-append-clause.md)
- [Datenstrukturierung (ADO)](data-shaping.md)
- [Shape-Befehle im allgemeinen (ADO)](shape-commands-in-general.md)

