---
title: Verwenden von ADO mit Skriptsprachen
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ae1812a3d141f9466d1ff4d332cb09f557dfd53b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580622"
---
# <a name="using-ado-with-scripting-languages"></a>Verwenden von ADO mit Skriptsprachen


**Gilt für**: Access 2013, Office 2013

In einer Skriptingumgebung können Sie mit ADO Daten mithilfe von serverseitigen Skripts verfügbar machen. In diesem Szenario werden ADO, der von ADO genutzte zugrunde liegende OLE DB-Anbieter und alle anderen Komponenten, die zum Verweisen auf einen bestimmten Datenspeicher verwendet werden, auf einem Server mit Internetinformationsdienste (Internet Information Services, IIS) installiert. ADO ist eine Komponente, auf die in einem Skript, das z. B. HTML erstellen kann, mithilfe von Active Server Pages (ASP) verwiesen wird. Dieser HTML-Inhalt kann über HTTP an einen Clientwebbrowser übergeben werden. Durch die Verwendung von Skripting kann die Webseite Aktionen zurück an das serverseitige Skript senden, sodass Sie bestimmte Daten aktualisieren, durchlaufen oder anzeigen können.

## <a name="odbc-data-sources"></a>ODBC-Datenquellen

Ein wichtiger Unterschied zwischen ADO-Code mit und ohne Skripting ist die ODBC-Datenquelle, wenn sie verwendet wird. Für Anwendungen ohne Skripting können Sie einen Benutzer-DSN im ODBC-Datenquellenadministrator erstellen. Für unter IIS ausgeführte Skripts müssen Sie einen System-DSN erstellen; andernfalls wird die erstellte Datenquelle von den Skripts nicht erkannt. Dies gilt für alle ADO-Skriptinganwendungen, von denen der Microsoft OLE DB-Anbieter für ODBC über Microsoft IIS verwendet wird.

## <a name="referencing-the-ado-library"></a>Verweisen auf die ADO-Bibliothek

Bei Skriptsprachen nicht verfügbar.

## <a name="handling-events"></a>Behandeln von Ereignissen

Bei Skriptsprachen nicht verfügbar.

Die folgenden Themen enthalten konkretere Informationen zum Verwenden von ADO mit Skriptsprachen:

- [JScript-ADO-Programmierung](jscript-ado-programming.md)

- [VBScript-ADO-Programmierung](vbscript-ado-programming.md)
