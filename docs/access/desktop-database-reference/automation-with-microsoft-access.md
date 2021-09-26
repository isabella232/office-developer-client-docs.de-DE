---
title: Automatisierung mit Microsoft Access
TOCTitle: Automation with Microsoft Access
description: Microsoft Access ist eine COM-Komponente, die Automatisierung, bisher OLE-Automatisierung genannt, unterstützt.
ms:assetid: 39fde349-3ba3-7c7a-3c92-316641dc8712
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192643(v=office.15)
ms:contentKeyID: 48544258
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13783
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 526887b6d63623174f0bcdffd43d87a17270a1b4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558842"
---
# <a name="automation-with-microsoft-access"></a>Automatisierung mit Microsoft Access

**Gilt für**: Access 2013, Office 2013

Microsoft Access ist eine COM-Komponente, die Automatisierung, früher OLE-Automatisierung genannt, unterstützt. Microsoft Access unterstützt die Automatisierung in zweierlei Hinsicht: in Microsoft Access können Sie mit Objekten arbeiten, die von einer anderen Komponente bereitgestellt werden, und umgekehrt stellt Microsoft Access auch seine Objekte anderen COM-Komponenten zur Verfügung.

Sie können das Schlüsselwort **New** oder die **CreateObject** -Methode verwenden, um eine neue Instanz einer Komponente zu erstellen. Mit der **GetObject** -Methode können Sie einer vorhandenen Instanz einer Komponente eine Variable zuweisen.

In Microsoft Access können Sie einen Verweis auf die Typbibliothek einer Komponente einrichten, um die Leistung zu steigern, wenn Sie mit dieser Anwendung über Automatisierung arbeiten. Microsoft Access enthält auch den Objektkatalog, ein Tool, mit dem Sie Objekte und ihre Methoden und Eigenschaften in Typbibliotheken anderer Anwendungen anzeigen können.

Die Microsoft Access-Typbibliothek stellt für andere Komponenten Informationen über Microsoft Access-Objekte bereit. Sie können in einer Komponente [einen Verweis](https://docs.microsoft.com/office/vba/access/Concepts/Settings/set-references-to-type-libraries) auf die Microsoft Access-Typbibliothek festlegen und deren Objekte im Objektkatalog anzeigen.

Wenn Sie Microsoft Access-Objekte über die Automatisierung bearbeiten möchten, erstellen Sie eine Instanz des Microsoft Access-Objekts **[Application](https://docs.microsoft.com/office/vba/api/Access.Application)**. Angenommen, Sie möchten Daten von Microsoft Excel in einem Microsoft Access-Formular oder -Bericht anzeigen. Um Microsoft Access von Microsoft Excel aus starten zu können, erstellen Sie zuerst mit dem Schlüsselwort **New** eine Instanz des Microsoft Access-Objekts **Application**. Sie können auch die **CreateObject** -Methode verwenden, um eine neue Instanz des Microsoft Access-Objekts **Application** zu erstellen, oder Sie können mit der **GetObject** -Methode eine Objektvariable als Zeiger auf eine bestehende Instanz von Microsoft Access definieren. Überprüfen Sie die Dokumentation der Komponente, um zu ermitteln, welche Syntax sie unterstützt.

Nachdem Sie eine Instanz von Microsoft Access gestartet haben und wenn Sie Microsoft Access-Objekte steuern möchten, öffnen Sie zuerst eine Datenbank oder ein Projekt (ADP) im Microsoft Access-Fenster. Hierzu verwenden Sie die **[OpenCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.OpenCurrentDatabase)** - oder die **[NewCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.NewCurrentDatabase)** -Methode für eine Datenbank bzw. die **[OpenAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.OpenAccessProject)** - oder die **[NewAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.NewAccessProject)** -Methode für ein Projekt.

Haben Sie Microsoft Access nur geöffnet, um die von Microsoft Access-DAO bereitgestellten Datenzugriffsobjekte zu verwenden, brauchen Sie im Microsoft Access-Fenster keine Datenbank zu öffnen. Sie können die **[DBEngine](https://docs.microsoft.com/office/vba/api/Access.Application.DBEngine)** -Eigenschaft des Microsoft Access-Objekts **Application** verwenden, um während einer Automatisierungsoperation auf Objekte in der Objektbibliothek des Microsoft Office 12.0 Access-Datenbankmoduls zuzugreifen.

