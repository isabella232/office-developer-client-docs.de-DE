---
title: TableDef.Connect-Eigenschaft (DAO)
TOCTitle: Connect Property
ms:assetid: 4fbb324c-a358-8fad-60f2-fb8005cf74d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193791(v=office.15)
ms:contentKeyID: 48544782
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053064
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c15343c003de0328d55125d52dcef865110665f0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881153"
---
# <a name="tabledefconnect-property-dao"></a>TableDef.Connect-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

Legt einen Wert fest, der Informationen über eine verknüpfte Tabelle bereitstellt, oder gibt den betreffenden Wert zurück. **String** -Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . Eine Verbindung herstellen

*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung der **Connect** -Eigenschaft ist ein **String** -Wert, der aus einem Datenbanktypbezeichner und null oder mehreren durch Semikolons getrennten Parametern besteht. Die **Connect** -Eigenschaft übergibt bei Bedarf zusätzliche Informationen an ODBC- und bestimmte ISAM-Treiber.

Bei einem **TableDef** -Objekt, das eine verknüpfte Tabelle darstellt, besteht die **Connect** -Eigenschaft aus einem oder zwei Teilen (ein Datenbanktypbezeichner und ein Pfad für die Datenbank). Beide Teile enden mit einem Semikolon.

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


Wenn ein Kennwort erforderlich ist, aber in der **Connect** -Eigenschaft nicht angegeben wird, wird ein Anmelde-Dialogfeld angezeigt, wenn der ODBC-Treiber erstmals auf eine Tabelle zugreift, und erneut, wenn die Verbindung geschlossen und neu geöffnet wird.

Für Daten in Microsoft Exchange sollte der erforderliche MAPILEVEL-Schlüssel in einen vollständig aufgelöster Ordnerpfad (beispielsweise "Postfach – Pat SmithIAlpha/heute") festgelegt werden. Der Pfad schließt nicht den Namen des Ordners ein, der als Tabelle geöffnet wird. der Name dieses Ordners sollten stattdessen als Namenargument für die **CreateTable** -Methode angegeben werden. Öffnen Sie einen Ordner (Standard) oder "1" zum Öffnen eines Adressbuchs sollte der TABLETYPE-Schlüssel auf "0" festgelegt werden. Die wichtigsten profilstandardeinstellungen Profil verwenden derzeit.

Für Basistabellen in einer Micorosoft Access-Datenbank ist der Wert der **Connect** -Eigenschaft eine Null-Zeichenfolge ("").


> [!NOTE]
> <UL>
> <LI>
> <P>[!HINWEIS] Vor dem Festlegen der <STRONG>ReturnsRecords</STRONG> -Eigenschaft müssen Sie die <STRONG>Connect</STRONG> -Eigenschaft festlegen.</P>
> <LI>
> <P>Sie müssen die Zugriffsberechtigungen für den Computer besitzen, der den Datenbankserver enthält, auf den Sie zugreifen wollen.</P></LI></UL>


