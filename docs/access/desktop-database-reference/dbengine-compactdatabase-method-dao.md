---
title: DBEngine.CompactDatabase-Methode (DAO)
TOCTitle: CompactDatabase Method
ms:assetid: 03f3a156-005a-4b71-81b0-598f326f7d42
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844821(v=office.15)
ms:contentKeyID: 48542997
ms.date: 10/24/2016
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052936
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: b50cb0453df1fa357fbd0b089af2e74fdd4b4c1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294337"
---
# <a name="dbenginecompactdatabase-method-dao"></a>DBEngine.CompactDatabase-Methode (DAO)

**Gilt für:** Access 2013 | Access 2016

Kopiert und komprimiert eine geschlossene Datenbank und bietet die Möglichkeit, ihre Version, Sortierreihenfolge und Verschlüsselung festzulegen. (Nur Microsoft Access-Arbeitsbereiche).

> [!NOTE]
> Wenn Sie verschlüsselte verknüpfte Tabellen für action-, update- und SQL-Abfragen verwenden, z. B. eine SQL UPDATE-Anweisung (CurrentDb.Execute „UPDATE..."), müssen Sie den Verschlüsselungsschlüssel angeben. Verknüpfte Tabellen weisen außerdem eine Beschränkung von 19 Zeichen für den Verschlüsselungsschlüssel auf. Weitere Informationen finden Sie im Abschnitt **Verschlüsselte verknüpfte Tabellen** am Ende dieses Themas.

## <a name="syntax"></a>Syntax

*expression* .CompactDatabase(***SrcName***, ***DstName***, ***DstLocale***, ***Options***, ***password***)

*expression* Ein Ausdruck, der ein **DBEngine**-Objekt zurückgibt.

## <a name="parameters"></a>Parameter

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Erforderlich/optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>SrcName</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Gibt eine vorhandene geschlossene Datenbank an. Dies kann ein vollständiger Pfad- und Dateiname sein, z. B. &quot;C:\db1.mdb&quot;. Wenn der Dateiname eine Erweiterung aufweist, müssen Sie diese angeben. Wenn Ihr Netzwerk dies unterstützt, können Sie auch einen Netzwerkpfad wie &quot;\\server1\share1\dir1\db1.mdb&quot; angeben.</p></td>
</tr>
<tr class="even">
<td><p><em>DstName</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Der Dateiname (und Pfad) der komprimierten Datenbank, die Sie erstellen. Sie können auch einen Netzwerkpfad angeben. Mit diesem Argument kann nicht die gleiche Datenbankdatei angegeben werden wie mit SrcName.</p></td>
</tr>
<tr class="odd">
<td><p><em>DstLocale</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein Zeichenfolgenausdruck, der eine Sortierreihenfolge zum Erstellen von DstName angibt, wie unter „Hinweise“ angegeben.</p>
<ul>
<li><p>Wenn Sie dieses Argument weglassen, hat DstName das gleiche Gebietsschema wie SrcName.</p></li>
<li><p>Sie können auch ein Kennwort für DstName erstellen, indem Sie die Kennwortzeichenfolge (die mit &quot;;pwd=&quot; beginnt) wie folgt mit einer Konstanten im DstLocale-Argument verketten: dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;.</p></li>
<li><p>Wenn Sie für DstLocale den gleichen Wert wie für SrcName verwenden (Standardwert), aber ein neues Kennwort angeben möchten, geben Sie einfach eine Kennwortzeichenfolge für DstLocale ein: &quot;;pwd=NewPassword&quot;</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><em>Optionen</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Optional. Ein Konstante oder Kombination aus Konstanten, mit der mindestens eine Option angegeben wird, wie unter „Hinweise“ angegeben. Sie können Optionen durch Summieren der entsprechenden Konstanten kombinieren.</p></td>
</tr>
<tr class="odd">
<td><p><em>password</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein Zeichenfolgenausdruck, der einen Verschlüsselungsschlüssel enthält, wenn die Datenbank verschlüsselt ist. Die Zeichenfolge &quot;;pwd=&quot; muss vor dem eigentlichen Kennwort stehen. Wenn Sie eine Kennworteinstellung in DstLocale einschließen, wird diese Einstellung ignoriert.</p><p><strong>HINWEIS</strong>: Dies ist ein veralteter Parameter, der im ACCDB-Format nicht unterstützt wird. Zum Verschlüsseln einer ACCDB-Datei, verwenden Sie die "pwd="-Optionszeichenfolge. Verwenden Sie sichere Kennwörter, die Groß- und Kleinbuchstaben, Zahlen und Symbole in Kombination verwenden. Unsichere Kennwörter enthalten keine Kombination dieser Elemente. Sicheres Kennwort: Y6dh!et5. Unsicheres Kennwort: Haus27. Verwenden Sie ein sicheres Kennwort, das Sie sich merken können, damit Sie es nicht aufschreiben müssen.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Sie können eine der folgenden Konstanten für das DstLocale-Argument verwenden, um die **CollatingOrder** -Eigenschaft für Zeichenfolgenvergleiche von Text anzugeben.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Sortierreihenfolge</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbLangGeneral</strong></p></td>
<td><p>Englisch, Deutsch, Französisch, Portugiesisch, Italienisch und modernes Spanisch</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangArabic</strong></p></td>
<td><p>Arabic</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangChineseSimplified</strong></p></td>
<td><p>Chinesisch (vereinfacht)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangChineseTraditional</strong></p></td>
<td><p>Chinesisch (traditionell)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangCyrillic</strong></p></td>
<td><p>Russisch</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangCzech</strong></p></td>
<td><p>Tschechisch</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangDutch</strong></p></td>
<td><p>Niederländisch</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangGreek</strong></p></td>
<td><p>Griechisch</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangHebrew</strong></p></td>
<td><p>Hebräisch</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangHungarian</strong></p></td>
<td><p>Ungarisch</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangIcelandic</strong></p></td>
<td><p>Isländisch</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangJapanese</strong></p></td>
<td><p>Japanisch</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangKorean</strong></p></td>
<td><p>Koreanisch</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangNordic</strong></p></td>
<td><p>Nordeuropäische Sprachen (nur Version 1.0 des Microsoft Jet-Datenbankmoduls)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangNorwDan</strong></p></td>
<td><p>Norwegisch und Dänisch</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangPolish</strong></p></td>
<td><p>Polnisch</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangSlovenian</strong></p></td>
<td><p>Slowenisch</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangSpanish</strong></p></td>
<td><p>Spanisch (Traditionell)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangSwedFin</strong></p></td>
<td><p>Schwedisch und Finnisch</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangThai</strong></p></td>
<td><p>Thailändisch</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangTurkish</strong></p></td>
<td><p>Türkisch</p></td>
</tr>
</tbody>
</table>

<br/>

Sie können eine der folgenden Konstanten im options-Argument verwenden, um anzugeben, ob die Datenbank während der Komprimierung verschlüsselt werden soll.

> [!NOTE]
> Die Konstanten dbEncrypt und dbDecrypt sind veraltet und werden im ACCDB-Dateiformat nicht unterstützt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbEncrypt</strong></p></td>
<td><p>Verschlüsselt die Datenbank beim Komprimieren.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDecrypt</strong></p></td>
<td><p>Entschlüsselt die Datenbank beim Komprimieren.</p></td>
</tr>
</tbody>
</table>

<br/>

Wenn Sie keine Verschlüsselungskonstante angeben, oder wenn Sie sowohl **DbDecrypt** als auch **DbEncrypt** einschließen, hat DstName die gleiche Verschlüsselung wie SrcName.

Sie können eine der folgenden Konstanten im options-Argument verwenden, um die Version des Datenformats für die komprimierte Datenbank anzugeben. Diese Konstante betrifft nur die Version des Datenformats von DstName und hat keine Auswirkungen auf die Version von von Microsoft Access definierten Objekten, wie Formulare und Berichte.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbVersion10</strong></p></td>
<td><p>Erstellt eine Datenbank, die beim Komprimieren das Dateiformat der Version 1.0 des Microsoft Jet-Datenbankmoduls verwendet.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion11</strong></p></td>
<td><p>Erstellt eine Datenbank, die beim Komprimieren das Dateiformat der Version 1.1 des Microsoft Jet-Datenbankmoduls verwendet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion20</strong></p></td>
<td><p>Erstellt eine Datenbank, die beim Komprimieren das Dateiformat der Version 2.0 des Microsoft Jet-Datenbankmoduls verwendet.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion30</strong></p></td>
<td><p>Erstellt eine Datenbank, die beim Komprimieren das Dateiformat der Version 3.0 des Microsoft Jet-Datenbankmoduls (kompatibel mit Version 3.5) verwendet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion40</strong></p></td>
<td><p>Erstellt eine Datenbank, die beim Komprimieren das Dateiformat der Version 4.0 des Microsoft Jet-Datenbankmoduls verwendet.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion120</strong></p></td>
<td><p>Erstellt eine Datenbank, die beim Komprimieren das Dateiformat der Version 12.0 des Microsoft Access-Datenbankmoduls verwendet.</p></td>
</tr>
</tbody>
</table>

<br/>

Sie können nur eine Versionskonstante angeben. Wenn Sie keine Versionskonstante angeben, hat DstName die gleiche Version wie SrcName. Sie können DstName nur auf eine Version komprimieren, die der von SrcName entspricht oder höher ist.

Wenn Sie Daten in einer Datenbank ändern, kann die Datenbankdatei fragmentiert werden und mehr Speicherplatz belegen als erforderlich. Sie können die Datenbank in regelmäßigen Abständen mit der **CompactDatabase**-Methode komprimieren, um die Datenbankdatei zu defragmentieren. Die komprimierte Datenbank ist in der Regel kleiner und wird oft schneller ausgeführt. Sie können auch die Sortierreihenfolge, die Verschlüsselung oder die Version des Datenformats ändern, während Sie die Datenbank kopieren und komprimieren.

Sie müssen SrcName schließen, bevor Sie die Datenbank komprimieren. In einer Mehrbenutzerumgebung darf SrcName während der Komprimierung nicht von einem anderen Benutzer geöffnet sein. Wenn SrcName nicht geschlossen oder nicht für die exklusive Verwendung verfügbar ist, tritt ein Fehler auf.

Da **CompactDatabase** eine Kopie der Datenbank erstellt, muss genügend Speicherplatz für das Original und die Kopie der Datenbank vorhanden sein. Wenn nicht genügend Speicherplatz vorhanden ist, tritt bei der Komprimierung ein Fehler auf. Die Kopie der DstName-Datenbank muss sich nicht auf demselben Datenträger wie SrcName befinden. Nach erfolgreicher Komprimierung einer Datenbank können Sie die SrcName-Datei löschen und die komprimierte DstName-Datei in den ursprünglichen Dateinamen umbenennen.

Die **CompactDatabase**-Methode kopiert alle Daten und die Einstellungen für die Sicherheitsberechtigung aus der durch SrcName angegebenen Datenbank in die durch DstName angegebene Datenbank.

> [!NOTE]
> Da die **CompactDatabase**-Methode keine Microsoft Access-Objekte konvertiert, sollten Sie **CompactDatabase** nicht zum Konvertieren einer Datenbank verwenden, die solche Objekte enthält.

## <a name="encrypted-linked-tables"></a>Verschlüsselte verknüpfte Tabellen

Verschlüsselte Kennwörter sind vom Dateiformat der Datenbank, die Sie verwenden, abhängig. Wenn Sie eine Access 2003 (.mdb) oder frühere Version der Datenbank verwenden, haben Sie ein Kennwort zum Schützen der Datenbank und ein weiteres Kennwort zum Verschlüsseln der Datenbank. Bei Datenbanken der Version Access 2007 (.accdb) und höher (.mdb) können Sie die Datenbank nur mit einem Kennwort verschlüsseln und schützen, da die Option zur Verwendung von zwei verschiedenen Kennwörtern entfernt wurde.

> [!NOTE]
> Für Access 2007-Datenbanken (ACCDB) ist das Kennwort der Verschlüsselungsschlüssel.

Sie können den folgenden VBA-Beispielcode für eine Befehlsschaltfläche verwenden:

```vb
    Private Sub Command0_Click()
    
    Dim strSourcePath As String
    Dim strDestPath As String
    
    strSourcePath = "<path>\sourceDb.accdb"
    strDestPath = "<path>\destDb.accdb"
    
    DBEngine.CompactDatabase strSourcePath, strDestPath, dbLangGeneral & ";pwd=Access", dbVersion120, ";pwd=Access"
    
    Set CurrentDatabase = CurrentDb
    Set LinkedTableDef = CurrentDatabase.CreateTableDef 
    ("My Linked Table")
    LinkedTableDef.Connect = "MS Access;pwd=Access";database=" & strDestPath
    LinkedTableDef.RefreshLink
    
    
    MsgBox "Finished"
    
    End Sub 
```

<br/>

Im folgenden Codebeispiel wird gezeigt, wie Sie CompactDatabase mit einem Kennwort (Verschlüsselungsschlüssel) verwenden und dann eine Verknüpfung zu einer Tabelle in dieser komprimierten Datenbank herstellen. Beachten Sie, dass ein Kennwort eingegeben werden muss.

```vb
    Private Sub CompactAndLink_Click() 
     
    Dim strSourcePath As String
    Dim strDestPath As String
    Dim strSourceTableName As String
    Dim strDestTableName As String
    Dim tdf As TableDef
     
    strSourcePath = "<path>\<database>.accdb"
    strDestPath = "<path>\<database>.accdb"
    strSourceTableName = "<table name in destination database>"
    strDestTableName = "<linked table name>"
     
    ' Compact source database into new destination database with encrypted password
    DBEngine.CompactDatabase strSourcePath, strDestPath, dbLangGeneral & ";pwd=Access", dbVersion120, ";pwd=Access"
     
    ' Link to one of the tables in the destination database
    ' Password must be provided in the Connect property
     
    Set CurrentDatabase = CurrentDb
    Set tdf = CurrentDatabase.CreateTableDef(strDestTableName)
       
        With tdf
            .Connect = ";pwd=Access" & ";DATABASE=" & strDestPath
            .SourceTableName = strSourceTableName
        End With
        
    CurrentDatabase.TableDefs.Append tdf
     
    MsgBox "Database compacted and encrypted password applied. Link to table also completed."
     
    End Sub
```
