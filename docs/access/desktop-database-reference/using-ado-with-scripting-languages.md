---
title: Verwenden von ADO mit Skriptsprachen
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2de5cd9507ede3308a207b078a5bc66a4917e267
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475980"
---
# <a name="using-ado-with-scripting-languages"></a>Verwenden von ADO mit Skriptsprachen


**Betrifft**: Access 2013 | Office 2013

In einer Skriptingumgebung können Sie mit ADO Daten mithilfe von serverseitigen Skripts verfügbar machen. In diesem Szenario werden ADO, der von ADO genutzte zugrunde liegende OLE DB-Anbieter und alle anderen Komponenten, die zum Verweisen auf einen bestimmten Datenspeicher verwendet werden, auf einem Server mit Internetinformationsdienste (Internet Information Services, IIS) installiert. ADO ist eine Komponente, auf die in einem Skript, das z. B. HTML erstellen kann, mithilfe von Active Server Pages (ASP) verwiesen wird. Dieser HTML-Inhalt kann über HTTP einem Clientwebbrowser übergeben werden. Mithilfe von Skripting können von der Webseite Aktionen zurück an das serverseitige Skript gesendet werden, sodass Sie bestimmte Daten aktualisieren, traversieren oder anzeigen können.

## <a name="odbc-data-sources"></a>ODBC-Datenquellen

Ein wichtiger Unterschied zwischen ADO-Code mit und ohne Skripting ist die ODBC-Datenquelle, wenn sie verwendet wird. Für Anwendungen ohne Skripting können Sie einen Benutzer-DSN im ODBC-Datenquellenadministrator erstellen. Für unter IIS ausgeführte Skripts müssen Sie einen System-DSN erstellen; andernfalls wird die erstellte Datenquelle von den Skripts nicht erkannt. Dies gilt für alle ADO-Skriptinganwendungen, von denen der Microsoft OLE DB-Anbieter für ODBC über Microsoft IIS verwendet wird.

## <a name="referencing-the-ado-library"></a>Verweisen auf die ADO-Bibliothek

Bei Skriptsprachen nicht verfügbar.

## <a name="handling-events"></a>Behandeln von Ereignissen

Bei Skriptsprachen nicht verfügbar.

Die folgenden Themen enthalten konkretere Informationen zum Verwenden von ADO mit Skriptsprachen:

  - [VBScript-ADO-Programmierung](vbscript-ado-programming.md)

  - [JScript-ADO-Programmierung](jscript-ado-programming.md)

