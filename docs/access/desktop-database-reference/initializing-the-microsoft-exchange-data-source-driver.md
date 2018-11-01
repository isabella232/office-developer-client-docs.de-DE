---
title: Initialisieren des Microsoft Exchange-Datenquellentreibers
TOCTitle: Initializing the Microsoft Exchange Data Source Driver
ms:assetid: cf87a746-f846-1a01-f4ec-20a25e335193
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834677(v=office.15)
ms:contentKeyID: 48547810
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032667
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c1ba74f754ef0c998a14f7421914bd4bcd7c9cf9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870198"
---
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a>Initialisieren des Microsoft Exchange-Datenquellentreibers

**Betrifft**: Access 2013, Office 2013

Beim Installieren des Microsoft® Exchange-Datenquellentreibers schreibt das Setupprogramm Standardwerte in die Unterschlüssel Engines und ISAM Formats der Microsoft Windows®-Registrierung. Diese Einstellungen dürfen nicht direkt geändert werden. Verwenden Sie stattdessen das Setupprogramm, um diese Einstellungen hinzuzufügen, zu entfernen oder zu ändern. In den folgenden Abschnitten werden die Einstellungen für die Initialisierung und das ISAM-Format für den Microsoft Exchange-Datenquellentreiber beschrieben.

## <a name="microsoft-exchange-data-source-initialization-settings"></a>Initialisierungseinstellungen für Microsoft Exchange-Datenquellen

Die **Konnektivitätsmodul für Access\\Module\\Exchange** Ordner enthält initialisierungseinstellungen für Aceexch.dll-Treiber für den externen Zugriff auf Microsoft Outlook und Microsoft Exchange-Ordner verwendet. Der einzige Eintrag in diesem Ordner lautet wie folgt:

`win32=<path>\ACEEXCH.DLL`

Microsoft Access-Datenbankmodul verwendet diese Einstellung, um den Speicherort der Aceexch.dll anzugeben. Der vollständige Pfad wird bei der Installation bestimmt. Werte sind vom Typ REG\_su.

Die Verwendung des Outlook-ISAM-Formats und des Exchange-Client-ISAM-Formats liefert ähnliche Ergebnisse. Der einzige Unterschied besteht darin, dass die beiden unterschiedlichen Clients für dieselben Spalten unterschiedliche Namen verwenden. Die beiden ISAM-Formate wurden erstellt, damit das Microsoft Access-Datenbankmodul die Spaltennamen in dem vom Benutzer gewünschten Format zurückgeben kann.

## <a name="microsoft-outlook-client-isam-formats"></a>Microsoft Outlook-Client-ISAM-Formate

Die **Konnektivitätsmodul für Access\\-ISAM-Formate\\Outlook 9.0** Ordner enthält die folgenden Einträge.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name des Eintrags</p></th>
<th><p>Type</p></th>
<th><p>Wert</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Engine</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange</p></td>
</tr>
<tr class="even">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Outlook()</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> Wenn Sie Einstellungen in der Windows-Registrierung ändern, müssen Sie das Datenbankmodul beenden und erneut starten, damit die neuen Einstellungen wirksam werden.



## <a name="microsoft-exchange-client-isam-formats"></a>Microsoft Exchange-Client-ISAM-Formate

Die **Konnektivitätsmodul für Access\\-ISAM-Formate\\Exchange 4.0** Ordner enthält die folgenden Einträge.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name des Eintrags</p></th>
<th><p>Type</p></th>
<th><p>Wert</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Engine</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange</p></td>
</tr>
<tr class="even">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange()</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> Wenn Sie Einstellungen in der Windows-Registrierung ändern, müssen Sie das Datenbankmodul beenden und erneut starten, damit die neuen Einstellungen wirksam werden.



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a>Anpassen der Datei "Schema.ini" für Outlook- und Exchange-Daten

Die Datei Schema.ini wird von Outlook- und Exchange-ISAM weitgehend wie von Text-ISAM verwendet. Schema.ini enthält die Angaben zur Datenquelle: wie die Daten formatiert werden und die Namen der zu verwendenden Spalten.

Es ist nicht erforderlich, die Datei Schema.ini zu ändern, um Daten für Outlook und Exchange zu lesen, zu importieren oder zu exportieren. Viele der Einstellungen für Outlook und Exchange in der Datei Schema.ini beziehen sich auf interne Tags, die für MAPI benötigt werden. Sie sollten nicht versuchen, diese Tagwerte zu ändern.

