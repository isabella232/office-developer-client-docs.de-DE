---
title: Visual C++-Erweiterungen für ADO
TOCTitle: Visual C++ Extensions for ADO
ms:assetid: 38048ae0-1dae-9e5e-c569-04011df8b5aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249134(v=office.15)
ms:contentKeyID: 48544212
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fc69d3244cf6faf3aa91fe954e4b39323cf13abf
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720233"
---
# <a name="visual-c-extensions-for-ado"></a>Visual C++-Erweiterungen für ADO


**Betrifft**: Access 2013, Office 2013

Die bevorzugte Methode zum Programmieren von ADO mit Visual C++ wird mithilfe der ** \#importieren** Richtlinie, wie in [Microsoft Visual C++-ADO-Programmierung](visual-c-ado-programming.md)erläutert. Jedoch frühere Versionen von ADO mit einer alternativen Methode der-Programmierung mit Visual C++ geliefert: die Visual C++-Erweiterungen. Dieser Abschnitt beschreibt dieses Feature für diejenigen, die Visual C++-Erweiterungen Code verwalten müssen, aber neuer ADO-Code geschrieben werden soll, mithilfe von \# **Importieren**.

Eine der mühsamsten Aufgaben, der sich Visual C++-Programmierer beim Abrufen von Daten mit ADO gegenübersehen, ist das Konvertieren der als VARIANT-Datentyp zurückgegebenen Daten in einen C++-Datentyp und das anschließende Speichern der konvertierten Daten in einer Klasse oder Struktur. Das Abrufen von C++-Daten über einen VARIANT-Datentyp ist nicht nur aufwändig, sondern es verringert auch die Leistung.

In ADO wird eine Schnittstelle bereitgestellt, die das Abrufen von Daten in systemeigene C/C++-Datentypen ohne Verwendung eines VARIANT-Datentyps unterstützt und außerdem Präprozessormakros bereitstellt, durch die die Verwendung der Schnittstelle vereinfacht wird. Das Ergebnis ist ein flexibles Tool, das einfacher zu verwenden ist und über eine gute Leistung verfügt.

Ein gängiges C/C++-Clientszenario ist das Binden eines Datensatzes in einem [Recordset](recordset-object-ado.md) an eine C/C++-Struktur oder -Klasse, die systemeigene C/C++-Typen enthält. Bei Verwendung von VARIANTs gehört hierzu das Schreiben von Code für die Konvertierung von VARIANT-Typen in systemeigene C/C++-Typen. Die Visual C++-Erweiterungen für ADO sollen dieses Szenario für Visual C++-Programmierer deutlich vereinfachen.

Unter den folgenden Themen finden Sie weitere Informationen zu den Visual C++-Erweiterungen für ADO.

  - [Verwenden von Visual C++-Erweiterungen](using-visual-c-extensions.md)

  - [Visual C++-Erweiterungsheader](visual-c-extensions-header.md)

  - [Visual C++-Erweiterungen (Beispiel)](visual-c-extensions-example.md)

