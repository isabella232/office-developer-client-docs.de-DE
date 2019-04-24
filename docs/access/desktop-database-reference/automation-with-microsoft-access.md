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
localization_priority: Priority
ms.openlocfilehash: 9635cdb2a06f610f42e4aa9fc9f998719aebb986
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296962"
---
# <a name="automation-with-microsoft-access"></a>Automatisierung mit Microsoft Access

**Gilt für**: Access 2013, Office 2013

Microsoft Access ist eine COM-Komponente, die Automatisierung, früher OLE-Automatisierung genannt, unterstützt. Microsoft Access unterstützt die Automatisierung in zweierlei Hinsicht: in Microsoft Access können Sie mit Objekten arbeiten, die von einer anderen Komponente bereitgestellt werden, und umgekehrt stellt Microsoft Access auch seine Objekte anderen COM-Komponenten zur Verfügung.

Sie können das Schlüsselwort **New** oder die **CreateObject** -Methode verwenden, um eine neue Instanz einer Komponente zu erstellen. Mit der **GetObject** -Methode können Sie einer vorhandenen Instanz einer Komponente eine Variable zuweisen.

In Microsoft Access können Sie einen Verweis auf die Typbibliothek einer Komponente einrichten, um die Leistung zu steigern, wenn Sie mit dieser Anwendung über Automatisierung arbeiten. Microsoft Access enthält auch den Objektkatalog, ein Tool, mit dem Sie Objekte und ihre Methoden und Eigenschaften in Typbibliotheken anderer Anwendungen anzeigen können.

Die Typbibliothek von Microsoft Access stellt Informationen zu Microsoft Access-Objekten für andere Komponenten zur Verfügung. Sie können in einer Komponente [einen Verweis auf die Microsoft Access-Typbibliothek einstellen](https://docs.microsoft.com/office/vba/access/Concepts/Settings/set-references-to-type-libraries) und deren Objekte im Objektkatalog anzeigen.

Wenn Sie Microsoft Access-Objekte über die Automatisierung bearbeiten möchten, erstellen Sie eine Instanz des Microsoft Access-Objekts **[Application](https://docs.microsoft.com/office/vba/api/Access.Application)**. Angenommen, Sie möchten Daten von Microsoft Excel in einem Microsoft Access-Formular oder -Bericht anzeigen. Um Microsoft Access von Microsoft Excel aus starten zu können, erstellen Sie zuerst mit dem Schlüsselwort **New** eine Instanz des Microsoft Access-Objekts **Application**. Sie können auch die **CreateObject** -Methode verwenden, um eine neue Instanz des Microsoft Access-Objekts **Application** zu erstellen, oder Sie können mit der **GetObject** -Methode eine Objektvariable als Zeiger auf eine bestehende Instanz von Microsoft Access definieren. Überprüfen Sie die Dokumentation der Komponente, um zu ermitteln, welche Syntax sie unterstützt.

Nachdem Sie eine Instanz von Microsoft Access gestartet haben und wenn Sie Microsoft Access-Objekte steuern möchten, öffnen Sie zuerst eine Datenbank oder ein Projekt (ADP) im Microsoft Access-Fenster. Hierzu verwenden Sie die **[OpenCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.OpenCurrentDatabase)** - oder die **[NewCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.NewCurrentDatabase)** -Methode für eine Datenbank bzw. die **[OpenAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.OpenAccessProject)** - oder die **[NewAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.NewAccessProject)** -Methode für ein Projekt.

Haben Sie Microsoft Access nur geöffnet, um die von Microsoft Access-DAO bereitgestellten Datenzugriffsobjekte zu verwenden, brauchen Sie im Microsoft Access-Fenster keine Datenbank zu öffnen. Sie können die **[DBEngine](https://docs.microsoft.com/office/vba/api/Access.Application.DBEngine)** -Eigenschaft des Microsoft Access-Objekts **Application** verwenden, um während einer Automatisierungsoperation auf Objekte in der Objektbibliothek des Microsoft Office 12.0 Access-Datenbankmoduls zuzugreifen.

