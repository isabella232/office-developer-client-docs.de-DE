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
ms.openlocfilehash: e988eec4b3997bb24bf3a9aa0bb7faed1629b1f1
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950104"
---
# <a name="dbenginecreatedatabase-method-dao"></a><span data-ttu-id="223bd-102">DBEngine.CreateDatabase-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="223bd-102">DBEngine.CreateDatabase method (DAO)</span></span>

<span data-ttu-id="223bd-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="223bd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="223bd-p101">Erstellt ein neues **[Database](database-object-dao.md)** -Objekt, speichert die Datenbank auf einem Datenträger und gibt ein geöffnetes **Database**-Objekt zurück (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="223bd-p101">Creates a new **[Database](database-object-dao.md)** object, saves the database to disk, and returns an opened **Database** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="223bd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="223bd-106">Syntax</span></span>

<span data-ttu-id="223bd-107">*Ausdruck* . CreateDatabase (***Name***, ***Gebietsschema***, ***Option***)</span><span class="sxs-lookup"><span data-stu-id="223bd-107">*expression* .CreateDatabase(***Name***, ***Locale***, ***Option***)</span></span>

<span data-ttu-id="223bd-108">*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="223bd-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="223bd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="223bd-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="223bd-110">Name</span><span class="sxs-lookup"><span data-stu-id="223bd-110">Name</span></span></p></th>
<th><p><span data-ttu-id="223bd-111">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="223bd-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="223bd-112">Datentyp</span><span class="sxs-lookup"><span data-stu-id="223bd-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="223bd-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="223bd-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="223bd-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="223bd-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="223bd-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="223bd-115">Required</span></span></p></td>
<td><p><span data-ttu-id="223bd-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-117">Eine Zeichenfolge bis zu 255 Zeichen lang sein darf, die den Namen der Datenbankdatei ist, den Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="223bd-117">A String up to 255 characters long that is the name of the database file that you're creating.</span></span> <span data-ttu-id="223bd-118">Der vollständige Pfad und der Dateiname kann sein.</span><span class="sxs-lookup"><span data-stu-id="223bd-118">It can be the full path and file name.</span></span> <span data-ttu-id="223bd-119">Wenn Ihr Netzwerk unterstützt, Sie können auch angeben einen Netzwerkpfad wie &quot; \\server1\share1\dir1\db1&quot;.</span><span class="sxs-lookup"><span data-stu-id="223bd-119">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1&quot;.</span></span> <span data-ttu-id="223bd-120">Sie können mit dieser Methode nur Microsoft Access-Datenbankdateien erstellen.</span><span class="sxs-lookup"><span data-stu-id="223bd-120">You can only create Microsoft Access database files with this method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="223bd-121"><em>Gebietsschema</em></span><span class="sxs-lookup"><span data-stu-id="223bd-121"><em>Locale</em></span></span></p></td>
<td><p><span data-ttu-id="223bd-122">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="223bd-122">Required</span></span></p></td>
<td><p><span data-ttu-id="223bd-123"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-123"><strong>String</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="223bd-p103">Ein Zeichenfolgenausdruck, der eine Sortierreihenfolge zum Erstellen der Datenbank angibt, wie unter Einstellungen festgelegt. Wenn Sie dieses Argument nicht angeben, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="223bd-p103">A string expression that specifies a collating order for creating the database, as specified in Settings. You must supply this argument or an error occurs.</span></span></p></li>
<li><p><span data-ttu-id="223bd-126">Sie können auch ein Kennwort für das neue <strong>Database</strong> -Objekt erstellen, indem Sie die Kennwortzeichenfolge (beginnend mit &quot;; Pwd =&quot; ) mit einer Konstante im Argument <em>Locale</em> verknüpfen, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="223bd-126">You can also create a password for the new <strong>Database</strong> object by concatenating the password string (starting with &quot;;pwd=&quot; ) with a constant in the <em>locale</em> argument, like this:</span></span></p></li>
<li><p><span data-ttu-id="223bd-127">DbLangSpanish &amp; &quot;; Pwd = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="223bd-127">dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="223bd-128">Wenn Sie das standardmäßige <em>locale</em> verwenden möchten, aber ein Kennwort angeben, geben Sie für das Argument <em>locale</em> einfach eine Kennwortzeichenfolge an:</span><span class="sxs-lookup"><span data-stu-id="223bd-128">If you want to use the default <em>locale</em>, but specify a password, simply enter a password string for the <em>locale</em> argument:</span></span></p></li>
<li><p><span data-ttu-id="223bd-129">&quot;; Pwd = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="223bd-129">&quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="223bd-p104">[!HINWEIS] Verwenden Sie sichere Kennwörter aus Groß- und Kleinbuchstaben, Zahlen und Symbolen. Unsichere Kennwörter enthalten keine Kombination dieser Elemente. Sicheres Kennwort: Y6dh!et5. Unsicheres Kennwort: Haus27. Verwenden Sie ein sicheres Kennwort, das Sie sich gut merken können, damit Sie es nicht aufschreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="223bd-p104">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="223bd-135"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="223bd-135"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="223bd-136">Optional</span><span class="sxs-lookup"><span data-stu-id="223bd-136">Optional</span></span></p></td>
<td><p><span data-ttu-id="223bd-137"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-137"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-p105">Eine Konstante oder eine Kombination aus Konstanten, die eine oder mehrere Optionen angibt, wie unter Einstellungen festgelegt. Sie können Optionen kombinieren, indem Sie die Summe der entsprechenden Konstanten bilden.</span><span class="sxs-lookup"><span data-stu-id="223bd-p105">A constant or combination of constants that indicates one or more options, as specified in Settings. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="223bd-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="223bd-140">Remarks</span></span>

<span data-ttu-id="223bd-141">Sie können eine der folgenden Konstanten für das Argument locale verwenden, um die **[CollatingOrder](database-collatingorder-property-dao.md)**-Eigenschaft von Text für Zeichenfolgenvergleiche anzugeben.</span><span class="sxs-lookup"><span data-stu-id="223bd-141">You can use one of the following constants for the locale argument to specify the **[CollatingOrder](database-collatingorder-property-dao.md)** property of text for string comparisons.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="223bd-142">Konstante</span><span class="sxs-lookup"><span data-stu-id="223bd-142">Constant</span></span></p></th>
<th><p><span data-ttu-id="223bd-143">Sortierreihenfolge</span><span class="sxs-lookup"><span data-stu-id="223bd-143">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="223bd-144"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-144"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-145">Englisch, Deutsch, Französisch, Portugiesisch, Italienisch und modernes Spanisch</span><span class="sxs-lookup"><span data-stu-id="223bd-145">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="223bd-146"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-146"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-147">Arabisch</span><span class="sxs-lookup"><span data-stu-id="223bd-147">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="223bd-148"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-148"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-149">Chinesisch (Vereinfacht)</span><span class="sxs-lookup"><span data-stu-id="223bd-149">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="223bd-150"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-150"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-151">Chinesisch (Traditionell)</span><span class="sxs-lookup"><span data-stu-id="223bd-151">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="223bd-152"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-152"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-153">Russisch</span><span class="sxs-lookup"><span data-stu-id="223bd-153">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="223bd-154"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-154"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-155">Tschechisch</span><span class="sxs-lookup"><span data-stu-id="223bd-155">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="223bd-156"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-156"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-157">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="223bd-157">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="223bd-158"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-158"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-159">Griechisch</span><span class="sxs-lookup"><span data-stu-id="223bd-159">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="223bd-160"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-160"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-161">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="223bd-161">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="223bd-162"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-162"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-163">Ungarisch</span><span class="sxs-lookup"><span data-stu-id="223bd-163">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="223bd-164"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-164"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-165">Isländisch</span><span class="sxs-lookup"><span data-stu-id="223bd-165">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="223bd-166"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-166"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-167">Japanisch</span><span class="sxs-lookup"><span data-stu-id="223bd-167">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="223bd-168"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-168"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-169">Koreanisch</span><span class="sxs-lookup"><span data-stu-id="223bd-169">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="223bd-170"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-170"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-171">Nordeuropäische Sprachen (nur Version 1.0 des Microsoft Jet-Datenbankmoduls)</span><span class="sxs-lookup"><span data-stu-id="223bd-171">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="223bd-172"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-172"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-173">Norwegisch und Dänisch</span><span class="sxs-lookup"><span data-stu-id="223bd-173">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="223bd-174"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-174"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-175">Polnisch</span><span class="sxs-lookup"><span data-stu-id="223bd-175">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="223bd-176"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-176"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-177">Slowenisch</span><span class="sxs-lookup"><span data-stu-id="223bd-177">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="223bd-178"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-178"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-179">Spanisch (Traditionell)</span><span class="sxs-lookup"><span data-stu-id="223bd-179">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="223bd-180"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-180"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-181">Schwedisch und Finnisch</span><span class="sxs-lookup"><span data-stu-id="223bd-181">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="223bd-182"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-182"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-183">Thailändisch</span><span class="sxs-lookup"><span data-stu-id="223bd-183">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="223bd-184"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-184"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-185">Türkisch</span><span class="sxs-lookup"><span data-stu-id="223bd-185">Turkish</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="223bd-186">Sie können eine oder mehrere der folgenden Konstanten im Argument options verwenden, um anzugeben, welche Version das Datenformat haben soll und ob die Datenbank verschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="223bd-186">You can use one or more of the following constants in the options argument to specify which version the data format should have and whether or not to encrypt the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="223bd-187">Konstante</span><span class="sxs-lookup"><span data-stu-id="223bd-187">Constant</span></span></p></th>
<th><p><span data-ttu-id="223bd-188">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="223bd-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="223bd-189"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-189"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-190">Erstellt eine verschlüsselte Datenbank.</span><span class="sxs-lookup"><span data-stu-id="223bd-190">Creates an encrypted database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="223bd-191"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-191"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-192">Erstellt eine Datenbank, die das Dateiformat der Version 1.0 des Microsoft Jet-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="223bd-192">Creates a database that uses the Microsoft Jet database engine version 1.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="223bd-193"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-193"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-194">Erstellt eine Datenbank, die das Dateiformat der Version 1.1 des Microsoft Jet-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="223bd-194">Creates a database that uses the Microsoft Jet database engine version 1.1 file format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="223bd-195"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-195"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-196">Erstellt eine Datenbank, die das Dateiformat der Version 2.0 des Microsoft Jet-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="223bd-196">Creates a database that uses the Microsoft Jet database engine version 2.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="223bd-197"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-197"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-198">Erstellt eine Datenbank, die das Dateiformat der Version 3.0 des Microsoft Jet-Datenbankmoduls verwendet (kompatibel mit Version 3.5).</span><span class="sxs-lookup"><span data-stu-id="223bd-198">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="223bd-199"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-199"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-200">Erstellt eine Datenbank, die das Dateiformat der Version 4.0 des Microsoft Jet-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="223bd-200">Creates a database that uses the Microsoft Jet database engine version 4.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="223bd-201"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="223bd-201"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="223bd-202">Erstellt eine Datenbank, die das Dateiformat der Version 12.0 des Microsoft Access-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="223bd-202">Creates a database that uses the Microsoft Access database engine version 12.0 file format.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="223bd-203">Wenn Sie die Verschlüsselungskonstante weglassen, erstellt **CreateDatabase** eine nicht verschlüsselte Datenbank.</span><span class="sxs-lookup"><span data-stu-id="223bd-203">If you omit the encryption constant, **CreateDatabase** creates an un-encrypted database.</span></span>

<span data-ttu-id="223bd-p106">Verwenden Sie die **CreateDatabase**-Methode zum Erstellen und Öffnen einer neuen, leeren Datenbank, und geben Sie das **Database**-Objekt zurück. Mithilfe zusätzlicher DAO-Objekte müssen Sie dessen Struktur und Inhalt vollständig angeben. Wenn Sie eine vorhandene Datenbank teilweise oder vollständig kopieren möchten, können Sie unter Verwendung der **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** -Methode eine Kopie erstellen und diese anpassen.</span><span class="sxs-lookup"><span data-stu-id="223bd-p106">Use the **CreateDatabase** method to create and open a new, empty database, and return the **Database** object. You must complete its structure and content by using additional DAO objects. If you want to make a partial or complete copy of an existing database, you can use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method to make a copy that you can customize.</span></span>

