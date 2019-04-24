---
title: QueryDef. Connect-Eigenschaft (DAO)
TOCTitle: Connect Property
ms:assetid: 14f19205-e92e-acc6-5677-b6d88772d5da
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845479(v=office.15)
ms:contentKeyID: 48543398
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 009e49a96ea1cd5ee3db0b96adb9cae4a6bce21b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301085"
---
# <a name="querydefconnect-property-dao"></a>QueryDef. Connect-Eigenschaft (DAO)

**Gilt für**: Access 2013, Office 2013

Legt einen Wert fest, der Informationen über die Quelle der in einer Pass-Through-Abfrage verwendeten Datenbank bereitstellt, oder gibt den betreffenden Wert zurück. Schreibgeschützter **String**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . Verbinden

*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung der **Connect**-Eigenschaft ist ein **String**-Wert, der aus einem Datenbanktypbezeichner und null oder mehreren durch Semikolons getrennten Parametern besteht. Die **Connect**-Eigenschaft übergibt bei Bedarf zusätzliche Informationen an ODBC- und bestimmte ISAM-Treiber.

Sie können eine SQL-Pass-Through-Abfrage für eine Tabelle ausführen, die mit Ihrer Microsoft Access-Datenbankdatei verknüpft ist, indem Sie zunächst die **Connect**-Eigenschaft der Datenbank der verknüpften Tabelle auf eine gültige ODBC-Verbindungszeichenfolge festlegen.

Der Pfad, wie in der folgenden Tabelle dargestellt, ist der vollständige Pfad für das Verzeichnis, das die Datenbankdateien enthält, und es muss der Bezeichner DATABASE = vorangestellt werden. In einigen Fällen (wie in den Datenbanken von Microsoft Excel und Microsoft Access-Datenbankmodul) sollten Sie einen bestimmten Dateinamen in das Argument Datenbankpfad aufnehmen.

In der folgenden Tabelle sind die möglichen Datenbanktypen und ihre entsprechenden Datenbankbezeichner und Pfadnamen für die Einstellungen der **Connect**-Eigenschaft aufgelistet.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Datenbanktyp</p></th>
<th><p>Bezeichner</p></th>
<th><p>Beispiel</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Microsoft Access-Datenbank</p></td>
<td><p>[Datenbank];</p></td>
<td><p>Laufwerk:\Pfad\Dateiname</p></td>
</tr>
<tr class="even">
<td><p>dBASE III</p></td>
<td><p>dBASE III;</p></td>
<td><p>Laufwerk:\Pfad</p></td>
</tr>
<tr class="odd">
<td><p>dBASE IV</p></td>
<td><p>dBASE IV;</p></td>
<td><p>Laufwerk:\Pfad</p></td>
</tr>
<tr class="even">
<td><p>dBASE 5</p></td>
<td><p>dBASE 5.0;</p></td>
<td><p>Laufwerk:\Pfad</p></td>
</tr>
<tr class="odd">
<td><p>Paradox 3.x</p></td>
<td><p>Paradox 3.x;</p></td>
<td><p>Laufwerk:\Pfad</p></td>
</tr>
<tr class="even">
<td><p>Paradox 4.x</p></td>
<td><p>Paradox 4.x;</p></td>
<td><p>Laufwerk:\Pfad</p></td>
</tr>
<tr class="odd">
<td><p>Paradox 5.x</p></td>
<td><p>Paradox 5.x;</p></td>
<td><p>Laufwerk:\Pfad</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel 3.0</p></td>
<td><p>Excel 3.0;</p></td>
<td><p>Laufwerk: \ path\filename.xls</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 4.0</p></td>
<td><p>Excel 4.0;</p></td>
<td><p>Laufwerk: \ path\filename.xls</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel 5.0 oder Microsoft Excel 95</p></td>
<td><p>Excel 5.0;</p></td>
<td><p>Laufwerk: \ path\filename.xls</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 97</p></td>
<td><p>Excel 8.0;</p></td>
<td><p>Laufwerk: \ path\filename.xls</p></td>
</tr>
<tr class="even">
<td><p>Lotus 1-2-3 WKS und WK1</p></td>
<td><p>Lotus WK1;</p></td>
<td><p>Laufwerk: \ path\filename.WK1</p></td>
</tr>
<tr class="odd">
<td><p>Lotus 1-2-3 WK3</p></td>
<td><p>Lotus WK3;</p></td>
<td><p>Laufwerk: \ path\filename.WK3</p></td>
</tr>
<tr class="even">
<td><p>Lotus 1-2-3 WK4</p></td>
<td><p>Lotus WK4;</p></td>
<td><p>Laufwerk: \ path\filename.WK4</p></td>
</tr>
<tr class="odd">
<td><p>HTML-Import</p></td>
<td><p>HTML-Import;</p></td>
<td><p>Laufwerk:\Pfad\Dateiname</p></td>
</tr>
<tr class="even">
<td><p>HTML-Export</p></td>
<td><p>HTML-Export;</p></td>
<td><p>Laufwerk:\Pfad</p></td>
</tr>
<tr class="odd">
<td><p>Text</p></td>
<td><p>Text;</p></td>
<td><p>Laufwerk:\Pfad</p></td>
</tr>
<tr class="even">
<td><p>ODBC</p></td>
<td><p>ODBC; DATABASE=Datenbank; UID=Benutzer; PWD=Kennwort; DSN= Datenquellenname; [LOGINTIMEOUT=Sekunden;]</p></td>
<td><p>Keine</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Exchange</p></td>
<td><p>Exchange 4,0; MAPILEVEL = folderPath; [BASISTYP = {0 | 1}]; [PROFILE = Profil;] [PWD = Kennwort;] [DATABASE = Datenbank;]</p></td>
<td><p>Laufwerk:\Pfad\Dateiname</p></td>
</tr>
</tbody>
</table>


