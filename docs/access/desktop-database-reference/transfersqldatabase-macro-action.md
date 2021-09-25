---
title: TransferSQLDatenbank-Makroaktion
TOCTitle: TransferSQLDatabase macro action
ms:assetid: 8cb95e22-f1f0-6c70-7dcb-3a3e9aafdc57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197344(v=office.15)
ms:contentKeyID: 48546244
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm111536
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 645dc3b4f098be2cd3f758c216c5606dff3ba9b9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593432"
---
# <a name="transfersqldatabase-macro-action"></a>TransferSQLDatenbank-Makroaktion

**Gilt für**: Access 2013, Office 2013

Verwenden Sie in einem Access-Projekt die **TransferSQLDatenbank** -Aktion, um eine Microsoft SQL Server-Datenbank der Version 7.0 oder höher zu übertragen. Weitere Informationen zum Übertragen einer Datenbank finden Sie in der SQL Server Dokumentation.

> [!NOTE]
> Diese Aktion ist nicht zulässig, wenn die Datenbank nicht vertrauenswürdig ist.

## <a name="setting"></a>Einstellung

Die **TransferSQLDatenbank**-Aktion hat die folgenden Argumente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Aktionsargument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Server</strong></p></td>
<td><p>Der Name des Datenbankservers mit SQL Server 7.0 oder höher, auf den Sie Daten kopieren.</p></td>
</tr>
<tr class="even">
<td><p><strong>Datenbank</strong></p></td>
<td><p>Der Name der neuen Datenbank, die auf dem Zielserver erstellt wird.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Vertrauenswürdige Verbindung verwenden</strong></p></td>
<td><p>Gibt an, ob eine vertrauenswürdige Verbindung mit dem SQL Server besteht. Wenn sie auf <strong>"Ja"</strong>festgelegt ist, gibt es eine vertrauenswürdige Verbindung, und die Argumente <strong>"Login"</strong> und <strong>"Password"</strong> sind nicht erforderlich. Bei Festlegung auf <strong>"Nein"</strong>sind die Argumente <strong>"Login"</strong> und <strong>"Password"</strong> erforderlich. Die Standardeinstellung ist <strong>Ja</strong>. Wenn Sie eine vertrauenswürdige Verbindung verwenden, wird SQL Server Sicherheit in die Windows Betriebssystemsicherheit integriert, um eine einzige Anmeldung am Netzwerk und in der Datenbank bereitzustellen.</p></td>
</tr>
<tr class="even">
<td><p><strong>Benutzername</strong></p></td>
<td><p>Der Anmeldename für den Zielserver.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Password</strong></p></td>
<td><p>Das Kennwort für das Argument <strong>Benutzername</strong>. Dieses Kennwort wird als Text im Access-Projekt gespeichert, bleibt während des Datenbanktransfers jedoch ausgeblendet.</p></td>
</tr>
<tr class="even">
<td><p><strong>Auch Daten kopieren</strong></p></td>
<td><p>Gibt an, ob Daten in den Datenbanktransfer eingeschlossen sind. Wenn das Argument auf <strong>Ja</strong> festgelegt ist, werden alle Daten aller Tabellen sowie alle Datenstrukturen, erweiterten Eigenschaften und Datenbankobjekte eingeschlossen. Ist das Argument auf <strong>Nein</strong> festgelegt, werden keine Daten aus den Tabellen eingeschlossen. Auf dem Zielserver werden nur die Tabellenstruktur und die erweiterten Eigenschaften erstellt sowie alle sonstigen Datenbankobjekte (außer Datenbankdiagramme). Die Standardeinstellung ist <strong>Ja</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>HinwBemerkungeneise

Während des Datenbanktransfers können keine weiteren Vorgänge ausgeführt werden.

Die **TransferSQLDatenbank** -Aktion kopiert standardmäßig Daten, Datendefinitionen, Datenbankobjekte und erweiterte Eigenschaften, wie Standardwerte, Gültigkeitsmeldungseinschränkungen und Nachschlagewerte.

Voraussetzungen für das Transferieren einer Datenbank:

- You must be a member of the sysadmin role on the destination server (No special role is required on the source server).

- Der aktuelle SQL Server, der mit dem Access-Projekt verbunden ist, und der Zielserver, an den Sie die Datenbank transferieren, müssen SQL Server, Version 7.0 oder höher, sein.

  > [!NOTE]
  > [!HINWEIS] Verbindungsserver werden während eines Datenbanktransfers nicht transferiert.

Verwenden Sie die **TransferSQLDatabase** -Methode des **DoCmd** -Objekts, um die **TransferSQLDatenbank** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

