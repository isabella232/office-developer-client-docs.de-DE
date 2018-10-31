---
title: 'Kapitel 12: RDS-Lernprogramm'
TOCTitle: 'Chapter 12: RDS Tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aec7c9a89ea078bfad9b05d664d373831491edc4
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860224"
---
# <a name="chapter-12-rds-tutorial"></a>Kapitel 12: RDS-Lernprogramm


**Betrifft**: Access 2013 | Office 2013

Dieses Lernprogramm zeigt, wie eine Datenquelle mit dem RDS-Programmiermodell abgefragt und aktualisiert wird. Zunächst werden die Schritte beschrieben, die für diese Aufgabe nötig sind. Das Lernprogramm wird dann in Microsoft® Visual Basic Scripting Edition und Microsoft® Visual J++® wiederholt, wobei ADO for Windows Foundation Classes (ADO/WFC) enthalten ist.

Aus zwei Gründen enthält dieses Lernprogramm Code in verschiedenen Sprachen:

  - Die Dokumentation für RDS setzt voraus, dass der Leser Visual Basic-Code verwendet. Dadurch eignet sich die Dokumentation besonders für Visual Basic-Programmierer, für Programmierer anderer Sprachen ist sie jedoch weniger praktisch.

  - Wenn Sie bei einem bestimmten Feature von RDS unsicher sind und gewisse Sprachkenntnisse in einer anderen Sprache haben, finden Sie vielleicht eine Lösung zu Ihrer Frage, indem Sie nach demselben Feature in einer anderen Sprache suchen.

## <a name="how-the-tutorial-is-presented"></a>Aufbau des Lernprogramms

Dieses Lernprogramm basiert auf dem RDS-Programmiermodell. Die jeweiligen Schritte des Programmiermodells werden dabei einzeln vorgestellt. Darüber hinaus wird jeder Schritt durch einen Ausschnitt eines Visual Basic-Codes veranschaulicht.

Das Codebeispiel wird ohne ausführliche Erläuterungen in weiteren Sprachen wiederholt. Jeder Schritt in einem Lernprogramm einer bestimmten Sprache ist mit dem entsprechenden Schritt im Programmiermodell und dem erläuternden Lernprogramm gekennzeichnet. Anhand der Schrittnummer finden Sie die Erläuterungen im Lernprogramm.

Das RDS-Programmiermodell wird unten aufgeführt. Verwenden Sie es als Leitfaden, wenn Sie das Lernprogramm durchgehen.

## <a name="rds-programming-model-with-objects"></a>RDS-Programmiermodell mit Objekten

  - Geben Sie das auf dem Server aufzurufende Programm an, und ermitteln Sie eine Möglichkeit (Proxy), vom Client darauf zu verweisen.

  - Aufrufen des Serverprogramms. Übergeben von Parametern an das Serverprogramm, die die Datenquelle und den auszugebenden Befehl identifizieren.

  - Das Serverprogramm ruft ein [Recordset](recordset-object-ado.md)-Objekt aus der Datenquelle ab, in der Regel unter Verwendung von ADO. Das **Recordset** -Objekt kann optional auf dem Server verarbeitet werden.

  - Das Serverprogramm gibt das endgültige **Recordset** -Objekt an die Clientanwendung zurück.

  - Auf dem Client wird das **Recordset** -Objekt optional in eine Form gebracht, die leicht von visuellen Steuerelementen verwendet werden kann.

  - Änderungen am **Recordset** -Objekt werden zurück an den Server gesendet und zur Aktualisierung der Datenquelle verwendet.

Dies sind die Schritte in diesem Lernprogramm:

- [Step 1: Specify a Server Program (RDS Tutorial)](step-1-specify-a-server-program-rds-tutorial.md)

- [Step 2: Invoke the Server Program (RDS Tutorial)](step-2-invoke-the-server-program-rds-tutorial.md)

- [Step 3: Server Obtains a Recordset (RDS Tutorial)](step-3-server-obtains-a-recordset-rds-tutorial.md)

- [Step 4: Server Returns the Recordset (RDS Tutorial)](step-4-server-returns-the-recordset-rds-tutorial.md)

- [Step 5: DataControl is Made Usable (RDS Tutorial)](step-5-datacontrol-is-made-usable-rds-tutorial.md)

- [Step 6: Changes are Sent to the Server (RDS Tutorial)](step-6-changes-are-sent-to-the-server-rds-tutorial.md)

- [RDS Tutorial (VBScript)](rds-tutorial-vbscript.md)

- [RDS-Lernprogramm (Visual J++)](rds-tutorial-visual-j.md)