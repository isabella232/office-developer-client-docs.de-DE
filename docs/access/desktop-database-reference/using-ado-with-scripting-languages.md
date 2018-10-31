---
title: Verwenden von ADO mit Skriptsprachen
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d357fe07a93548419fd03745541435d94d59a8c
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861036"
---
# <a name="using-ado-with-scripting-languages"></a>Verwenden von ADO mit Skriptsprachen


**Betrifft**: Access 2013 | Office 2013

<<<<<<< HEAD innerhalb einer Umgebung mit Skripting, ADO können Sie Daten mithilfe von serverseitigen Skripts verfügbar machen. In diesem Szenario ADO die zugrunde liegende OLE DB-Anbieter, der es verwendet, und andere Komponenten erforderlich, um einen bestimmten Datenspeicher verweisen auf einem Server mit Internetinformationsdienste (Internet Information Services, IIS) installiert sind. ADO ist Active Server Pages (ASP) verwenden, eine Komponente, die in einem Skript die HTML, beispielsweise generieren kann verwiesen wird. Dieser HTML-Inhalt kann über HTTP in einem Clientwebbrowser übergeben werden. Mithilfe von Skripting können die Webseite Aktionen zurück an das serverseitige Skript ermöglicht es Ihnen, aktualisieren, Traversieren oder anzeigen bestimmte Daten senden.
=== Innerhalb einer Umgebung mit Skripting ermöglicht ADO Daten mithilfe von serverseitigen Skripts verfügbar zu machen. In diesem Szenario ADO die zugrunde liegende OLE DB-Anbieter, der es verwendet, und andere Komponenten erforderlich, um einen bestimmten Datenspeicher verweisen auf einem Server mit Internetinformationsdienste (Internet Information Services, IIS) installiert sind. ADO ist Active Server Pages (ASP) verwenden, eine Komponente, die in einem Skript die HTML, beispielsweise generieren kann verwiesen wird. Dieser HTML-Inhalt kann über HTTP in einem Clientwebbrowser übergeben werden. Mithilfe von Skripting kann die Webseite Aktionen zurück an das serverseitige Skript ermöglicht es Ihnen, aktualisieren, Traversieren oder anzeigen bestimmte Daten senden.
>>>>>>> master

## <a name="odbc-data-sources"></a>ODBC-Datenquellen

Ein wichtiger Unterschied zwischen ADO-Code mit und ohne Skripting ist die ODBC-Datenquelle, wenn sie verwendet wird. Für Anwendungen ohne Skripting können Sie einen Benutzer-DSN im ODBC-Datenquellenadministrator erstellen. Für unter IIS ausgeführte Skripts müssen Sie einen System-DSN erstellen; andernfalls wird die erstellte Datenquelle von den Skripts nicht erkannt. Dies gilt für alle ADO-Skriptinganwendungen, von denen der Microsoft OLE DB-Anbieter für ODBC über Microsoft IIS verwendet wird.

## <a name="referencing-the-ado-library"></a>Verweisen auf die ADO-Bibliothek

Bei Skriptsprachen nicht verfügbar.

## <a name="handling-events"></a>Behandeln von Ereignissen

Bei Skriptsprachen nicht verfügbar.

Die folgenden Themen enthalten konkretere Informationen zum Verwenden von ADO mit Skriptsprachen:

- [JScript ADO Programming](jscript-ado-programming.md)

- [VBScript-ADO-Programmierung](vbscript-ado-programming.md)