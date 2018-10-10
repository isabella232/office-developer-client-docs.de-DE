---
title: TransferSQLDatenbank-Makroaktion
TOCTitle: TransferSQLDatabase Macro Action
ms:assetid: 8cb95e22-f1f0-6c70-7dcb-3a3e9aafdc57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197344(v=office.15)
ms:contentKeyID: 48546244
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm111536
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 301fce8bcdeff45135c305054da72f4c75f503eb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473247"
---
# <a name="transfersqldatabase-macro-action"></a>TransferSQLDatenbank-Makroaktion


**Betrifft**: Access 2013 | Office 2013

Verwenden Sie in einem Access-Projekt die **TransferSQLDatenbank** -Aktion, um eine Microsoft SQL Server-Datenbank der Version 7.0 oder höher zu übertragen. Weitere Informationen zum Übertragen einer Datenbank finden Sie in der SQL Server-Dokumentation.


> [!NOTE]
> <P>[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</P>



## <a name="setting"></a>Einstellung

Die **TransferSQLDatenbank** -Aktion hat die folgenden Argumente.

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
<td><p><strong>Database</strong></p></td>
<td><p>Der Name der neuen Datenbank, die auf dem Zielserver erstellt wird.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Vertrauenswürdige Verbindung verwenden</strong></p></td>
<td><p>Gibt an ist, ob eine vertrauenswürdige Verbindung zu SQL Server nicht vorhanden. Wenn legen Sie auf <strong>Ja</strong>, und klicken Sie dann eine vertrauenswürdige Verbindung vorhanden ist und die Argumente <strong>Benutzername</strong> und <strong>Kennwort</strong> nicht erforderlich sind. Wenn Sie auf <strong>Nein</strong>, den <strong>Benutzernamen</strong> und <strong>das Kennwort</strong> Argumente erforderlich sind. Die Standardeinstellung ist <strong>Ja</strong>. Wenn Sie eine vertrauenswürdige Verbindung verwenden, ist SQL Server-Sicherheit in die Sicherheit des Betriebssystems Windows anzugebende eine einzige Anmeldung am Netzwerk und die Datenbank integriert.</p></td>
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


## <a name="remarks"></a>Hinweise

Während des Datenbanktransfers können keine weiteren Vorgänge ausgeführt werden.

Die **TransferSQLDatenbank** -Aktion kopiert standardmäßig Daten, Datendefinitionen, Datenbankobjekte und erweiterte Eigenschaften, wie Standardwerte, Gültigkeitsmeldungseinschränkungen und Nachschlagewerte.

Voraussetzungen für das Transferieren einer Datenbank:

  - Sie müssen auf dem Zielserver ein Mitglied der Rolle sysadmin sein. (Auf dem Quellserver ist keine spezielle Rolle erforderlich.)

<!-- end list -->

  - Der aktuelle SQL Server, der mit dem Access-Projekt verbunden ist, und der Zielserver, an den Sie die Datenbank transferieren, müssen SQL Server, Version 7.0 oder höher, sein.


> [!NOTE]
> <P>[!HINWEIS] Verbindungsserver werden während eines Datenbanktransfers nicht transferiert.</P>



Verwenden Sie die **TransferSQLDatabase** -Methode des **DoCmd** -Objekts, um die **TransferSQLDatenbank** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

