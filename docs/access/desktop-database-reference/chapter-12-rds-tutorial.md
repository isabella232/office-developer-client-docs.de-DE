---
title: 'Kapitel 12: RDS-Lernprogramm'
TOCTitle: 'Chapter 12: RDS tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 276e8989b674c61414c42428bbff795bf700c6dc
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947679"
---
# <a name="chapter-12-rds-tutorial"></a>Kapitel 12: RDS-Lernprogramm

**Betrifft**: Access 2013, Office 2013

Dieses Lernprogramm zeigt, wie eine Datenquelle mit dem RDS-Programmiermodell abgefragt und aktualisiert wird. Zunächst werden die Schritte beschrieben, die für diese Aufgabe nötig sind. Das Lernprogramm wird dann in Microsoft Visual Basic Scripting Edition und Microsoft Visual J++ mit ADO für Windows Foundation Classes (ADO/WFC) wiederholt.

Aus zwei Gründen enthält dieses Lernprogramm Code in verschiedenen Sprachen:

- Die Dokumentation für RDS setzt voraus, dass der Leser Visual Basic-Code verwendet. Dadurch eignet sich die Dokumentation besonders für Visual Basic-Programmierer, für Programmierer anderer Sprachen ist sie jedoch weniger praktisch.

- Wenn Sie bei einem bestimmten Feature von RDS unsicher sind und gewisse Sprachkenntnisse in einer anderen Sprache haben, finden Sie vielleicht eine Lösung zu Ihrer Frage, indem Sie nach demselben Feature in einer anderen Sprache suchen.

## <a name="how-the-tutorial-is-presented"></a>Wie des Lernprogramms

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

- [Schritt 1: Angeben eines Serverprogramms](step-1-specify-a-server-program-rds-tutorial.md)
- [Schritt 2: Aufrufen des Serverprogramms](step-2-invoke-the-server-program-rds-tutorial.md)
- [Schritt 3: Abrufen ein Recordset-Objekts den Server](step-3-server-obtains-a-recordset-rds-tutorial.md)
- [Schritt 4: Server gibt das Recordset-Objekt zurück.](step-4-server-returns-the-recordset-rds-tutorial.md)
- [Schritt 5: DataControl ist verwendbar vorgenommen.](step-5-datacontrol-is-made-usable-rds-tutorial.md)
- [Schritt 6: Änderungen werden an den Server gesendet.](step-6-changes-are-sent-to-the-server-rds-tutorial.md)
- [RDS-Lernprogramm (VBScript)](rds-tutorial-vbscript.md)
- [RDS-Lernprogramm (Visual J++)](rds-tutorial-visual-j.md)