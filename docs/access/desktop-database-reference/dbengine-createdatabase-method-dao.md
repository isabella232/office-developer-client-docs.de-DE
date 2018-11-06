---
title: DBEngine.CreateDatabase-Methode (DAO)
TOCTitle: CreateDatabase Method
ms:assetid: d5821a4b-483a-b8fa-e929-5f036057d8c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835033(v=office.15)
ms:contentKeyID: 48547966
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052972
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e9c77eabfc0689c6696c4ea6c8b4998b6b345458
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998350"
---
# <a name="dbenginecreatedatabase-method-dao"></a>DBEngine.CreateDatabase-Methode (DAO)

**Betrifft**: Access 2013, Office 2013

Erstellt ein neues **[Database](database-object-dao.md)** -Objekt, speichert die Datenbank auf einem Datenträger und gibt ein geöffnetes **Database**-Objekt zurück (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . CreateDatabase (***Name***, ***Gebietsschema***, ***Option***)

*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.

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
<th><p>Erforderlich oder optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Eine Zeichenfolge bis zu 255 Zeichen lang sein darf, die den Namen der Datenbankdatei ist, den Sie erstellen. Der vollständige Pfad und der Dateiname kann sein. Wenn Ihr Netzwerk unterstützt, Sie können auch angeben einen Netzwerkpfad wie &quot; \\server1\share1\dir1\db1&quot;. Sie können mit dieser Methode nur Microsoft Access-Datenbankdateien erstellen.</p></td>
</tr>
<tr class="even">
<td><p><em>Gebietsschema</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><ul>
<li><p>Ein Zeichenfolgenausdruck, der eine Sortierreihenfolge zum Erstellen der Datenbank angibt, wie unter Einstellungen festgelegt. Wenn Sie dieses Argument nicht angeben, tritt ein Fehler auf.</p></li>
<li><p>Sie können auch ein Kennwort für das neue <strong>Database</strong> -Objekt erstellen, indem Sie die Kennwortzeichenfolge (beginnend mit &quot;; Pwd =&quot; ) mit einer Konstante im Argument <em>Locale</em> verknüpfen, wie folgt:</p></li>
<li><p>DbLangSpanish &amp; &quot;; Pwd = NewPassword&quot;</p></li>
<li><p>Wenn Sie das standardmäßige <em>locale</em> verwenden möchten, aber ein Kennwort angeben, geben Sie für das Argument <em>locale</em> einfach eine Kennwortzeichenfolge an:</p></li>
<li><p>&quot;; Pwd = NewPassword&quot;</p></li>
<li><p>[!HINWEIS] Verwenden Sie sichere Kennwörter aus Groß- und Kleinbuchstaben, Zahlen und Symbolen. Unsichere Kennwörter enthalten keine Kombination dieser Elemente. Sicheres Kennwort: Y6dh!et5. Unsicheres Kennwort: Haus27. Verwenden Sie ein sicheres Kennwort, das Sie sich gut merken können, damit Sie es nicht aufschreiben müssen.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><em>Option</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine Konstante oder eine Kombination aus Konstanten, die eine oder mehrere Optionen angibt, wie unter Einstellungen festgelegt. Sie können Optionen kombinieren, indem Sie die Summe der entsprechenden Konstanten bilden.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Sie können eine der folgenden Konstanten für das Argument locale verwenden, um die **[CollatingOrder](database-collatingorder-property-dao.md)**-Eigenschaft von Text für Zeichenfolgenvergleiche anzugeben.

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
<td><p>Arabisch</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangChineseSimplified</strong></p></td>
<td><p>Chinesisch (Vereinfacht)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangChineseTraditional</strong></p></td>
<td><p>Chinesisch (Traditionell)</p></td>
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


Sie können eine oder mehrere der folgenden Konstanten im Argument options verwenden, um anzugeben, welche Version das Datenformat haben soll und ob die Datenbank verschlüsselt werden soll.

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
<td><p>Erstellt eine verschlüsselte Datenbank.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion10</strong></p></td>
<td><p>Erstellt eine Datenbank, die das Dateiformat der Version 1.0 des Microsoft Jet-Datenbankmoduls verwendet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion11</strong></p></td>
<td><p>Erstellt eine Datenbank, die das Dateiformat der Version 1.1 des Microsoft Jet-Datenbankmoduls verwendet.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion20</strong></p></td>
<td><p>Erstellt eine Datenbank, die das Dateiformat der Version 2.0 des Microsoft Jet-Datenbankmoduls verwendet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion30</strong></p></td>
<td><p>Erstellt eine Datenbank, die das Dateiformat der Version 3.0 des Microsoft Jet-Datenbankmoduls verwendet (kompatibel mit Version 3.5).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion40</strong></p></td>
<td><p>Erstellt eine Datenbank, die das Dateiformat der Version 4.0 des Microsoft Jet-Datenbankmoduls verwendet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion120</strong></p></td>
<td><p>Erstellt eine Datenbank, die das Dateiformat der Version 12.0 des Microsoft Access-Datenbankmoduls verwendet.</p></td>
</tr>
</tbody>
</table>


Wenn Sie die Verschlüsselungskonstante weglassen, erstellt **CreateDatabase** eine nicht verschlüsselte Datenbank.

Verwenden Sie die **CreateDatabase**-Methode zum Erstellen und Öffnen einer neuen, leeren Datenbank, und geben Sie das **Database**-Objekt zurück. Mithilfe zusätzlicher DAO-Objekte müssen Sie dessen Struktur und Inhalt vollständig angeben. Wenn Sie eine vorhandene Datenbank teilweise oder vollständig kopieren möchten, können Sie unter Verwendung der **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** -Methode eine Kopie erstellen und diese anpassen.