Wenn der Bezeichner nur "ODBC;" lautet, zeigt der ODBC-Treiber ein Dialogfeld an, in dem alle registrierten ODBC-Datenquellennamen aufgeführt werden, sodass der Benutzer eine Datenbank auswählen kann.

Wenn ein Kennwort erforderlich ist, aber in der **Connect**-Eigenschaft nicht angegeben wird, wird ein Anmelde-Dialogfeld angezeigt, wenn der ODBC-Treiber erstmals auf eine Tabelle zugreift, und erneut, wenn die Verbindung geschlossen und neu geöffnet wird.

Für Daten in Microsoft Exchange muss für den erforderlichen MAPILEVEL-Schlüssel ein vollständig aufgelöster Ordnerpfad angegeben werden (z. B. "Mailbox - Pat SmithIAlpha/Today"). Der Pfad umfasst nicht den Namen des Ordners, der als Tabelle geöffnet wird. Der Name dieses Ordners muss stattdessen als name-Argument der **CreateTable**-Methode angegeben werden. Zum Öffnen eines Ordners muss der TABLETYPE-Schlüssel auf "0" gesetzt werden (Standard), zum Öffnen eines Adressbuchs muss er den Wert "1" erhalten. Der PROFILE-Schlüssel erhält standardmäßig den Wert des aktuell verwendeten Profils.

On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query. Der DatabaseType der Verbindungszeichenfolge ist "ODBC;", und der Rest der Zeichenfolge enthält spezifische Informationen für den ODBC-Treiber, der für den Zugriff auf die Remotedaten verwendet wird. For more information, see the documentation for the specific driver.

> [!NOTE]
> - Vor dem Festlegen der **ReturnsRecords**-Eigenschaft müssen Sie die **Connect**-Eigenschaft festlegen.
> - Sie müssen die Zugriffsberechtigungen für den Computer besitzen, der den Datenbankserver enthält, auf den Sie zugreifen wollen.


