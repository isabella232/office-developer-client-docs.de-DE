---
title: Initialisieren des Microsoft Exchange-Datenquellentreibers
TOCTitle: Initializing the Microsoft Exchange Data Source driver
ms:assetid: cf87a746-f846-1a01-f4ec-20a25e335193
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834677(v=office.15)
ms:contentKeyID: 48547810
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032667
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 1365e21a7b316d6513d1aad2e62a08c60f24289b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631958"
---
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a>Initialisieren des Microsoft Exchange-Datenquellentreibers

**Gilt für**: Access 2013, Office 2013

Wenn Sie den Microsoft Exchange Datenquellentreiber installieren, schreibt das Setupprogramm einen Satz von Standardwerten in die Unterschlüssel Engines und ISAM Formats der Microsoft Windows-Registrierung. You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings. The following sections describe initialization and ISAM Format settings for the Microsoft Exchange Data Source driver.

## <a name="microsoft-exchange-data-source-initialization-settings"></a>Initialisierungseinstellungen für Microsoft Exchange Datenquellen

Der Ordner **Access Connectivity Engine \\ Engines \\ Exchange** enthält Initialisierungseinstellungen für den Aceexch.dll-Treiber, der für den externen Zugriff auf Microsoft Outlook- und Microsoft Exchange-Ordner verwendet wird. The only entry in this folder is the following:

`win32=<path>\ACEEXCH.DLL`

The Microsoft Access database engine uses this setting to indicate the location of Aceexch.dll. Der vollständige Pfad wird bei der Installation festgelegt. Werte sind vom Typ REG \_ SZ.

Die Verwendung des Outlook-ISAM-Formats und des Exchange-Client-ISAM-Formats liefert ähnliche Ergebnisse. Der einzige Unterschied besteht darin, dass die beiden unterschiedlichen Clients für dieselben Spalten unterschiedliche Namen verwenden. Die beiden ISAM-Formate wurden erstellt, damit das Microsoft Access-Datenbankmodul die Spaltennamen in dem vom Benutzer gewünschten Format zurückgeben kann.

## <a name="microsoft-outlook-client-isam-formats"></a>ISAM-Formate des Microsoft Outlook-Clients

The **Access Connectivity Engine \\ ISAM Formats Outlook \\ 9.0** folder contains the following entries.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name des Eintrags</p></th>
<th><p>Typ</p></th>
<th><p>Wert</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Motor</p></td>
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



## <a name="microsoft-exchange-client-isam-formats"></a>MICROSOFT Exchange-Client-ISAM-Formate

The **Access Connectivity Engine \\ ISAM Formats Exchange \\ 4.0** folder contains the following entries.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name des Eintrags</p></th>
<th><p>Typ</p></th>
<th><p>Wert</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Motor</p></td>
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



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a>Anpassen der Schema.ini datei für Outlook und Exchange Daten

The Schema.ini file is used by the Outlook and Exchange ISAM in much the same way that it is used by the Text ISAM. Schema.ini contains the specifics of a data source: how the data is formatted, and the names of columns that should be accessed.

It is not necessary to modify the Schema.ini file before data can be read, imported, or exported for Outlook and Exchange. Many of the settings inside the Schema.ini file for Outlook and Exchange are specific to internal tags that MAPI requires. You should not attempt to modify those tag values.

