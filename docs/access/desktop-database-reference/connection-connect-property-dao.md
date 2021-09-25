---
title: Verbindung. Verbinden-Eigenschaft (DAO)
TOCTitle: Connect Property
ms:assetid: 58b514a2-91cd-7918-cba5-15d71c2457a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194335(v=office.15)
ms:contentKeyID: 48545001
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 39576c39546e3f02652a0d997044fc2afac80010
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565765"
---
# <a name="connectionconnect-property-dao"></a>Verbindung. Verbinden-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Legt einen Wert fest, der Informationen zur Quelle einer geöffneten Verbindung bereitstellt, oder gibt den Wert zurück. **String**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*expression* .Connect

*Ausdruck* Eine Variable, die ein **Connection** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung der **Connect**-Eigenschaft ist ein **String**-Wert, der aus einem Datenbanktypbezeichner und null oder mehreren durch Semikolons getrennten Parametern besteht. Die **Connect**-Eigenschaft übergibt bei Bedarf zusätzliche Informationen an ODBC- und bestimmte ISAM-Treiber.

Wenn Sie eine SQL Pass-Through-Abfrage zu einer Tabelle ausführen möchten, die mit der Microsoft Access-Datenbankdatei verknüpft ist, müssen Sie zuerst die **Connect**-Eigenschaft der Datenbank, zu der die verknüpfte Tabelle gehört, auf eine gültige ODBC-Verbindungszeichenfolge festlegen.

Bei einem **TableDef** -Objekt, das eine verknüpfte Tabelle darstellt, besteht die **Connect** -Eigenschaft aus einem oder zwei Teilen (ein Datenbanktypbezeichner und ein Pfad für die Datenbank). Beide Teile enden mit einem Semikolon.

Der Pfad ist der vollständige Pfadname für das Verzeichnis, das die Datenbankdateien enthält, wie in der folgenden Tabelle dargestellt. Der Pfadname muss mit dem Bezeichner DATABASE= beginnen. In einigen Fällen (wie bei Microsoft Excel- und Microsoft Access-Datenbanken) muss ein spezifischer Dateiname in das Argument des Datenbankpfads einbezogen werden.

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
<td><p>Laufwerk:\Pfad\Dateiname.xls</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 4.0</p></td>
<td><p>Excel 4.0;</p></td>
<td><p>Laufwerk:\Pfad\Dateiname.xls</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel 5.0 oder Microsoft Excel 95</p></td>
<td><p>Excel 5.0;</p></td>
<td><p>Laufwerk:\Pfad\Dateiname.xls</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 97</p></td>
<td><p>Excel 8.0;</p></td>
<td><p>Laufwerk:\Pfad\Dateiname.xls</p></td>
</tr>
<tr class="even">
<td><p>Lotus 1-2-3 WKS und WK1</p></td>
<td><p>Lotus WK1;</p></td>
<td><p>Laufwerk:\Pfad\Dateiname.wk1</p></td>
</tr>
<tr class="odd">
<td><p>Lotus 1-2-3 WK3</p></td>
<td><p>Lotus WK3;</p></td>
<td><p>Laufwerk:\Pfad\Dateiname.wk3</p></td>
</tr>
<tr class="even">
<td><p>Lotus 1-2-3 WK4</p></td>
<td><p>Lotus WK4;</p></td>
<td><p>Laufwerk:\Pfad\Dateiname.wk4</p></td>
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
<td><p>Exchange 4.0; MAPILEVEL=Ordnerpfad; [TABLETYPE={ 0 | 1 }];[PROFILE=Profil;] [PWD=Kennwort;] [DATABASE=Datenbank;]</p></td>
<td><p>Laufwerk:\Pfad\Dateiname</p></td>
</tr>
</tbody>
</table>


Wenn der Bezeichner nur "ODBC;" lautet, zeigt der ODBC-Treiber ein Dialogfeld an, in dem alle registrierten ODBC-Datenquellennamen aufgeführt werden, sodass der Benutzer eine Datenbank auswählen kann.

Wenn ein Kennwort erforderlich ist, aber in der **Connect**-Eigenschaft nicht angegeben wird, wird ein Anmelde-Dialogfeld angezeigt, wenn der ODBC-Treiber erstmals auf eine Tabelle zugreift, und erneut, wenn die Verbindung geschlossen und neu geöffnet wird.

Für Daten in Microsoft Exchange muss für den erforderlichen MAPILEVEL-Schlüssel ein vollständig aufgelöster Ordnerpfad angegeben werden (z. B. "Mailbox - Pat SmithIAlpha/Today"). Der Pfad umfasst nicht den Namen des Ordners, der als Tabelle geöffnet wird. Der Name dieses Ordners muss stattdessen als name-Argument der **CreateTable**-Methode angegeben werden. Zum Öffnen eines Ordners muss der TABLETYPE-Schlüssel auf "0" gesetzt werden (Standard), zum Öffnen eines Adressbuchs muss er den Wert "1" erhalten. Der PROFILE-Schlüssel erhält standardmäßig den Wert des aktuell verwendeten Profils.

Für Basistabellen in einer Micorosoft Access-Datenbank ist der Wert der **Connect**-Eigenschaft eine Null-Zeichenfolge ("").

Sie können die **Verbinden-Eigenschaft** für ein **Database-Objekt** festlegen, indem Sie ein Quellargument für die **OpenDatabase-Methode** angeben. Überprüfen Sie die Einstellung, um den Typ, den Pfad, die Benutzer-ID, das Kennwort oder die ODBC-Datenquelle der Datenbank zu ermitteln.

On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query. Der Datenbanktyp der Verbindungszeichenfolge lautet "ODBC;", und der Rest der Zeichenfolge enthält Informationen speziell für den ODBC-Treiber, der für den Zugriff auf die Remotedaten verwendet wird. For more information, see the documentation for the specific driver.


> [!NOTE]
> - Vor dem Festlegen der **ReturnsRecords**-Eigenschaft müssen Sie die **Connect**-Eigenschaft festlegen.
> - Sie müssen die Zugriffsberechtigungen für den Computer besitzen, der den Datenbankserver enthält, auf den Sie zugreifen wollen.


