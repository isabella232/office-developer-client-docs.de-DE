---
title: QueryDef.Connect Property (DAO)
TOCTitle: Connect Property
ms:assetid: 14f19205-e92e-acc6-5677-b6d88772d5da
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845479(v=office.15)
ms:contentKeyID: 48543398
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1aef24850a2dfa9eeb801708ea773087b9d1ff40
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871444"
---
# <a name="querydefconnect-property-dao"></a>QueryDef.Connect Property (DAO)


**Betrifft**: Access 2013, Office 2013

Legt einen Wert fest, der Informationen über die Quelle der in einer Pass-Through-Abfrage verwendeten Datenbank bereitstellt, oder gibt den betreffenden Wert zurück. Schreibgeschützter **String**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . Eine Verbindung herstellen

*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung der **Connect**-Eigenschaft ist ein **String**-Wert, der aus einem Datenbanktypbezeichner und null oder mehreren durch Semikolons getrennten Parametern besteht. Die **Connect**-Eigenschaft übergibt bei Bedarf zusätzliche Informationen an ODBC- und bestimmte ISAM-Treiber.

Sie können eine SQL-Pass-Through-Abfrage für eine Tabelle ausführen, die mit Ihrer Microsoft Access-Datenbankdatei verknüpft ist, indem Sie zunächst die **Connect**-Eigenschaft der Datenbank der verknüpften Tabelle auf eine gültige ODBC-Verbindungszeichenfolge festlegen.

Der Pfad ist der vollständige Pfadname für das Verzeichnis, das die Datenbankdateien enthält, wie in der folgenden Tabelle dargestellt. Der Pfadname muss mit dem Bezeichner DATABASE= beginnen. In einigen Fällen (wie bei Microsoft Excel- und Microsoft Access-Datenbanken) muss ein spezifischer Dateiname in das Argument des Datenbankpfads einbezogen werden.

In der folgenden Tabelle sind die möglichen Datenbanktypen und ihre entsprechenden Datenbankbezeichner und Pfadnamen für die Einstellungen der **Connect** -Eigenschaft aufgelistet.

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
<td><p>Exchange 4.0; MAPILEVEL = Folderpath; [TABLETYPE = {0 | 1}]; [PROFILE = Profile;] [PWD = Password;] [DATABASE = Datenbank;]</p></td>
<td><p>Laufwerk:\Pfad\Dateiname</p></td>
</tr>
</tbody>
</table>


Wenn der Bezeichner nur "ODBC;" lautet, zeigt der ODBC-Treiber ein Dialogfeld an, in dem alle registrierten ODBC-Datenquellennamen aufgeführt werden, sodass der Benutzer eine Datenbank auswählen kann.

Wenn ein Kennwort erforderlich ist, aber in der **Connect** -Eigenschaft nicht angegeben wird, wird ein Anmelde-Dialogfeld angezeigt, wenn der ODBC-Treiber erstmals auf eine Tabelle zugreift, und erneut, wenn die Verbindung geschlossen und neu geöffnet wird.

Für Daten in Microsoft Exchange sollte der erforderliche MAPILEVEL-Schlüssel in einen vollständig aufgelöster Ordnerpfad (beispielsweise "Postfach – Pat SmithIAlpha/heute") festgelegt werden. Der Pfad schließt nicht den Namen des Ordners ein, der als Tabelle geöffnet wird. der Name dieses Ordners sollten stattdessen als Namenargument für die **CreateTable** -Methode angegeben werden. Öffnen Sie einen Ordner (Standard) oder "1" zum Öffnen eines Adressbuchs sollte der TABLETYPE-Schlüssel auf "0" festgelegt werden. Die wichtigsten profilstandardeinstellungen Profil verwenden derzeit.

Für ein **QueryDef** -Objekt in einer Microsoft Access-Arbeitsbereich können Sie die **Connect** -Eigenschaft mit der ReturnsRecords-Eigenschaft verwenden, um eine ODBC SQL Pass-Through-Abfrage zu erstellen. Die "databasetype" der Verbindungszeichenfolge ist "ODBC;", und den Rest der Zeichenfolge enthält Informationen zu den ODBC-Treiber verwendet, um die remote-Daten zugreifen. Weitere Informationen finden Sie in der Dokumentation des Treibers.


> [!NOTE]
> <UL>
> <LI>
> <P>Vor dem Festlegen der <STRONG>ReturnsRecords</STRONG>-Eigenschaft müssen Sie die <STRONG>Connect</STRONG>-Eigenschaft festlegen.</P>
> <LI>
> <P>Sie müssen die Zugriffsberechtigungen für den Computer besitzen, der den Datenbankserver enthält, auf den Sie zugreifen wollen.</P></LI></UL>


